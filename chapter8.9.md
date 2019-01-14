# jquery动画

通过animate方法可以设置元素某属性值上的动画，可以设置一个或多个属性值，动画执行完成后会执行一个函数。

```

$('#div1').animate({
    width:300,
    height:300
},1000,swing,function(){
    alert('done!');
});
```


参数可以写成数字表达式：

```
$('#div1').animate({
    width:'+=100',
    height:300
},1000,swing,function(){
    alert('done!');
});
```
