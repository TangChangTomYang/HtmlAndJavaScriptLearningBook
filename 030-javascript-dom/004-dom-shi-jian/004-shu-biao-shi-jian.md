#### DOM 鼠标 事件


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
首先当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件

```
<script>

    function touchDown() {
        document.getElementById("test").innerHTML = "鼠标按下";
    }

    function touchUp() {
        document.getElementById("test").innerHTML = "鼠标抬起";
    }

</script>

<div class="touch"
         onmousedown="touchDown()"
         onmouseup="touchUp()">
</div>

<div id="test"> 测试标签</div>
```


<br>
#### 三、完整的鼠标事件

**一个鼠标对HTML标签的完整执行过程
1> 当鼠标移动到某个HTML 标签后会 触发 onmouseover 事件
2> 当用户的鼠标按下时会触发 onmousedown 事件
3> 当用户松开鼠标会触发  onmouseup 事件
4> 当onmouseup 事件 事件执行完成就会执行 onclick 事件
5> 最后鼠标移除会执行 onmouseout 事件**

```
<script>

        function touchOver() {
            var msg =  "鼠标 进入";
            document.getElementById("test").innerHTML =  msg;
            console.log(msg);
        }

        function touchOut() {
            var msg =  "鼠标 移除";
            document.getElementById("test").innerHTML = msg;
            console.log(msg);
        }

        function touchDown() {
            var msg =  "鼠标 按下";
            document.getElementById("test").innerHTML = msg;
            console.log(msg);
        }

        function touchUp() {
            var msg =  "鼠标 抬起";
            document.getElementById("test").innerHTML = msg;
            console.log(msg);
        }

        function onClickComplete() {
            var msg =  "鼠标 点击 完成";
            document.getElementById("test").innerHTML = msg;
            console.log(msg);
        }

</script>



 <div class="touch"
         onmouseover="touchOver()"
         onmouseout="touchOut()"
         onmousedown="touchDown()"
         onmouseup="touchUp()"
         onclick="onClickComplete()">
 </div>
 <div id="test"> 测试标签</div>
    
```



