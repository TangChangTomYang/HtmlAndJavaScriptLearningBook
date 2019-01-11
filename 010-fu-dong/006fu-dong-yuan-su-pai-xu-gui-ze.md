#### 浮动元素排序规则

1、相同方向上的浮动元素, 先浮动的元素会显示在前面, 后浮动的元素会显示在后面

2、不同方向上的浮动元素, 左浮动会找左浮动, 右浮动会找右浮动

3、浮动元素浮动之后的位置, 由浮动元素浮动前在标准流中的位置来确定

![](/assets/float_guize.png)


```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>


    <style>


         .box{
             width: 50px;
             height: 50px;
             background: red;
             float: left;
         }

        .box2{
            width: 100px;
            height: 100px;
            background: orange;
            float: left;
        }

         .box3{
             width: 80px;
             height: 80px;
             background: yellow;
             float: right;

         }
         .box4{
             width: 180px;
             height: 180px;
             background: green;
             float: right;
         }
 

    </style>
</head>
<body>
 
    <div class="box" >  1</div>
    <div class="box2" > 2 </div> 
    <div class="box3" >3 </div>
    <div class="box4" > 4</div>
 
</body>
</html>
```
