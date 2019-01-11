####一、外边距


1、什么是外边距?

标签与标签之间的距离就是外边距

2、格式
.连写
```
margin : 上 右 下 左
margin : 10px 20px 30px 40 px
```

.非连写
```
margin-top:
margin-right:
margin-bottom:
margin-left:
```
![](/assets/span.png)


代码
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>


    <style>
        *{
            border: 0px;
            margin: 0px;
        }

        span{
            display: inline-block;
            border: 1px solid #000;

            width: 150px;
            height: 150px;

        }

        div{
            border: 1px solid #000;
            height: 100px;
        }

        .box{
            margin-top: 10px;
            margin-right: 20px;
            margin-bottom: 30px;
            margin-left: 40px;
        }
    </style>
</head>
<body>


<span class="box">我是span</span><span>我是span</span><span>我是span</span>
<div>我是div</div>
</body>
```



3、注意点:
外边距(margin) 的部分是不会显示背景色的, 而padding 内边距是会显示背景色的.




####二、外边距合并现象

外边距的合并现象也叫外边距的塌陷


1、 水平方向上的Margin (外边距是可以叠加的)
 ![](/assets/margin_shuiping_diejia.png)


2、竖直方向上 margin 合并 (坍塌) 那个大就取那个
![](/assets/margin_chuizhi_hebing.png)


注意:
在默认情况下, 在垂直方向上, 外边距(margin) 是会合并的(坍塌)谁的值大一点就听谁的.
在默认情况下, 在水平方向上, 外边距(margin) 是不会合并的, 水平方向会叠加


3、 在什么情况下回发生外边距合并
在垂直方向上有2个相邻的外边距就会发生外边距合并(坍塌)现象.




