#### javaScript 对象

javaScript 中所有的事物都是对象: **字符串/ 数值/ 数组/ 函数...** ,此外,javaScript 允许自定义对象.


<br>
javaScript 提供多个内健对象, 比如: String/ Date/ Array 等等. **对象只是带有属性和方法的特殊数据类型.**






#### 一、访问对象的属性
属性是与对象相关的值
```
访问对象的属性语法:
objName.propertyName;


var msg = "Hello javaScript";
var len = msg.length; // 通过属性获取字符串的长度
```






<br>
#### 二、访问对象的方法
方法是能够在对象上执行的动作
```
访问对象的方法的语法:
objName.methodName();

var msg = "hello javascript";
msg.toUpperCase(); // 将小写转换为大写

```









<br> 
#### 三、创建javaScript 对象

通过javaScript 你能定义并创建自己的对象.


**创建对象有2种不同的方法:**

 ** ⭐️ ⭐️ ⭐️ 1、 定义并创建对象的实例**
```
这个例子创建了对象的一个新实例, 并向其中添加了4个属性
var person = new Object();
person.mame = "zhangsan";
person.age = 25;
person.eyeColor = "blue";


语法糖 
var stu = {name:"zhangsan",age:25,sex:"man"}; // 属性名: 属性值
```

2、 使用函数来定义对象, 然后创建新的对象实例.













