# 函数

函数就是重复执行的代码片。

#### 函数定义与执行

```
<script type="text/javascript">
    // 函数定义
    function aa(){
        alert('hello!');
    }
    // 函数执行
    aa();
</script>
```


变量与函数预解析 


JavaScript解析过程分为两个阶段，先是编译阶段，然后执行阶段，在编译阶段会将function定义的函数提前，并且将var定义的变量声明提前，将它赋值为undefined。

```
<script type="text/javascript">    
    aa();       // 弹出 hello！
    alert(bb);  // 弹出 undefined
    function aa(){
        alert('hello!');
    }
    var bb = 123;
</script>
```

#### 提取行间事件 

在html行间调用的事件可以提取到javascript中调用，从而做到结构与行为分离。

```

<!--行间事件调用函数   -->
<script type="text/javascript">        
    function myalert(){
        alert('ok!');
    }
</script>
......
<input type="button" name="" value="弹出" onclick="myalert()">

<!-- 提取行间事件 -->
<script type="text/javascript">

window.onload = function(){
    var oBtn = document.getElementById('btn1');
    oBtn.onclick = myalert;
    function myalert(){
        alert('ok!');
    }
}    
</script>
......
<input type="button" name="" value="弹出" id="btn1">
```

#### 匿名函数

定义的函数可以不给名称，这个叫做匿名函数，可以将匿名函数直接赋值给元素绑定的事件来完成匿名函数的调用。


```
<script type="text/javascript">

window.onload = function(){
    var oBtn = document.getElementById('btn1');
    /*
    oBtn.onclick = myalert;
    function myalert(){
        alert('ok!');
    }
    */
    // 直接将匿名函数赋值给绑定的事件

    oBtn.onclick = function (){
        alert('ok!');
    }
}

</script>
```


#### 函数传参
 
```
<script type="text/javascript">
    function myalert(a){
        alert(a);
    }
    myalert(12345);
</script>
```

#### 函数'return'关键字 

函数中'return'关键字的作用：

1、返回函数执行的结果

2、结束函数的运行

3、阻止默认行为

```
<script type="text/javascript">
function add(a,b){
    var c = a + b;
    return c;
    alert('here!');
}

var d = add(3,4);
alert(d);  //弹出7
</script>
```

