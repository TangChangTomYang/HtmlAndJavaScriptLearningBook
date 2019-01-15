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

****
<br> 
#### 一、javaScript 中的函数语法

在javaScript 中, 函数就是包裹在花括号{} 中的代码块, 前面使用了关键字 **function**

```
function funcName(){
    // 这里是要执行的代码
}
```

<br>
**1、  带参数的函数**
```
// 声明带参数的函数
function myFunc(var1,  var2){ // 在定义函数不必指明函数的参数类型
    // 执行逻辑
}

// 调用带参数的函数
myFunc(var1, var2);
```

<br> 
**2、带返回值的函数**

有时我们希望函数将值返回调用它的地方.
通过使用return 语句就可以实现
在使用 return 语句时, 函数会停止执行(javaScript 并不会停止执行,仅仅是函数后面不执行了), 并返回指定的值

```
function myFunc(var1, var2){
    // 执行逻辑
    return xxx;
}
```


