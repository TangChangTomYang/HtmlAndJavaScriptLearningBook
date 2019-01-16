#### HTML DOM 给标签绑定(分配) 点击事件

我们可以通过 标签的 **onclik** 属性给标签绑定(分配) 点击事件, 当用户点击对应的标签是,执行绑定的事件

<br>
**方式1:**
直接在标签内修改属性/ 样式/ 内容
```
<p onclick="this.style.color='purple'; this.style.lineHeight='50px'">点击修改文字</p>
```


<br>
#### **方式2:**
1> 定义 javaScript 函数
2> 通过 标签的 onclik 属性,将 已经定义的 javaScript 函数绑定为标签的点击事件

```
<script>
    function changeColor(element){
        element.style.color = "red";
    }
</script>

<p onclick="changeColor(this)"> 点击修改颜色</p>
```