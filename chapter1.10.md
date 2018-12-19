#html内嵌框架


##html内嵌框架

&lt;iframe&gt;标签会创建包含另外一个html文件的内联框架（即行内框架），src属性来定义另一个html文件的引用地址，frameborder属性定义边框，scrolling属性定义是否有滚动条，代码如下：

```
<iframe src="http://www..." frameborder="0" scrolling="no"></iframe>
```


##内嵌框架与a标签配合使用
a标签的target属性可以将链接到的页面直接显示在当前页面的iframe中，代码如下：

```
<a href="01.html" target="myframe">页面一</a>
<a href="02.html" target="myframe">页面二</a>
<a href="03.html" target="myframe">页面三</a>
<iframe src="01.html" frameborder="0" scrollin"no" name="myframe"></iframe>
```

