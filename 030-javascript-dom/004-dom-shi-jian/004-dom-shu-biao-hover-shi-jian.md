

#### DOM 鼠标 Hover 在标签事件

onmouseover 和 onmouseout 事件可用于在用户的鼠标 移动至 HTML标签上 或 移除标签时触发


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
