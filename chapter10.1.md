# less、sass、stylus


它们是三种类似的样式动态语言，属于css预处理语言，它们有类似css的语法，为css赋予了动态语言的特性、如变量、继承、运算、函数等。这么做是为了css的编写和维护。

它们使用的文件分别是：.less、.scss、*.styl,这些文件是不能再网页上直接使用的，最终要编译成css文件来使用，编译的方法有软件编译，或者用nodejs程序。

less、sass编译软件：
http://koala-app.com/index-zh.html

less中文网址：http://lesscss.cn/

## less语法：
1、注释
```
    // 不会被编译的注释
    /* 会被编译的注释 */
    ```
2、变量

```
@w:200px;
.box{
    width:@w;
    height:@w;
    background-color:red;
}
```

3、混合

```
.border{
    border:1px solid #ddd;
}
.box(@w:100px,@h:50px,@bw:1px){
    width:@w;
    height:@h;
    border:@bw solid #ddd;
}
.box{
    .border;
    background-color:red;
}
```

4、匹配模式

```
.p(r){
    postion:relative;
}
.p(a){
    postion:absolute;
}
.p(f){
    postion:fixed;
}
.box{
    .p(f);
}
```


5、运算

```
@w:300px;
.box{
    width:@w+20;
}
```
4、嵌套

```
.list{    
    li{
        ...
    }
    a{
        ...
        &:hover{
            ...
        }
    }
    span{
        ...
    }
}
```


5、导入

```
// 导入common.less,导入a.css文件

@import "common";
@import (less) "a.css";
```
