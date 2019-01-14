# swiper


swiper.js是一款成熟稳定的应用于PC端和移动端的滑动效果插件，一般用来触屏焦点图、触屏整屏滚动等效果。 swiper分为2.x版本和3.x版本，2.x版本支持低版本浏览器(IE7)，3.x放弃支持低版本浏览器，适合应用在移动端。

2.x版本中文网址：http://2.swiper.com.cn/

3.x版本中文网地址：http://www.swiper.com.cn/

## swiper使用方法：
```
<script type="text/javascript" src="js/swiper.min.js"></script>
......

<link rel="stylesheet" type="text/css" href="css/swiper.min.css">
......

<div class="swiper-container">
  <div class="swiper-wrapper">
    <div class="swiper-slide">slider1</div>
    <div class="swiper-slide">slider2</div>
    <div class="swiper-slide">slider3</div>
  </div>
    <div class="swiper-pagination"></div>
    <div class="swiper-button-prev"></div>
    <div class="swiper-button-next"></div>
</div>

<script> 
var swiper = new Swiper('.swiper-container', {
    pagination: '.swiper-pagination',
  prevButton: '.swiper-button-prev',
  nextButton: '.swiper-button-next',
    initialSlide :1,
  paginationClickable: true,
  loop: true,
  autoplay:3000,
  autoplayDisableOnInteraction:false
});
</script>
```


## swiper使用参数：


1、initialSlide：初始索引值，从0开始

2、direction：滑动方向 horizontal | vertical

3、speed：滑动速度，单位ms

4、autoplay：设置自动播放及播放时间

5、autoplayDisableOnInteraction：用户操作swipe后是否还自动播放，默认是true，不再自动播放

6、pagination：分页圆点

7、paginationClickable：分页圆点是否点击

8、prevButton：上一页箭头

9、nextButton：下一页箭头

10、loop：是否首尾衔接

11、onSlideChangeEnd：回调函数，滑动结束时执行

## swiper制作实例：


1、swiper制作移动端焦点图实例

2、swiper制作整页滚动效果