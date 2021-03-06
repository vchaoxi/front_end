# 移动端页面布局


## 移动端app分类

1、Native App 原生app手机应用程序
使用原生的语言开发的手机应用，Android系统用的是java，iOS系统用的是object-C

2、Hybrid App 混合型app手机应用程序
混合使用原生的程序和html5页面开发的手机应用

3、Web App 基于Web的app手机应用程序
完全使用html5页面加前端js框架开发的手机应用

## Viewport 视口

视口是移动设备上用来显示网页的区域，一般会比移动设备可视区域大，宽度可能是980px或者1024px，目的是为了显示下整个为PC端设计的网页，这样带来的后果是移动端会出现横向滚动条，为了避免这种情况，移动端会将视口缩放到移动端窗口的大小。这样会让网页不容易观看，可以用 meta 标签，name=“viewport ” 来设置视口的大小，将视口的大小设置为和移动设备可视区一样的大小。

设置方法如下：

```
<head>
......
<meta name="viewport" content="width=device-width, user-scalable=no,
 initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
......
</head>
```


pc端与移动端渲染网页过程：

![示例图片](/assets/8888.jpg)

## 视网膜屏幕（retina屏幕）清晰度解决方案

视网膜屏幕指的是屏幕的物理像素密度更高的屏幕，物理像素可以理解为屏幕上的一个发光点，无数发光的点组成的屏幕，视网膜屏幕比一般屏幕的物理像素点更小，常见有2倍的视网膜屏幕和3倍的视网膜屏幕，2倍的视网膜屏幕，它的物理像素点大小是一般屏幕的1/4,3倍的视网膜屏幕，它的物理像素点大小是一般屏幕的1/9。

图像在视网膜屏幕上显示的大小和在一般屏幕上显示的大小一样，但是由于视网膜屏幕的物理像素点比一般的屏幕小，图像在上面好像是被放大了，图像会变得模糊，为了解决这个问题，可以使用比原来大一倍的图像，然后用css样式强制把图像的尺寸设为原来图像尺寸的大小，就可以解决模糊的问题。

清晰度解决过程示意图：
![
示例图片](/assets/8889.jpg)

背景图强制改变大小，可以使用background新属性

#### background新属性 

background-size:

 - length：用长度值指定背景图像大小。不允许负值。
 - percentage：用百分比指定背景图像大小。不允许负值。
 - auto：背景图像的真实大小。
 - cover：将背景图像等比缩放到完全覆盖容器，背景图像有可能超出容器。
 - contain：将背景图像等比缩放到宽度或高度与容器的宽度或高度相等，背景图像始终被包含在容器内。
 
## PC及移动端页面适配方法

设备屏幕有多种不同的分辨率，页面适配方案有如下几种：

1、全适配：流体布局+响应式布局

2、移动端适配：

 - 流体布局+少量响应式
 - 基于rem的布局
 - 弹性盒模型
 
 
## 流体布局

 - 流体布局，就是使用百分比来设置元素的宽度，元素的高度按实际高度写固定值，流体布局中，元素的边线无法用百分比，可以使用样式中的计算函数 calc() 来设置宽度，或者使用 box-sizing 属性将盒子设置为从边线计算盒子尺寸。

#### calc() 

可以通过计算的方式给元素加尺寸，比如： width：calc(25% - 4px);

#### box-sizing 

1、content-box 默认的盒子尺寸计算方式

2、border-box 置盒子的尺寸计算方式为从边框开始，盒子的尺寸，边框和内填充算在盒子尺寸内

## 响应式布局

响应式布局就是使用媒体查询的方式，通过查询浏览器宽度，不同的宽度应用不同的样式块，每个样式块对应的是该宽度下的布局方式，从而实现响应式布局。响应式布局的页面可以适配多种终端屏幕（pc、平板、手机）。

相应布局的伪代码如下：

```
@media (max-width:960px){
    .left_con{width:58%;}
    .right_con{width:38%;}
}
@media (max-width:768px){
    .left_con{width:100%;}
    .right_con{width:100%;}
}
```

## 基于rem的布局

首先了解em单位，em单位是参照元素自身的文字大小来设置尺寸，rem指的是参照根节点的文字大小，根节点指的是html标签，设置html标签的文字大小，其他的元素相关尺寸设置用rem，这样，所有元素都有了统一的参照标准，改变html文字的大小，就会改变所有元素用rem设置的尺寸大小。

#### cssrem安装

cssrem插件可以动态地将px尺寸换算成rem尺寸

下载本项目，比如：git clone https://github.com/flashlizi/cssrem (进入packages目录：Sublime Text -> Preferences -> Browse Packages... 复制下载的cssrem目录到刚才的packges目录里。 重启Sublime Text。

配置参数 参数配置文件：Sublime Text -> Preferences -> Package Settings -> cssrem px_to_rem - px转rem的单位比例，默认为40。 max_rem_fraction_length - px转rem的小数部分的最大长度。默认为6。 available_file_types - 启用此插件的文件类型。默认为：[".css", ".less", ".sass"]。

## 弹性盒模型布局

1、容器属性
display : flex
声明使用弹性盒布局


flex-direction : row | row-reverse | column | column-reverse
确定子元素排列的方向


flex-wrap : nowrap | wrap | wrap-reverse
元素超过父容器尺寸时是否换行


flex-flow : flex-direction | flex-wrap
同时设置flex-direction 和 flex-wrap


justify-content : flex-start | flex-end | center | space-between | space-around
子元素的尺寸确定之后，用此属性来设置flex-direction定义方向上的分布方式


align-items : flex-start | flex-end | center | baseline | stretch
子元素的尺寸确定之后，用此属性来设置flex-direction定义方向上的垂直方向的分布方式


align-content : flex-start | flex-end | center | space-between | space-around | stretch
设置多行子元素在行方向上的对齐方式


2、条目属性


flex : none | <' flex-grow '> <' flex-shrink >'? || <' flex-basis '>

同时设置flex-grow 和 flex-shrink 以及 flex-basis

flex-grow ： number

表示的是当父元素有多余的空间时，这些空间在不同子元素之间的分配比例

flex-shrink： number

当父元素的空间不足时，各个子元素的尺寸缩小的比例

flex-basis ：length | percentage | auto | content

用来确定弹性条目的初始主轴尺寸。

align-self ：auto | flex-start | flex-end | center | baseline | stretch

覆写父元素指定的对齐方式

order : integer

改变条目在容器中的出现顺序

