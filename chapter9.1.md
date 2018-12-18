#移动端js事件


移动端的操作方式和PC端是不同的，移动端主要用手指操作，所以有特殊的touch事件，touch事件包括如下几个事件：

1、touchstart: //手指放到屏幕上时触发
2、touchmove: //手指在屏幕上滑动式触发
3、touchend: //手指离开屏幕时触发
4、touchcancel: //系统取消touch事件的时候触发，比较少用

移动端一般有三种操作，点击、滑动、拖动，这三种操作一般是组合使用上面的几个事件来完成的，所有上面的4个事件一般很少单独使用，一般是封装使用来实现这三种操作，可以使用封装成熟的js库。