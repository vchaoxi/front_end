#zeptojs

Zepto是一个轻量级的针对现代高级浏览器的JavaScript库， 它与jquery有着类似的api。 如果你会用jquery，那么你也会用zepto。Zepto的一些可选功能是专门针对移动端浏览器的；它的最初目标是在移动端提供一个精简的类似jquery的js库。

zepto官网：http://zeptojs.com/
zepto中文api：http://www.css88.com/doc/zeptojs_api/
zepto包含很多模块，默认下载版本包含的模块有Core, Ajax, Event, Form, IE模块，如果还需要其他的模块，可以自定义构建。
zepto自定义构建地址：http://github.e-sites.nl/zeptobuilder/


touch模块封装了针对移动端常用的事件，可使用此模块进行移动端特定效果开发，这些事件有：

 - tap 元素tap的时候触发，此事件类似click，但是比click快。
 - longTap 当一个元素被按住超过750ms触发。
 - swipe, swipeLeft, swipeRight, swipeUp, swipeDown 当元素被划过时触发。(可选择给定的方向)
