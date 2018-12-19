#HTML5 音频和视频


html5增加了audio和video标签，提供了在页面上插入音频和视频的标准方法。

####audio标签 
支持格式：ogg、wav、mp3

对应属性：

1、autoplay 自动播放

2、controls 显示播放器

3、loop 循环播放

4、preload 预加载

5、muted 静音

举例：

```

<audio src="source/audio.mp3" autoplay controls loop preload></audio>

<!-- 或者用如下方式：  -->

<audio  autoplay controls loop preload>
    <source src="source/audio.mp3" type="">
    <source src="source/audio02.wav" type="">
</audio>
```


source标签的作用是提供多个媒体文件地址，如果一个地址的文件不兼容，就使用下一个地址。

####video标签 
支持格式：ogg、mp4、webM

属性：

1、width

2、height

3、Poster

可选第三方播放器：

1、cyberplayer

2、tencentPlayer

3、youkuplayer

