#### 2D 转换

![](/assets/Snip20181221_5.png)

代码如下:

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
                width: 300px;
                height: 300px;
                border: 1px solid #000;
                margin: 0 auto;
                margin-top: 50px;
                list-style: none;
            }

            li{
                width: 50px;
                height: 30px;
                background-color: red;
                margin: 0 auto;
                margin-top: 20px;
                line-height: 30px;
                text-align: center;
            }

            /*旋转*/
            li:nth-of-type(2){
                transform: rotate(45deg);
            }

            /*平移*/
            li:nth-of-type(3){
                /*!*transform: translate(20px ,30px);*! */
            }

            /*缩放*/
            li:nth-of-type(4){
                transform: scale(1.5,2);
                /*如果x方向和y方向的缩放比例是一样的就可以传一个值*/
                /*transform: scale(1.5);*/
            }

            /*综合*/
            li:nth-of-type(5){
                /*如果要同时执行多个转换, 转换之间使用空格隔开即可*/
                transform: rotate(30deg) translate(10px, 20px) scale(1.5);
            }

    </style>
</head>
<body>

<ul>
    <li>正常</li>
    <li>旋转</li>
    <li>平移</li>
    <li>缩放</li>
    <li>综合</li>
</ul>

</body>
</html>
```
