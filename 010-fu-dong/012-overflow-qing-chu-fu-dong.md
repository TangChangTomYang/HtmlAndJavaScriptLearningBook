#### overflow 清除浮动

1、`overflow:hidden; `的作用

(1)、 可以将超出标签范围内的内容裁剪掉(不显示)
```
 .box1{
   width: 200px;
   height: 200px;
   background-color: red;
  // 超出元素变宽部分不显示
   overflow: hidden;
}
```
![](/assets/overflow.png)


(2)`overflow:hidden;` 也可以用来清除浮动, 而且清除浮动后不会影响上一个盒子和下一个盒子使用margin 属性

代码如下:
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


        .box1{
            background-color: red;
            overflow: hidden;
            margin-bottom: 10px;;
            //overflow 也是由兼容性问题的, 使用下面这个属性来设置兼容性问题
            *zoom:1;
        }

        .box1 p{
            width: 100px;
            background-color: cyan;
        }

        .box2{
            background-color: yellow;
            margin-top: 20px;;
        }

        .box2 p{
            width: 100px;
            background-color: green;
        }

        p{
            float: left;
        }


    </style>
</head>
<body>


<div class="box1">
    <p>测试文字</p>
    <p>测试文字</p>
    <p>测试文字</p>
</div>

<div class="box2">
    <p>测试文字2</p>
    <p>测试文字2</p>
    <p>测试文字2</p>
</div>



</body>
</html>
```

![](/assets/overflowClearFloat.png)


(3)、`overflow:hidden;` 也可用用来 清除里面的子元素设置margin-top 后将外面的盒子顶下来,原来我们为了保证里面的盒子设置了margin-top 后不会把外面的盒子顶下来,是给外面的盒子添加border 属性, 现在我们可以通过给外面的盒子设置 `overflow:hidden;`属性来解决这个问题了.

![](/assets/Snip20181217_15.png)
