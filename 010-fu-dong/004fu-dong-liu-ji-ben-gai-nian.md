#### 浮动流基本概念


1、 什么是网页的布局方式?
网页的布局方式其实就是指浏览器是如何对网页中的元素进行排版


2、标准流(文档流/ 普通流)排版方式
(1)、其实浏览器默认的排版方式就是标准流的排版方式
(2)、在CSS 中将元素分为3类, 分别是块级元素/ 行内元素 / 行内块级元素
(3)、在标准流中有2中排版方式, 一种是垂直排版. 一种是水平排版.

**垂直排版:** 如果元素是块级元素, 那么就会垂直排版

**水平排版: ** 如果元素是行内元素/ 行内块级元素, 那么就水平排版


3、浮动流排版方式
(1)、浮动流是一种`半脱离标准流` 的排版方式
(2)、浮动流只有一种排版方式, 就是水平排版, 它只能设置某个元素左对齐或者右对齐

**注意点**
(1)、浮动流中没有居中对齐, 也就是说没有center这个取值
(2)、浮动流中是不可以使用`margin : 0 auto ;` 来居中的

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>


    <style>

         .box{
             width: 100px;
             height: 100px;
             background: blue;
             display: inline-block;
             float: left;
         }

        .box2{
            width: 100px;
            height: 100px;
            background: red;
            display: inline-block;
            float: right;
        }


    </style>
</head>
<body>

    <!--整体内容-->
    <div class="box" >  </div>
    <div class="box2" >  </div>
</body>
</html>
```
![](/assets/float.png)


**浮动流的特点**
(1)、在浮动流是不区分 `块级元素/ 行内元素/ 行内块级元素`的(都支持左右浮动) 都可以水平排版.
(2)、 在浮动流中无论是 `块级元素/ 行内元素/ 行内块级元素` 都可以设置宽高
(3)、浮动流中的元素和标准流中的 行内块级元素很想




4、定位流排版方式
