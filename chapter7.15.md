#变量作用域

变量作用域指的是变量的作用范围，javascript中的变量分为全局变量和局部变量。

1、全局变量：在函数之外定义的变量，为整个页面公用，函数内部外部都可以访问。
2、局部变量：在函数内部定义的变量，只能在定义该变量的函数内部访问，外部无法访问。

```
< script type="text/javascript">
    //全局变量
    var a = 12;
    function myalert()
    {
        //局部变量
        var b = 23;
        alert(a);
        alert(b);
    }
    myalert(); //弹出12和23
    alert(a);  //弹出12    
    alert(b);  //出错
< /script>
```

