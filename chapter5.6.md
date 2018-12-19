#CSS3 animation动画


1、@keyframes 定义关键帧动画

2、animation-name 动画名称

3、animation-duration 动画时间

4、animation-timing-function 动画曲线

- linear 匀速
- ease 开始和结束慢速
- ease-in 开始是慢速
- ease-out 结束时慢速
- ease-in-out 开始和结束时慢速steps 动画步数

5、animation-delay 动画延迟

6、animation-iteration-count 动画播放次数 n|infinite

7、animation-direction

 - normal 默认动画结束不返回
 - Alternate 动画结束后返回
 
8、animation-play-state 动画状态

 - paused 停止
 - running 运动
 
9、animation-fill-mode 动画前后的状态

 -  none 不改变默认行为
 - forwards 当动画完成后，保持最后一个属性值（在最后一个关键帧中定义）
 - backwards 在 animation-delay 所指定的一段时间内，在动画显示之前，应用开始属性值（在第一个关键帧中定义）
 - both 向前和向后填充模式都被应用
 
10、animation:name duration timing-function delay iteration-count direction;同时设置多个属性

##举例：（人物走路动画）


```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>走路动画</title>
    <style type="text/css">        
        .box{
            width:120px;
            height:180px;
            border:1px solid #ccc;            
            margin:50px auto 0;
            position:relative;
            overflow:hidden;            
        }

        .box img{
            display:block;
            width:960px;
            height:182px;
            position: absolute;
            left:0;
            top:0;
            animation:walking 1.0s steps(8) infinite;            
        }
        @keyframes walking{
            from{
                left:0px;
            }

            to{
                left:-960px;
            }
        }
    < /style>
</head>
<body>
    < div class="box">< img src="images/walking.png"></div>
</body>
</html>
```


动画中使用的图片如下：

![示例图片](/assets/333333333333333333333333333.png)