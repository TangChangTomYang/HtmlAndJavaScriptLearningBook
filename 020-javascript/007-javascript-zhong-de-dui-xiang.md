#### javaScript 对象

[javascript 对象](http://www.w3school.com.cn/js/js_objects.asp)

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

 ** ⭐️ ⭐️ ⭐️ 方式一:  定义并创建对象的实例**
```
这个例子创建了对象的一个新实例, 并向其中添加了4个属性
var person = new Object();
person.mame = "zhangsan";
person.age = 25;
person.eyeColor = "blue";


语法糖 
var stu = {name:"zhangsan",age:25,sex:"man"}; // 属性名: 属性值
```

** ⭐️ ⭐️ ⭐️ 方式二: 使用对象构造器创建对象(分2步: 构造和实例化)**

```

step1> 创建构造对象的函数
function Person(firstName, age, eyeColor){
  this.firstName = firstName;
  this.age = age;
  this.eyeColor = eyeColor;
}
 
step2> 使用构造对象的函数,构造对象
 
var stu = new Person("张三",18,"blue");
```

 
 
 
 
 
 
 
 
 <br>
 #### 四、给已经实例化的对象添加属性
 
 你可以通过为对象赋值, 向已有对象添加新的属性;
 
 比如: person 这个对象,已经有 name/ age/ eydColor 这3个属性了, 那么你可以 已向person 赋值的形式给它添加新的属性, 比如: sex
 
 ```
 var person = {name:"zhangsan", age:15, eycColor:"blue"}; //现在3个属性
 
 person.sex = "girl"; // 新增 sex 属性
 
 
 此后: person 这个对象就由 name/ age/ eyeColor/ sex 这4个属性了
 ```














<br>
#### 五、把方法添加到 javaScript 对象上

方法只不过时附加在对象上的函数


1、在构造函数内部定义对象的方法









