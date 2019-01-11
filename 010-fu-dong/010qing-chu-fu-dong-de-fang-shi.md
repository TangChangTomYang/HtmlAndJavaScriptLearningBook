#### 为什么要清除浮动 

清除浮动的场景,如下图:
![](/assets/clearFloat.png)
在标准流的情况下, 红色的盒子和蓝色的盒子, 没有设置高度和宽度, 红色的盒子被里面的内容(黄色)撑起来了, 蓝色的盒子被里面的内容(天蓝色)撑起来了, 具体代码如下:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>


    <style>

        *{
            margin: 0px;
            padding: 0px;
        }

        .divOne{
            background: red;
        }

        .divOne p{
            width: 100px;
            background-color: yellow;
        }

        .divTwo{
            background-color: blue;
        }

        .divTwo p{
            width: 100px;
            widows: 100px;
            background-color: cyan;
        }


    </style>
</head>
<body>

    <div class="divOne">
        <p>段子一</p>
        <p>段子一</p>
        <p>段子一</p>
    </div>
    <div class="divTwo">
        <p>段子二</p>
        <p>段子二</p>
        <p>段子二</p>
    </div>

     
</body>
</html>
```
当红色盒子和蓝色盒子里面的内容浮动后, 就出现问题了, 如下图:
![](/assets/allfloat.png)
本来分属于不同盒子的内容(黄色内容,天蓝色内容) 因为父元素没有设置高度,全部浮动排在一起, 这不是我们想要的结果


其实一句话概括为什么要清除浮动
就是,不然后面盒子中浮动的子元素去找前一个盒子中浮动的元素, 让盒子中的浮动的子元素,只在当前盒子中找浮动的元素

#### 清除浮动的方式(一)

1、 给前面一个父元素设置高度

![](/assets/clearFloat2.png)


**注意点:**
在企业开发中, 我们能不写高度就不写高度,所以这种方式写的很少









#### 清除浮动的方式(二)

给不想浮动的子元素去找上一个父元素的父元素标签增加 clear 属性
```
.box{
    clear:both;
}
```
![](/assets/floatxg.png)


- clear 属性的主要取值

```
clear:left;  // 让浮动的子元素不去找上一个父元素中左浮动的元素
clear:right; // 让浮动的子元素不去找上一个父元素中右浮动的元素
clear:both;  // 让浮动的子元素不去找上一个父元素中左右浮动的元素

clear:none;  // 默认就是这个
```


其实可以将添加 clear 属性理解为, 在当前父元素的上方强制加一根分割线, 这样子元素就上去找不到了, 做了给测试如下:

在 box1 , box2, 后增加了个box3,为了让box3强制显示在box2的子元素后,就需要给box3设置clear属性
```
clear:both;
```
![](/assets/clearxg.png)
<br>
![](/assets/clearxg2.png)


**注意点:**
给元素添加clear 属性后, 标签原来的margin 属性就会失效, 正式因为这一点, 后面就由了我们的清除浮动的第三种方式.



#### 清除浮动方式(三)

1、外墙法
就是在两个盒子之间设置一个 块级元素, 并设置clear属性为both 即可

 

**注意点:**

(1)、使用了外墙法后, 外墙法可以让第二个盒子使用 `margin-top` 属性,不能让第一个盒子使用 `margin-bottom` 属性, 会出问题margin 显示时的错误问题.
(2)、在使用了外墙法后, 如果想让上一个盒子和下一个盒子之间有个 类似margin 的间隔效果, 通常的做法是, 直接给这个墙添加一个高度来实现.


![](/assets/wqsx.png)
```
<div class="divOne">
<p>段子一</p>
<p>段子一</p>
<p>段子一</p>
</div>
// 需要给wall 这个div 设置clear 属性为both
<div class="wall"></div>
<div class="divTwo">
<p>段子二</p>
<p>段子二</p>
<p>段子二</p>
</div>
```
  


3、内墙法
什么是内墙法?

内墙法就是在第一个盒子的所有元素后天添加一个盒子, 并给这个盒子设置 clear 属性为 both

**内墙法相比外墙法的优势**
(1)、使用内墙法后, 第一个盒子可以正常的使用 margin-bottom 属性, 第二个盒子可以使用margin-top 属性, 内墙也可以设置高度.

**外墙法和内墙法的区别:**
(1)、外墙法不能撑起第一个盒子的高度, 内墙法可以撑起第一个盒子的高度




因为外墙法和内墙法都是需在再额外的添加一个盒子并设置clear 属性为both, 因此在实际的开发中我们外墙法和内墙法用的不多. 而且我们在前端中推崇的是结构和样式分离, 而不管使用外墙法还是内墙法, 结构和样式都是交叉在一起的,因此代码阅读性不好,不推崇.



