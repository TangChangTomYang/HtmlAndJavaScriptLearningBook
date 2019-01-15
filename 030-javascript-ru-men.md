#### javaScript 入门



<br>
**1、javaScript 写入HTML 输出**

```
<script>

    document.write("<h1>这个是标题</h1>");
    document.write("<p>这个是段落</p>")
    document.write(" <div style=\"width: 120px; height: 20px; background-color:red;\"></div>");

</script>
```
![](/assets/Snip20190115_2.png)



<br>
2、 HTML 标签 调用javaScript 方法

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

     
    <script> 
        function chagneName() {
            document.getElementById("demo").innerHTML = "我的名字叫李四"; 
        }
    </script>
</head>
<body>

    <p id="demo"> 张三 </p>
    // 当按钮点击时, 执行chagneName() 这个方法 修改名字
    <button type="button" onclick="chagneName()"> 点击这里弹窗 </button>

</body>
</html>
```