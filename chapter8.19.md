# json

json是 JavaScript Object Notation 的首字母缩写，单词的意思是javascript对象表示法，这里说的json指的是类似于javascript对象的一种数据格式，目前这种数据格式比较流行，逐渐替换掉了传统的xml数据格式。

javascript对象字面量：

```

var tom = {
    name:'tom',
    age:18
}
```


json格式的数据：

```

{
    "name":'tom',
    "age":18
}
```


与json对象不同的是，json数据格式的属性名称需要用双引号引起来，用单引号或者不用引号会导致读取数据错误。

json的另外一个数据格式是数组，和javascript中的数组字面量相同。

```
['tom',18,'programmer']
```

