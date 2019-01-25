#### 一、z-index 属性

1、什么是z-index 属性

默认情况下,所有的元素都有一个默认的`z-index`属性, 取值为0.

z-index 属性的作用是专门用于控制定位流元素的覆盖关系的.


2、默认情况下定位流中的元素会覆盖标准流中的元素.

3、默认情况下定位流的元素, 后面的定位流元素会盖上前面的定位流元素, 因此在处理像有导航条这种固定定位的元素,不希望被其它元素覆盖, 就需要使用z-index 来调整层的关系.

4、如果定位流元素设置了 z-index 属性, 那么谁的z-index 值大, 那么谁就在最上面, 如果相同,那么后面的就会盖住前面的.

  
**注意:**
在固定定位中是不能使用 z-index, 失效





<br>

#### 二、float / position z-index 层级关系

**1、在标准流中,默认所有的 标签/元素 z-index 值为 0, 且后面的标签 覆盖 前面的标签的子标签(如果上一个标签的子标签有超出父标签, 且子标签 为标准流 (非 float/ 非定位流(position:relative/  position:absolute)))**
```
.box1{
    width: 150px;
    height: 50px;
    background-color: pink;  
}
.box1-son{
    width: 50px;
    height: 75px;
    background-color: blue;
} 
.box2{
    width: 250px;
    height: 125px;
    background-color: cyan;
}


<div class="box1">
     <div class="box1-son"></div>
</div>
<div class="box2"></div>
```

![](/assets/Snip20190125_1.png)







**2、 在标准流中, 如果上一个标签/元素 的子元素是float 或者 定位流(position:relative; position:absolute;), 那么如果子标签超出父标签, 那么父标签后面的标签会被子标签覆盖**


```
<style>

        .box1{
            width: 150px;
            height: 50px;
            background-color: pink;
        }
        .box1-son{
            width: 50px;
            height: 75px;
            background-color: blue;
            float: left; /*或者 position: relative; 或者 position: absolute;*/
        }
        .box2{
            width: 250px;
            height: 125px;
            background-color: cyan;
        }

</style>
    
    
 <div class="box1">
     <div class="box1-son"></div>
 </div>
 <div class="box2"></div>
```
![](/assets/Snip20190125_4.png)



3、 

```
 .box1{
        width: 150px;
        height: 50px;
        background-color: pink;
}
.box1-son{
    width: 50px;
    height: 75px;
    background-color: blue;
    position: relative;  /*此处必须为 定位流才能 盖住后面的 box2*/
    z-index: 1;
}
.box2{
    width: 250px;
    height: 125px;
    background-color: cyan;
    position: relative;
    
}
        
 <div class="box1">
 <div class="box1-son"></div>
 </div>
 <div class="box2"></div>
```

![](/assets/Snip20190125_5.png)



#### z-index 结论

 ⭐️⭐️⭐️⭐️⭐️**1> 同一个容器中的 所有的 标准流中的标签/ 元素在同一层级.
2> 同一个容器中的 所有的 浮动流(float:left)中的标签/ 元素在同一层级
3> 同一个容器中的 所有的 定位流(position:relative; positon:absolute)中的标签/ 元素在同一层级
4> z-index 使用来处理同一层级中的元素的层级关系的, z-index 大的在上面
5> 同一容器中, 定位刘的元素层级  > 浮动流元素层级 > 标准流层级. **


