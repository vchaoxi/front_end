# 封闭函数


封闭函数是javascript中匿名函数的另外一种写法，创建一个一开始就执行而不用命名的函数。

一般定义的函数和执行函数：

```
function changecolor(){
    var oDiv = document.getElementById('div1');
    oDiv.style.color = 'red';
}
changecolor();
```


封闭函数：

```
(function(){
    var oDiv = document.getElementById('div1');
    oDiv.style.color = 'red';
})();
```


还可以在函数定义前加上“~”和“!”等符号来定义匿名函数

```
!function(){
    var oDiv = document.getElementById('div1');
    oDiv.style.color = 'red';
}()
```