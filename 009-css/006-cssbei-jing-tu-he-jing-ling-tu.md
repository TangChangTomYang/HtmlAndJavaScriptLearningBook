#### 精灵图

1. 一个网页中往往会应用很多的背景图像作为装饰, 当网页中的图像过多时, 服务器就会频繁的接受和发送请求, 这将大大的降低页面的加载速度. 为了有效的减少服务器接受和发送请求的次数,提高页面的加载速度, 就出现了CSS精灵图

2. 简单的说, CSS精灵图就是一种处理网页背景图的方式. 他将一个网页中涉及到的背景图像都集中在一张大图中, 然后将大图应用于网页中, 这样当用户访问该页面时, 只需要向服务器发送一次请求图像即可全部展示出来.

在CSS中使用精灵图,需要用到几个CSS属性
1>  background-image: url("xxx.png");
2>  background-position : 20xp 30px;
3>  background-repeat : no-repeat;
