#### 大小盒子居中问题


要求: 
1、 在一个大盒子(500*500) 中放一个小盒子(200*200) , 要求 小盒子在大盒子正中间

![](/assets/boxInbox.png)



解决方案: 

(方案一): <br> 增加大盒子的Padding-top padding-left, 将小盒子挤到中间. 这个方案有缺陷(虽然小盒子可以被放到指定的位置, 但是默认情况下增加盒子的border 和 padding 会导致盒子原来 尺寸变大 )
 
因此, 如采用此方案, 在给大盒子增加了padding-top 和 padding-left 后, 必须在width 和 height 上减去对应的宽度 或者设置大盒子的 box-sizing : border-box;


```
解决方案1-1:
.big{
    width: 350px;
    height: 350px;
    background: red;

    padding-top: 150px;
    padding-left: 150px;
}

.small{
    width: 200px;
    height: 200px;
    background: blue;
}


解决方案1-2:
 .big{
    width: 500px;
    height: 500px;
    background: red;

    padding-top: 150px;
    padding-left: 150px;
    box-sizing: border-box;
}

.small{
    width: 200px;
    height: 200px;
    background: blue;
}

```


解决方案(二)
1. 给小盒子增加外边距 margin-left 和 margin-top
带来的问题, 虽然这个方案 margin-left 能让小盒子水平居中, 但是 margin-top 不能让小盒子垂直居中, 而且还会把大盒子顶下来.

 ![](/assets/margin-top.png)
**注意点: **
(1)、如果2个盒子是嵌套关系,如果给里面的盒子设置了 margin-top 后, 那么外边的盒子也会被顶下来.
(2)、如果外面的盒子不想被里面的盒子顶下来, 需要给外面的盒子设置border 属性

(3)、在企业开发中,一般情况下如果需要控制嵌套关系(盒子之间的距离), 应该首先想到 padding, 其次才考虑margin. 因为padding的本质是用来处理内部关系(父子关系)的, 而margin 是用来处理兄弟关系之间的距离的. 这一点需要牢记
![](/assets/margin-center.png)


##### 关于margin的注意点

margin 分开写
```
margin-top:
margin-right:
margin-bottom:
margin-left:
```
margin 连写
```
margin: top right bottom left;
```
在处理父子关系时, 可以用 `margin : 0 auto;` 来让 子空间在父控件中水平居中, 不能写: `margin: auto auto`.

![](/assets/Snip20181212_12.png)





