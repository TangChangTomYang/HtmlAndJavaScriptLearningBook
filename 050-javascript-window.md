#### javaScript Window



<br>
**javaScript Window ---- 浏览器对象模型**


**浏览器对象模型(BOM Browser Object Model), 使得javaScript 有能力与浏览器对话**


<br>
#### 一、浏览器对象模型(BOM Browser Object Model)

由于现代浏览器已近(几乎) 实现了javaScript 交互性方面的相同的方法和属性, 因此常被称为是 **BOM的方法和属性**




<br>
#### 二、 Window 对象

**1、 所有的浏览器都支持Window对象, 它代表的是浏览器窗口**
**2、所有的javaScript 全局对象/ 函数/ 以及变量均自动成为 Window 对象的成员**

1> 全局变量是 Window 对象的属性
2> 全局函数是 Window对象的方法
3> 甚至HTML DOM的 document 也是Window 对象的属性之一

比如:
```
window.document.getElementById("box");
等价于
document.getElementById("box");
```




<br>
<br>
#### 三、 Window (对象) 尺寸


1、浏览器窗口的尺寸是指浏览器的视口, 不包括工具条和滚动条
2、获取浏览器尺寸的方式有3种








