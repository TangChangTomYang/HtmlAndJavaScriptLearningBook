#### 浮动元素字围效果

其实, 元素浮动的一个主要场景就是字围效果(用来做图文混排)

图文混排

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>


    <style>

    .content{
        width: 300px;
        height: 300px;

        background: orange;
    }

        img{
            float: left;
            width: 150px;
            height: 150px;
        }

        .txt{
            width: 300px;
            height: 300px;

            border: 1px solid #000;
        }


    </style>
</head>
<body>


    <div class="content">
        <img src="images/a.png" alt="" class="pic">
        <div class="txt"> 2019年是新中国成立70周年，是决胜全面建成小康社会第一个百年奋斗目标的关键之年。

            　　围绕关键之年的经济工作，会议强调，坚持稳中求进工作总基调，坚持新发展理念，坚持推进高质量发展，坚持以供给侧结构性改革为主线，坚持深化市场化改革、扩大高水平开放，并要求进一步稳就业、稳金融、稳外贸、稳外资、稳投资、稳预期。

            　　中国国际经济交流中心学术委员会委员王  </div>
    </div>

</body>
</html>
```

![](/assets/picTxt.png)
