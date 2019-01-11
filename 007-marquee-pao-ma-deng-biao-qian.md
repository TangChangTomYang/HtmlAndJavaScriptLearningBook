#### 007-marquee 跑马灯标签


<br>
##marguee 标签


- 什么是marquee 标签?
做跑马灯效果
![](/assets/Snip20180816_6.png)

- 格式:
```
<marquee>
    //添加需要跑马灯效果的内容即可
    //跑马灯的内容 可以自己定义
</marquee>
```

示例:
```
//direction 属性用来设置滚动的方向

<marquee direction="left">跑马灯内容</marquee>
<marquee direction="right">跑马灯内容</marquee>
<marquee direction="up">跑马灯内容</marquee>
<marquee direction="down">跑马灯内容</marquee>

//scrollamount 属性用来设置跑马灯的速度,值越大速度越快
<marquee scrollamount="1" direction="down">跑马灯内容</marquee>
<marquee scrollamount="100" direction="down">跑马灯内容</marquee>

// loop 属性用于设置循环的次数
<marquee loop="1" direction="down">跑马灯内容
</marquee>

//behavior 属性用于设置滚动的类型, 有2个值,slide(滚到边界就停) 和 alternate (来回反弹)
<marquee behavior="slide">跑马灯内容
</marquee>
<marquee behavior="alternate">跑马灯内容
</marquee>

```
- 注意点:
marquee 标签不是W3C 推荐的标签,在W3C官方文档中也是无法查询到这个标签的,但是各大浏览器厂商对这个标签支持的都是非常好.
