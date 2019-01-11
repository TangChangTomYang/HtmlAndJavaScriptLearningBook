#### 绝对定位 水平居中



绝对定位水平居中的步骤
(1)、 设置父元素 为相对定位(`position:relative;`) 不脱标.
(2)、 设置子元素为绝对定位(`position:absolute;`)脱标, 脱标后相对于父元素绝对定位.
(3)、 设置子元素 `top;50%` 这样, 子元素距离父元素左边的距离刚好是父元素的一半.
(4)、 设置子元素的 `margin-left: - 子元素宽度一半` 这样, 子元素就微调到父元素的水平中间了, 代码如下


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
         /*相对定位不脱标,称为子元素的绝对定位参看点*/
          position: relative;

          }
     .box2{
         width: 100px;
         height: 100px;
         background: green;
         /*相对于父元素绝对定位*/
         position: absolute;
         /*水平居中*/
         left: 50%;
         margin-left: -50px;
         /*垂直居中*/
         top:50%;
         margin-top: -50px;
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
![](/assets/spczjz.png)
