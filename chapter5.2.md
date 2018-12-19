#CSS3新增选择器

1、E:nth-child(n)：匹配元素类型为E且是父元素的第n个子元素

```
<style type="text/css">            
    .list div:nth-child(2){
        background-color:red;
    }
</style>
......
<div class="list">
    <h2>1< /h2>
    <div>2< /div>
    <div>3<  /div>
    <div>4< /div>
    <div>5< /div>
</div>

<!-- 第2个子元素div匹配 -->
```

2、E:nth-last-child(n)：匹配元素类型为E且是父元素的倒数第n个子元素（与上一项顺序相反）

3、E:first-child：匹配元素类型为E且是父元素的第一个子元素

4、E:last-child：匹配元素类型为E且是父元素的最后一个子元素

5、E:only-child：匹配元素类型为E且是父元素中唯一的子元素

6、E:nth-of-type(n)：匹配父元素的第n个类型为E的子元素

7、E:nth-last-of-type(n)：匹配父元素的倒数第n个类型为E的子元素（与上一项顺序相反）

8、E:first-of-type：匹配父元素的第一个类型为E的子元素

9、E:last-of-type：匹配父元素的最后一个类型为E的子元素

10、E:only-of-type：匹配父元素中唯一子元素是E的子元素

11、E:empty 选择一个空的元素

12、E:enabled 可用的表单控件

13、E:disabled 失效的表单控件

14、E:checked 选中的checkbox

15、E:not(s) 不包含某元素


 ```
  <s tyle type="text/css">            
    .list div:not(:nth-child(2)){
        background-color:red;
    }
</style>
......
<div class="list">
    <h2>1< /h2>
    <div>2< /div>
    <div>3< /div>
    <div>4< /div>
    <div>5< /div>
</div>

<!-- 第 3、4、5 子元素div匹配 -->
```

  
16、E:target 对应锚点的样式

```
<style type="text/css">
    h2:target{
        color:red;
    }
</style>
......
<a href="#tit01">标题一</a>
......
<h2 id="tit01">标题一</h2>

<!-- 点击链接，h2标题变红 -->

``` 


17、E > F E元素下面第一层子集
18、E ~ F E元素后面的兄弟元素
19、E + F 紧挨着的兄弟元素

属性选择器：
1、E[data-attr] 含有data-attr属性的元素

```
<style type="text/css">
    div[data-attr='ok']{
        color:red;
    }
</style>
......
<div data-attr="ok">这是一个div元素< /div>
<!-- 点击链接，h2标题变红 -->
```




2、E[data-attr='ok'] 含有data-attr属性的元素且它的值为“ok”

3、E[data-attr^='ok'] 含有data-attr属性的元素且它的值的开头含有“ok”

4、E[data-attr$='ok'] 含有data-attr属性的元素且它的值的结尾含有“ok”

5、E[data-attr*='ok'] 含有data-attr属性的元素且它的值中含有“ok”