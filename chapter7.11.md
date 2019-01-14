# 字符串处理方法

1、字符串合并操作：“ + ”

2、parseInt() 将数字字符串转化为整数

3、parseFloat() 将数字字符串转化为小数

4、split() 把一个字符串分隔成字符串组成的数组

5、charAt() 获取字符串中的某一个字符

6、indexOf() 查找字符串是否含有某字符

7、substring() 截取字符串 用法： substring(start,end)（不包括end）

8、toUpperCase() 字符串转大写

9、toLowerCase() 字符串转小写

#### 字符串反转

```
var str = 'asdfj12jlsdkf098';
var str2 = str.split('').reverse().join('');

alert(str2);
```