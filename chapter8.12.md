jquery事件


# 事件函数列表：

```
blur() 元素失去焦点

focus() 元素获得焦点

change() 表单元素的值发生变化

click() 鼠标单击

dblclick() 鼠标双击

mouseover() 鼠标进入（进入子元素也触发）

mouseout() 鼠标离开（离开子元素也触发）

mouseenter() 鼠标进入（进入子元素不触发）

mouseleave() 鼠标离开（离开子元素不触发）

hover() 同时为mouseenter和mouseleave事件指定处理函数

mouseup() 松开鼠标

mousedown() 按下鼠标

mousemove() 鼠标在元素内部移动

keydown() 按下键盘

keypress() 按下键盘

keyup() 松开键盘

load() 元素加载完毕

ready() DOM加载完成

resize() 浏览器窗口的大小发生改变

scroll() 滚动条的位置发生变化

select() 用户选中文本框中的内容

submit() 用户递交表单

toggle() 根据鼠标点击的次数，依次运行多个函数

unload() 用户离开页面
```

**绑定事件的其他方式**

```
$(function(){
    $('#div1').bind('mouseover click', function(event) {
        alert($(this).html());
    });
});
```

**取消绑定事件**

```
$(function(){
    $('#div1').bind('mouseover click', function(event) {
        alert($(this).html());

        // $(this).unbind();
        $(this).unbind('mouseover');

    });
});
```
