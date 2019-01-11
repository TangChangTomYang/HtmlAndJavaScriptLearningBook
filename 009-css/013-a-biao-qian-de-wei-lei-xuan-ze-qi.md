#### a 标签的伪类选择器 


![](/assets/abq.png)
1、通过我们的观察, 我们发现 `a` 标签存在一定的状态
(1)、 默认状态从未访问过的状态
(2)、 被访问过的状态
(3)、 鼠标长按的状态


2、 什么是 `a` 标签的伪类选择器?
a 标签的伪类选择器,就是专门用来修改a 标签不同状态的样式的


```
   /*注意,以下3个属性,如果不生效可能是因为缓存的问题, 清除缓存即可解决*/
    /*修改未被访问过时的状态样式*/
   a:link{
       color: red;
   }

   /*修改已经被访问过的状态的样式*/
    a:visited{
        color: green;
    }
    
    /*鼠标悬停时的样式 */
    a:hover{
        color: blue;
    }

    /*修改被按下状态时的状态样式*/
    a:active{
        color: orange;
    }
```

3、 a标签伪类选择器的注意点

(1)、 a标签的伪类选择器可以单独出现,也可以一起出现
(2)、 a标签的伪类选择器如果一起出现,那么有严格的顺序要求, 编写的顺序必须是`link/ visited/ hover/ active` 即 lvha, love hate
(3)、 如果在实际开发中`未访问 和 已经访问`状态是一样的颜色, 那么可以简写,如下:
```
 a:link{
       color: green;
   }

  a:visited{
        color: green;
  }
  a:hover{
        color: blue;
  }

  a:active{
        color: orange;
  }

等价于
a{
    color: green;
}
 
a:hover{
    color: blue;
}

a:active{
    color: orange;
}
```

