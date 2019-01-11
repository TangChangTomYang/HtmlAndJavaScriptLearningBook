#### 伪元素选择器

1、 什么是伪元素选择器?
 
 伪元素选择器就是给指定标签的内容前面添加一个子元素或者给指定标签的内容后面添加一个子元素.
 
 ```
 <div class="box">
  测试文字
 </div>
 ```
 ![](/assets/insert.png)
 
 实现代码
 ```
  /*表示在某个标签的内容前面添加一个子元素*/
  .box::before{
      // 添加的子元素的内容
      content: "前面";
      // 添加的子元素的背景色
      background-color: cyan;
      // 添加的子元素的显示模式, 默认是inline
      display: inline-block;
      // 添加的子元素的宽度
      width: 50px;
      // 添加的子元素的高度
      height: 50px;
      // 设置的添加的子元素是否可见
      visibility: hidden; 
  }

  /*表示在某个标签内容的后面添加一个子元素*/
  .box::after{
      content: "后面";
      background-color: cyan;
      width: 50px;
      height: 50px;
      display: inline-block;
  }
```

效果
![](/assets/hover insert.png)

