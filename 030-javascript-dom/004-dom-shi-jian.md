#### DOM 事件


**HTML DOM 使javaScript 有能力对 HTML 事件作出反应.**




<br>
#### 一、 对事件做出反应

我们可以在事件发生时执行 javaScript, 比如: 当用户在 HTML 元素上点击时.

如需在用户点击某个元素时执行代码, 请向一个 HTML 事件属性添加 javaScript 代码
```
onclick=javaScript
```


HTML 事件的例子

- 当用户点击鼠标时
- 当网页加载时
- 当图像已加载时
- 当鼠标移动到元素上时
- 当输入字段被改变时
- 当提交 HTML 表单时
- 当用户触发按键时

<br>
##### (一)、 当用户在 &lt; h1 &gt; 元素上点击时, 改变其内容

通过给标签设置 **onclick** 属性,给标签绑定点击事件(当标签被点击了做...)

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <script>
//        修改元素的内容 和 样式
        function myfunc(thisElement) {

            thisElement.innerHTML = "我是大大标题";
            thisElement.style.backgroundColor = "red";
        }
    </script>
</head>
<body>
    <!--修改元素的内容 和 样式-->
    <h1 onclick="myfunc(this)"> 我是大标题</h1>

    <!--修改元素的内容-->
    <h2 onclick="this.innerHTML='wo shi er ji biao ti'"> 我是二级标题</h2>
</body>
</html>
```
![](/assets/Snip20190116_14.png)