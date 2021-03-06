#### 绝对定位注意点

1、 如果一个绝对定位的元素是相对于body 作为参考点, 那么其实这个参考点的宽度是以网页的首屏的宽度和高度作为参考点, 而不是以网页可滚动的真实宽度高度为参考点.


如下图:
![](/assets/realtive_body.png)
这种效果就很怪, 我明明是参考body 绝对定位, 网页的尺寸发生变化时,就带来了不想要的效果了,这也是我们在使用绝对定位时相对于body 带来的一个弊端.

2、绝对定位相对于参考点的定位是,参考祖先元素的boder 以内, 也就是说, 如果一个子元素相对于一个父元素绝对定位,那么他的相对位置是相对于父元素的border

```
 .box1{
     width: 300px;
     height: 300px;
     background-color: red;
     border: 5px solid #000;
     padding: 20px;
     position: relative;


  }
  .box2{
      width: 100px;
      height: 100px;
      background: green;
      border: 2px solid yellow;
      position: absolute;
      bottom: 0px;
      right: 0px;
    }
```
![](/assets/rg.png)





<br>
**注意:**
如果一个标签 使用了绝对定位,先设置了left位置再设置right位置, 或者先设置了top位置再设置bottom位置, 那么后面设置的 right位置 和 bottom位置将不会生效, 这是因为 left/ top 的优先级比 right/ bottom 的优先级高.

示例:

```


div{
    position: relative;
}

a{
    position: absolute;
    left: 0px;
    top:0px;
}

div a{
    right: 0px; /*此处无效, 已经先设置了 left, left 权限高于right*/
    bottom:0px; /*此处无效, 已经先设置了 top, top 权限高于bottom*/
}
        
        

<div class="box">
    <a href="@">a 标签 </a>
</div>

```
