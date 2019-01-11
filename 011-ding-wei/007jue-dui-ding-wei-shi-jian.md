#### 绝对定位 实践

绝对定位在实际应用中主要是用到 子绝父相


```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>




    <style>

        *{
            margin: 0;
            padding: 0;
        }
        
        /*最外面的大盒子*/
        .box1{
            width: 300px;
            height: 300px;
            margin: 0 auto;
            overflow: hidden;
            border: 1px solid #000; 
        }

        /*大盒子里面装图片发的小盒子*/
        .picBox{
            width: 300px;;
            height: 250px;
            overflow: hidden;
            position: relative;
        }
        
        /*热标签*/
        .picBox img:nth-of-type(2){
             position: absolute;
             top: 0px;
             left: 0px;
         }

        /*价格标签*/
        .picBox img:nth-of-type(3){
            position: absolute;
            left: 0px;
            bottom: 0px;
        }

    </style>
</head>
<body>


<div class="box1">

    <div class="picBox">
        <img src="images/meat.jpg" alt="">
        <img src="images/hot.png" alt="" class="hot">
        <img src="images/money.png" alt="" class="price">
    </div>

    <div class="txt">adsfasdfadsfadsfasdfadsfasd</div>
</div>

</body>
</html>
```

![](/assets/zjfxsj.png)
