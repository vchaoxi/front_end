# 循环语句

程序中进行有规律的重复性操作，需要用到循环语句。

#### for循环

```

for(var i=0;i<len;i++)
{
    ......
}
```


#### while循环

```
var i=0;

while(i<8){

    ......

    i++;

}
```

#### 数组去重

```
var aList = [1,2,3,4,4,3,2,1,2,3,4,5,6,5,5,3,3,4,2,1];

var aList2 = [];

for(var i=0;i<aList.length;i++)
{
    if(aList.indexOf(aList[i])==i)
    {
        aList2.push(aList[i]);
    }
}

alert(aList2);
```

