#### 绝对定位---子绝父相

自绝父相定位的原理
1、相对定位的元素`position:relative;` 不会影响自己再标准流中的位置.
2、绝对定位的元素`position:absolute;` 会脱离标准流, 且绝对定位的元素会将离自己最近的有设置过定位流(相对定位/ 绝对定位/ 固定定位)的祖先元素作为参考点.
3、定位流中的元素(相对定位/ 绝对定位/ 固定定位) 都可以设置 top/ right/ bottom/ left/ width/ height 属性


```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title> 

    <style> 
     .box1{
              width: 300px;
              height: 300px;
              background-color: red;
              border: 5px solid #000;
              /*padding: 20px;*/
              position: relative;
              text-align: center;
         line-height: 300px; 
          }
     .box2{
         width: 100px;
         height: 100px;
         background: green;
         /*border: 2px solid yellow;*/
         position: absolute;
         top:0px;
         left: 100px;
     } 
    </style>
</head>
<body>

 <div class="box1">
     我是div
     <div class="box2"></div>
 </div> 
</body>
</html>
```


**为什么要采用子绝父相, 相对于body 绝对定位不行吗?**


(1)、 其实默认情况下绝对定位都是相对于 body 来定位的. 但是相对body 定位有个弊端, 就是相对于body 绝对定位后, 上下左右 都参考的是,网页首屏的宽度高度, 而当用户把网页的尺寸调整时就会出现参考错误.

(2)、子绝父相的优势在于, 相对定位父元素不脱标, 父元素尺寸相对固定, 给子元素参考时带来一个固定的值, 这样网页变化尺寸时, 父子相对位置就不会变化.



