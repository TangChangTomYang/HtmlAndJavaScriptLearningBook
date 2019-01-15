#### javascript 中的变量

1、javascript 是基于对象的一门语言,而不是面向对象的一门语言.

2、javascript 是一门严格区分大小写的语言.

 ```
 javascript 中定义变量
 var age = 12;
 var name = "zhangsan";
 ```

3、定义一个变量, 用来接收用户的输入

```
<script>
  var name = prompt("请输入你的姓名");
  alert(name);
</script>
```
![](/assets/Snip20190114_14.png)




<br>
#### javascript 中局部变量 和 全局变量


**1、局部 JavaScript 变量**
在 JavaScript 函数内部声明的变量（使用 var）是局部变量，所以只能在函数内部访问它。（该变量的作用域是局部的）。
 
只要函数运行完毕，本地变量就会被删除。



**2、全局 JavaScript 变量**
在函数外声明的变量是全局变量，网页上的所有脚本和函数都能访问它。



**3、JavaScript 变量的生存期**
JavaScript 变量的生命期从它们被声明的时间开始。
局部变量会在函数运行以后被删除。
全局变量会在页面关闭后被删除。