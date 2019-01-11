#### 定位流  绝对定位


1、在我们实际的开发中,相对定位用来微调元素在标准流中的应用场景并不多, 相对定位的主要应用场景是配合绝对定位来使用.


2、 什么是绝对定位?
给元素添加 `position:absolute;`属性后, 元素就是绝对定位元素了,(绝对定位是相对于body 定位)
![](/assets/absolute.png)

3、 绝对定位会脱离标准流(和元素的浮动很像), 以前我们学过,元素的浮动时会脱离标准流而且浮动的元素是不区分行内元素/ 行内块级元素/ 块级元素的. 其实我们的绝对定位也是不区分行内元素/ 行内块级元素/ 块级元素的. 经过测试验证, 脱离标准流的元素(浮动后的元素/ 绝对定位的元素) 都是可以设置元素的宽度和高度

4、绝对定位元素的定位.
(1)、绝对定位的元素会像浮动元素一样,脱离标准流
(2)、绝对定位的元素可以设置 top/ right/ bottom/ left/ width/ height 的, 默认情况下, 给绝对定位的元素设置top/ right/ bottom/ left 属性是相对于body 来计算的.

代码如下:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>


    <style>




     .box1{
         background-color: red;
         width: 100px;
         height: 100px;

      }
      .box2{

          background-color: green;
          width: 80px;
          height: 80px;
          position: absolute;
          right: 0px;
        }
      .box3{
          background-color: blue;
          width: 120px;
          height: 120px;
        }


    </style>
</head>
<body>

 <div class="box1"></div>
 <div class="box2"></div>
 <div class="box3"></div>

</body>
</html>
```
![](/assets/abs.png)
