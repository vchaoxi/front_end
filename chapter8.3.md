#jquery选择器

**jquery用法思想一 **
选择某个网页元素，然后对它进行某种操作

**jquery选择器 **
jquery选择器可以快速地选择元素，选择规则和css样式相同，使用length属性判断是否选择成功。

```
$(document) //选择整个文档对象
$('li') //选择所有的li元素
$('#myId') //选择id为myId的网页元素
$('.myClass') // 选择class为myClass的元素
$('input[name=first]') // 选择name属性等于first的input元素
$('#ul1 li span') //选择id为为ul1元素下的所有li下的span元素
```

**对选择集进行修饰过滤(类似CSS伪类)**

```
$('#ul1 li:first') //选择id为ul1元素下的第一个li
$('#ul1 li:odd') //选择id为ul1元素下的li的奇数行
$('#ul1 li:eq(2)') //选择id为ul1元素下的第3个li
$('#ul1 li:gt(2)') // 选择id为ul1元素下的前三个之后的li
$('#myForm :input') // 选择表单中的input元素
$('div:visible') //选择可见的div元素
```

**对选择集进行函数过滤**

```
$('div').has('p'); // 选择包含p元素的div元素
$('div').not('.myClass'); //选择class不等于myClass的div元素
$('div').filter('.myClass'); //选择class等于myClass的div元素
$('div').first(); //选择第1个div元素
$('div').eq(5); //选择第6个div元素
```


**选择集转移**

```
$('div').prev('p'); //选择div元素前面的第一个p元素
$('div').next('p'); //选择div元素后面的第一个p元素
$('div').closest('form'); //选择离div最近的那个form父元素
$('div').parent(); //选择div的父元素
$('div').children(); //选择div的所有子元素
$('div').siblings(); //选择div的同级元素
$('div').find('.myClass'); //选择div内的class等于myClass的元素
```
