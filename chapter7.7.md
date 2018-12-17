#条件语句


通过条件来控制程序的走向，就需要用到条件语句。

####运算符 


1、算术运算符： +(加)、 -(减)、 *(乘)、 /(除)、 %(求余)
2、赋值运算符：=、 +=、 -=、 *=、 /=、 %=
3、条件运算符：==、===、>、>=、<、<=、!=、&&(而且)、||(或者)、!(否)

####if else

```
var a = 6;
if(a==1)
{
    alert( '语文');
}
else if(a==2)
{
    alert('数学');
}
else if(a==3)
{
    alert('英语');
}
else if(a==4)
{
    alert('美术');
}
else if(a==5)
{
    alert('舞蹈');
}
else
{
    alert('不补习');
}
```

####switch

```
var a = 6;

switch (a){
    case 1:
        alert('语文');
        break;
    case 2:
        alert('数学');
        break;
    case 3:
        alert('英语');
        break;
    case 4:
        alert('美术');
        break;
    case 5:
        alert('舞蹈');
        break;
    default:
        alert('不补习');
}
```
