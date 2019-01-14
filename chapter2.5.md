# CSS盒子模型


#### 盒子模型解释 

元素在页面中显示成一个方块，类似一个盒子，CSS盒子模型就是使用现实中盒子来做比喻，帮助我们设置元素对应的样式。盒子模型示意图如下：

![盒子模型示例图片](/assets/view01.jpg)

把元素叫做盒子，设置对应的样式分别为：盒子的边框(border)、盒子内的内容和边框之间的间距(padding)、盒子与盒子之间的间距(margin)。


#### 设置边框 

设置一边的边框，比如顶部边框，可以按如下设置：

```
border-top-color:red;    /* 设置顶部边框颜色为红色 */  
border-top-width:10px;   /* 设置顶部边框粗细为10px */   
border-top-style:solid;  /* 设置顶部边框的线性为实线，常用的有：solid(实线)  
  dashed(虚线)  dotted(点线); */
  ```
  
  
上面三句可以简写成一句：

```

border-top:10px solid red;
```


设置其它三个边的方法和上面一样，把上面的'top'换成'left'就是设置左边，换成'right'就是设置右边，换成'bottom'就是设置底边。

四个边如果设置一样，可以将四个边的设置合并成一句：

```
border:10px solid red;
```


#### 设置内间距padding


设置盒子四边的内间距，可设置如下：

```
padding-top：20px;     /* 设置顶部内间距20px */ 
padding-left:30px;     /* 设置左边内间距30px */ 
padding-right:40px;    /* 设置右边内间距40px */ 
padding-bottom:50px;   /* 设置底部内间距50px */
```


上面的设置可以简写如下：

```
padding：20px 40px 50px 30px; /* 
四个值按照顺时针方向，分别设置的是 上 右 下 左  
四个方向的内边距值。 */
```


padding后面还可以跟3个值，2个值和1个值，它们分别设置的项目如下：

```
padding：20px 40px 50px; /* 设置顶部内边距为20px，左右内边距为40px，底部内边距为50px */ 
padding：20px 40px; /* 设置上下内边距为20px，左右内边距为40px*/ 
padding：20px; /* 设置四边内边距为20px */
```


#### 设置外间距margin


外边距的设置方法和padding的设置方法相同，将上面设置项中的'padding'换成'margin'就是外边距设置方法。

#### 盒子模型的尺寸

按照下面代码制作页面：

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>盒子的真实尺寸</title>
    <style type="text/css">
        .box01{width:50px;height:50px;background-color:gold;}
        .box02{width:50px;height:50px;background-color:gold;border:50px
         solid #000}
        .box03{width:50px;height:50px;background-color:gold;border:50px
         solid #000;padding: 50px;}
    </style>
</head>
<body>
    <div class="box01">1</div>
    <br />
    <div class="box02">2</div>
    <br />
    <div class="box03">3</div>
</body>
</html>
```


页面显示效果如下：

![](/assets/2.jpg)


通过上面的页面得出结论：盒子的width和height设置的是盒子内容的宽和高，不是盒子本身的宽和高，盒子的真实尺寸计算公式如下：

- 盒子宽度 = width + padding左右 + border左右
- 盒子高度 = height + padding上下 + border上下


#### 思考题：

1.在布局中，如果我想增大内容和边框的距离，又不想改变盒子显示的尺寸，应该怎么做？

####  课堂练习 
请制作图中所示的标题：

![](/assets/8.jpg)

#### margin相关技巧 
1、设置元素水平居中： margin:x auto;
2、margin负值让元素位移及边框合并

####  外边距合并

外边距合并指的是，当两个垂直外边距相遇时，它们将形成一个外边距。合并后的外边距的高度等于两个发生合并的外边距的高度中的较大者。解决方法如下：

1、使用这种特性
2、设置一边的外边距，一般设置margin-top
3、将元素浮动或者定位

##### margin-top 塌陷

在两个盒子嵌套时候，内部的盒子设置的margin-top会加到外边的盒子上，导致内部的盒子margin-top设置失败，解决方法如下：

1、外部盒子设置一个边框
2、外部盒子设置 overflow:hidden
3、使用伪元素类：

```
.clearfix:before{
    content: '';
    display:table;
}
```