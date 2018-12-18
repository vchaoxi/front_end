#css选择器


常用的选择器有如下几种：
**
1、标签选择器**

标签选择器，此种选择器影响范围大，建议尽量应用在层级选择器中。
举例：

```
*{margin:0;padding:0}
div{color:red}   


<div>....</div>   <!-- 对应以上两条样式 -->
<div class="box">....</div>   <!-- 对应以上两条样式 -->
```


**2、id选择器**

通过id名来选择元素，元素的id名称不能重复，所以一个样式设置项只能对应于页面上一个元素，不能复用，id名一般给程序使用，所以不推荐使用id作为选择器。
举例：

```
\# box{ color:red} 

<div id="box">....</div>   <!-- 对应以上一条样式，其它元素不允许应用此样式 -->
```


**3、类选择器**

通过类名来选择元素，一个类可应用于多个元素，一个元素上也可以使用多个类，应用灵活，可复用，是css中应用最多的一种选择器。
举例：

```
.red{color:red}
.big{font-size:20px}
.mt10{margin-top:10px} 

<div class="red">....</div>
<h1 class="red big mt10">....< /h1>
<p class="red mt10">....</p>
```


**4、层级选择器**

主要应用在选择父元素下的子元素，或者子元素下面的子元素，可与标签元素结合使用，减少命名，同时也可以通过层级，防止命名冲突。
举例：

```
.box span{color:red}
.box .red{color:pink}
.red{color:red}

<div class="box">
    < span>....</span>
    < a href="#" class="red">....</a>
</div>


<h3 class="red">....</h3>
```


**5、组选择器**

多个选择器，如果有同样的样式设置，可以使用组选择器。
举例：

```
.box1,.box2,.box3{width:100px;height:100px}
.box1{background:red}
.box2{background:pink}
.box2{background:gold}

< div class="box1">....</div>
< div class="box2">....</div>
< div class="box3">....</div>
```


**6、伪类及伪元素选择器**

常用的伪类选择器有hover，表示鼠标悬浮在元素上时的状态，伪元素选择器有before和after,它们可以通过样式在元素中插入内容。

```
.box1:hover{color:red}
.box2:before{content:'行首文字';}
.box3:after{content:'行尾文字';}


<div class="box1">....</div>
<div class="box2">....</div>
<div class="box3">....</div>
```
