#### 盒子阴影和文字阴影


1、如何设置盒子阴影

```
box-shadow: 水平偏移 垂直偏移  模糊度 阴影扩展 阴影颜色 内外阴影; // 后面3个参数可以省略


box-shadow: 10px 10px 10px 10px blue inset;  
```

**注意点:**
(1)、盒子的阴影分为内外阴影, 默认情况下就是外阴影
(2)、默认情况下, 盒子的阴影就是盒子内容的颜色

快速设置盒子yinying
```
box-shadow: 10px 10px 20px
```

![](/assets/bsd.png)


2、文字阴影

```
text-shadow: 水平偏移 垂直偏移 模糊度 阴影颜色; //颜色可以省略
```

![](/assets/tsd.png)
