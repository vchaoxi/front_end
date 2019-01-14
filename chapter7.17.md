# 闭包


**什么是闭包** 

函数嵌套函数，内部函数可以引用外部函数的参数和变量，参数和变量不会被垃圾回收机制收回

```
function aaa(a){      
      var b = 5;      
      function bbb(){
           a++;
           b++;
         alert(a);
         alert(b);
      }
      return bbb;
  }

 var ccc = aaa(2);

 ccc();
 ccc();
 ```
 
 
改写成封闭函数的形式：

```
var ccc = (function(a){

  var b = 5;
  function bbb(){
       a++;
       b++;
     alert(a);
     alert(b);
  }
  return bbb;

})(2);

ccc();
ccc();
```


**用处 **
1、将一个变量长期驻扎在内存当中，可用于循环中存索引值

```
<script type="text/javascript">
    window.onload = function(){
        var aLi = document.getElementsByTagName('li');
        for(var i=0;i<aLi.length;i++)
        {
            (function(i){
                aLi[i].onclick = function(){
                    alert(i);
                }
            })(i);
        }
    }
</script>
......
<ul>
    < li>111</li>
    < li>222</li>
    <  l i>333</li>
    < li>444</li>
    < li>555</li>
</ul>
```

2、私有变量计数器，外部无法访问，避免全局变量的污染


```
<script type="text/javascript">

var count = (function(){
    var a = 0;
    function add(){
        a++;
        return a;
    }

    return  add;

})()

count();
count();

var nowcount = count();

alert(nowcount);

</script>
```

