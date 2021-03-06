#### 定位流分类

####一、定位的分类
1、相对定位
2、绝对定位
3、固定定位
4、静态定位



####1、 什么是相对定位
(1)、相对定位, 就是相对于自己以前在标准流中的位置

(2)、如何让标签元素相对定位, 给标签添加 `position:relative;`属性, 后就可以给标签设置相对属性的具体值了

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>


    <style>

      div{
          width: 100px;
          height: 100px;
      }

        .box1{
            background-color: red;
        }
      .box2{
            background-color: green;
          /*设置box2为相对定位(让box2 使用相对定位)*/
          position: relative;
          /*设置box2 的相对位置(相对于原来自己再标准流中的位置)*/
          top: 20px;
          left: 20px;

        }
      .box3{
            background-color: blue;
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
![](/assets/relative.png)

(3)、 相对定位是不会脱离标准流的, 在标准流中还是会占用一分空间

(4)、 相对定位一共有4个取值, top/ right/ bottom/ left.

**记住一点就好:**
相对定位,就是相对于原来自己再标准流中的定位. 上下左右偏移


**注意点**
相对定位一共有4个取值, 上下左右, 但是, 上和下是相同的取值, 左和右是相同的取值, 因此在使用的过程中, 设置了上就不要设置下, 设置了右就不要设置左.

以下是错误的用法
```
.box{
    position:relative; // 使用相对定位
    left:20px;
    right:20px;  //错误写法, 矛盾
}
```

(5)、由于相对定位是不脱离标准流的, 因此相对定位是要区分 行内元素/ 行内块级元素/ 块级元素的.
(6)、由于相对定位是不脱离标准流的, 因此在相对定位元素中是不能使用浮动的.
(7)、虽然相对定位要区分行内元素/ 行内块级元素/ 块级元素, 但是行内元素/ 行内块级元素/ 块级元素在使用top/ right/ bottom/ left 的效果是一样的 位置都会变化, 只是行内元素不能设置宽高而已.
(8)、给元素添加了相对定位属性后, 不影响原来元素设置margin/ padding/ border 属性, 原来的属性仍然有效.


####三、相对定位的应用场景

1、用于对元素在标准流中的位置进行微调(和margin 的作用查不多)
2、配合后面的绝对定位来使用

**说明**
虽然我们在使用margin 属性和相对定位属性后都能改变元素在标准流中的位置, 但是margin 的应用场景和相对定位的应用场景是不一样的. 当我们使用margin 来改变元素在标准流中的位置时, margin 的值一般是写死的, 很难根据环境自动变化, 但是我们如果使用相对定位的话, 就可以使用比例或者一个值来动态调整元素在标准流中的位置.







<br>
**注意:**

**行内元素/ 行内块级元素 不能直接设置定位流为 position:relative, 必须先设置 display:block 后才可以设置,position为 relative.**












