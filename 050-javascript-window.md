#### javaScript Window



<br>
**javaScript Window ---- 浏览器对象模型**


**浏览器对象模型(BOM Browser Object Model), 使得javaScript 有能力与浏览器对话**


<br>
#### 一、浏览器对象模型(BOM Browser Object Model)

由于现代浏览器已近(几乎) 实现了javaScript 交互性方面的相同的方法和属性, 因此常被称为是 **BOM的方法和属性**




<br>
#### 二、 Window 对象

**1、所有的浏览器都支持Window对象, 它代表的是浏览器窗口**
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

1> 对于 Internet Explorer/ Chrome/ firefox/ Opera及Safari 直接使用 **window.innerHeight 和 window.innerWidht** 即可获取窗口的高度和宽度.

2> 对于 Internet Explorer 8/7/6/5 使用 ** document.documentElement.clientHeight 和 document.documentElement.clientWidth ** 获取高度和宽度.
3> Internet Explorer 也可以使用 **document.body.clientHeight 和 document.body.width** 来获取高度宽度




获取浏览器宽高通用方案
```
<script>
        
        function displayWindowSize() {
            var height = window.innerHeight
                    || document.documentElement.clientHeight
                    || document.body.clientHeight;
            
            var width = window.innerWidth
                    || document.documentElement.clientWidth
                    || document.body.clientWidth;
            
            var winSize = "width:" + width + "height:" + height;
            
            alert(winSize);
        }
        
</script>


// 注意, 该示例显示的浏览器窗口高度和宽度, 不包括工具栏和滚动条
```





