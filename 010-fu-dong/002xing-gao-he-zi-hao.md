#### 行高和字号


1、 什么是行高? 

在CSS中所有的行都有自己的行高


注意点: 
很容易将盒子的高度和行高混淆

行高和盒子的高是不同的


2、设置行高
```
ling-height: 82px
```

3、规律
(1)、文字在行高中默认是垂直居中的
(2)、在企业开发中,我们经常将盒子的高和行高一样, 那么一行文字就在盒子的中间 (因为一行文字总是在行高的中间)
![](/assets/lineHeight.png)
(3)、 如果没有单独设置行高, 那么文字的行高就是比文字的高度高一点点.
(4)、默认情况下盒子的高度会被行高撑起来(没有设置盒子的高 height)

![](/assets/boxlineHeight.png)
(5)如果想让一行文字正好在盒子的中间, 那么可以设置文字的行高为盒子的高度
(6)如果有多行文字, 想要让文字显示在盒子的中间, 那么就需要同时设置行高和padding-top 来调整了.
