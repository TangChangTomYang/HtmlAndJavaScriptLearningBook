#### DOM onmouse 事件


<br>
#### 一、onmouseover 和 onmouseout 事件


onmouseover 和 onmouseout 事件可用于在用户的鼠标移至 HTML 元素上方或移出元素时触发函数。

```
<script>
    function changeColor(isOver) {
        var box = document.getElementById("box2");
        (isOver == true) ?  box.style.backgroundColor = "red" : box.style.backgroundColor = "blue";
    }
</script>

<div class="box" onmouseover="changeColor(true)" onmouseout="changeColor(false)" ></div>
<div id="box2"></div>
```



<br>
#### 二、onmousedown 和 onmouseup 事件
