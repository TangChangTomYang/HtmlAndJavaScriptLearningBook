#### 005-多媒体标签


<br>
##HTML5 多媒体标签


***
<br>
####一、 video 标签 (HTML5标志性的标签)

**题外话:**
在HTML5 之前,我们的html语言只能处理图片数据和文字数据,在html5之后呢,我们的HTML5标签可以处理多媒体数据了.video 是我们html5的一个标志性标签。


- 1、什么是video标签？<br>
作用： 播放视频

- 2、格式(1):

```
<video src="../imgs/sb2.webm" poster="../imgs.abc.jpg" autoplay="autoplay" loop="loop" controls="controls"></video>


```
video标签常用属性
```
//video 标签的常用属性:
//src: 用于告诉video标签需要播放的视频地址
//autoplay: 用于告诉video标签是否需要自动播放
//controls: 用于告诉video标签在播放视频时,是否需要显示控制条
//poster: 用于告诉video标签,在没有播放时,显示一张占位图片
//loop: 一般用于广告视频,用于循环播放
//preload: 用于预加载视频,注意preload 和autoplay 属性相冲,设置了autoplay 属性preload属性就会失效
//muted: 静音
//width:
//height:
```

- 3 、格式(2):
```
<video autoplay="autoplay" controls="controls">
    <source src="../imgs/sb1.webm" type="video/webm"></source>
    <source src="../imgs/sb1.mp4" type="video/mp4"></source>
    <source src="../imgs/sb1.ogg" type="video/ogg"></source>
</video>
```
**说明:为什么会有这种格式呢?** 
(1)由于视频数据非常的重要,所以5大浏览器厂商都不愿意支持别人的视频格式,所以导致了没有一种视频格式是所有浏览器支持的.这时,w3c为了解决这个问题,所以推出了第二种video标签的格式. 
(2)第二种格式存在的意义的, 就是为了解决浏览器的适配问题. 
(3)video标签支持3种格式(.MP3, ogg, webm),我们可以把这3种格式都通过source标签指定给video标签,那么,以后当浏览器播放视频时,它就会从这三中中选一种自己的格式

- 4 注意点:
虽然通过第二种格式,能指定所有浏览器都支持的视频格式,但是所有浏览器都能通过video标签来播放视频还是有一个前提条件的,就是浏览器必须支持 html5标签,否则同样无法播放.在过去的一些浏览器是不支持html5标签的,所以为了让过去的一些浏览器也能通过video 标签来播放视频,那么我们以后可以通过一个 JS 框架叫做 html5media来实现.


***
<br>
####二、audio 标签

- 格式(1)
```
<audio src=""></audio>
```

- 格式(2)
```
<audio>
    <source src="../imgs/abc.mp3" type="audio/mp3"> </source>
    <source src="../imgs/abc.mp3" type="audio/mp3"> </source>
    <source src="../imgs/abc.mp3" type="audio/mp3"> </source>
</audio>
```
- 注意点:<br>
audio 标签的使用和video标签的使用基本一样,video标签中能够使用的在audio标签中大部分也能使用,并且功能都一样,<br>
只不过有3个属性不能使用 height width poster










