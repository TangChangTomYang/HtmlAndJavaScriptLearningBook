#### 2D转换   形变中心点

1、形变中心点 `transform-origin`  默认是元素的中心点


```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
            *{
                margin:0;
                padding: 0px;
            }

            ul{
                width:  150px;
                height: 150px;
                border: 1px solid #000;
                margin: 0 auto;
                margin-top: 50px;
                list-style: none;
                position: relative;
            }

            li{
                width:  150px;
                height: 150px;
                position: absolute;
                left: 0px;
                top: 0px;
            }

            li:nth-child(1){
                background-color: red;
                transform: rotate(30deg);
            }

            li:nth-child(2){
                background-color: green;
                transform: rotate(50deg);
            }

            li:nth-child(3){
                background-color: blue;
                transform: rotate(60deg);
            }
    </style>
</head>
<body>
<ul>
    <li></li>
    <li></li>
    <li></li>
</ul>
</body>
</html>
```

![](/assets/to.png)

2、修改形变中心点
```
li{
    // 第一个参数表示水平方向
    // 第二个参数表示竖直方向
    transform-origin: 10px 20px;
    
}
```
形变中心点其实有3中书写方式
(1)、像素的写法 `10px 20px`
(2)、百分比 `30% 50%`
(3)、方位 `left  right top bottom center`
![](/assets/toi.png)
