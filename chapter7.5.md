# 操作元素属性

获取的页面元素，就可以对页面元素的属性进行操作，属性的操作包括属性的读和写。

#### 操作属性的方法 

1、“.” 操作

2、“[ ]”操作

#### 属性写法

1、html的属性和js里面属性写法一样

2、“class” 属性写成 “className”

3、“style” 属性里面的属性，有横杠的改成驼峰式，比如：“font-size”，改成”style.fontSize”

通过“.”操作属性：

```
<script type="text/javascript">

    window.onload = function(){
        var oInput = document.getElementById('input1');
        var oA = document.getElementById('link1');
        // 读取属性值
        var val = oInput.value;
        var typ = oInput.type;
        var nam = oInput.name;
        var links = oA.href;
        // 写(设置)属性
        oA.style.color = 'red';
        oA.style.fontSize = val;
    }

</script>

......

<input type="text" name="setsize" id="input1" value="20px">
<a href="http://www.itcast.cn" id="link1">传智播客</a>
```


通过“[ ]”操作属性：


```

<script type="text/javascript">

    window.onload = function(){
        var oInput1 = document.getElementById('input1');
        var oInput2 = document.getElementById('input2');
        var oA = document.getElementById('link1');
        // 读取属性
        var val1 = oInput1.value;
        var val2 = oInput2.value;
        // 写(设置)属性
        // oA.style.val1 = val2; 没反应
        oA.style[val1] = val2;        
    }
</script>

......

<input type="text" name="setattr" id="input1" value="fontSize">
<input type="text" name="setnum" id="input2" value="30px">
<a href= " http://www.itcast.cn" id="link1">传智播客</a>
```


#### innerHTML 

innerHTML可以读取或者写入标签包裹的内容

```
<script type="text/javascript">
    window.onload = function(){
        var oDiv = document.getElementById('div1');
        //读取
        var txt = oDiv.innerHTML;
        alert(txt);
        //写入
        oDiv.innerHTML = '<a href="http://www.itcast.cn">传智播客<a/>';
    }
</script>

......

<div id="div1">这是一个div元素</div>
```

