#### 透视属性

1、什么是透视属性

透视属性就是`近大 远小`

**注意** 
(1)、距离越远透视效果越弱, 越近,效果越明显
(2)、透视效果必须添加在需要显示透视效果的父元素上(祖先元素也可以,建议在父元素上)

![](/assets/ts.png)

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


            div{
                width: 200px;
                height: 200px;
                border: 1px solid #000;
                margin: 0 auto;
                margin-top: 50px;
                // 这个就是透视属性, 指的是 你距离多远去看
                perspective: 1500px ;
            }

            img{
                width: 200px;
                height: 200px;
                transform-origin: bottom;
                transition: transform 1s;

            }
            div:hover img{
                transform: rotateX(70deg);
            }
 
    </style>
</head>
<body>

    <div><img src="images/meat.jpg" alt=""></div>
 

</body>
</html>
```
![](/assets/tsxg.png)

