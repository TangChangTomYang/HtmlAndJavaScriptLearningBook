#### javaScript 中的函数


在javaScript 中 函数是由事件驱动的, 或者当他被调用时执行的可重复使用的代码块,如下:


```
<!DOCTYPE html>
<html>
    <head>
        <script>
            function myFunction() {
                alert("Hello World!");
            }
        </script>
    </head>

    <body>
        // 当用户点击这个按钮是, 执行上面 js 中的 myFunction 方法
        <button onclick="myFunction()">点击这里</button>
    </body>
    </html>
```
