#### 手风琴过渡效果
![](/assets/sfqgu1.png)
<br>
![](/assets/sfqgd2.png)


实现代码如下:

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
                width: 585px;
                height: 150px;
                background-color: red;
                margin: 0 auto ;
                margin-top: 50px;
                list-style: none;

                /*超出ul的部分全部裁剪掉*/
                overflow: hidden;

            }

            li{
                width: 50px;
                float: left;
                box-sizing: border-box;
                transition: all 1s;
            }

            img{
                height: 150px;
            }
            
            /*当hover到父元素时, 将所有的li的宽度设置为最窄*/
            ul:hover li{
                width: 50px;
            }
            /*当hover到父元素里面的具体元素时, 将子元素的宽度设置为最宽*/
            ul li:hover{
                width: 335px;
            }
    </style>
</head>
<body>
<ul>
    <li><img src="images/ad1.jpg" alt=""></li>
    <li><img src="images/ad2.jpg" alt=""></li>
    <li><img src="images/ad3.jpg" alt=""></li>
    <li><img src="images/ad4.jpg" alt=""></li>
    <li><img src="images/ad5.jpg" alt=""></li>
    <li><img src="images/ad6.jpg" alt=""></li>
</ul>
</body>
</html>
```


**重点:**
(1)ul:hover li
(2)ul li:hover
