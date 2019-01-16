#### DOM 改变 HTML

HTML DOM 允许javaScript 改变 HTML元素内容.







<br>
#### 一、改变 HTML 输出流

javaScript 能够创建动态的 HTML 内容


在javaScript 中, document.write() 可用于直接向 HTML输出流写内容.

```
// 在当前的网页输出 "当前的时间"
document.write(Date());

// document.write(); 不仅可以输出文本, 还可以输出标签
```

**注意:**
绝对不要使用在文档加载之后使用 document.write(). 这会覆盖整个网页.








<br>
#### 二、改变 HTML 内容
修改HTML 内容的最简单方法是使用 **innnerHTML** 属性
如果需要改变 HTML 的内容,请使用这个语法

```
document.getElementById("demo").innerHTML = new HTML ;
```





<br>
#### 三、改变HTML 属性 (注意: 属性和CSS样式不同)

如需修改 HTML标签的属性, 请使用 **document.getElementById(id).attribute = new value ;**



<br>
修改图片
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <script> 

        function myfunc() {
            var element = document.getElementById("box");
            alert(element);
            element.src =  "../image/b.png"; 
        }
    </script>

</head>
<body> 
    <img id="box" src="../image/a.png" alt="">
    <button type="button" onclick="myfunc()">点击且含</button>
</body>
</html>
```


