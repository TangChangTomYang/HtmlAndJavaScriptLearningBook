#### javaScript HTML DOM 改变 CSS

HTML DOM 允许 javaScript 改变 HTML 元素的样式(style)


<br>
#### 一、 改变HTML 样式 (Style)


```
需要改变 HTML 的样式, 请使用这个语法:

document.getElementById(id).style.property = new value;
```

示例: 修改元素的高和颜色
```
<script>
    function changeColor(){
        var element =  document.getElementById("div");
        element.style.backgroundColor = "red";
        element.style.height = "120px";
    }
</script>


<div id="div" style="width:120px; height: 20px; background-color: orange;"></div>
<button type="button" onclick="changeColor()">点击修改颜色</button>
```