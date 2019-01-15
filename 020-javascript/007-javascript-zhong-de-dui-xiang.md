#### javaScript 对象

[javascript 对象](http://www.w3school.com.cn/js/js_objects.asp)

javaScript 中所有的事物都是对象: **字符串/ 数值/ 数组/ 日期/ 函数...** ,此外,javaScript 允许自定义对象.




<br>
在javaScript 中, 对象是数据(变量) 拥有属性和方法
,javaScript 提供多个内健对象, 比如: String/ Date/ Array 等等. **对象只是带有属性和方法的特殊数据类型.**






#### 一、访问对象的属性
属性是与对象相关的值
```
访问对象的属性语法:
objName.propertyName; // 方式一
objName["propertyName"]; // 方式二, 也可以访问对象的属性


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
```
funcion person(name, age, eyeColor){
  this.name = name;
  this.age = age;
  this.eyeColor = eyeColor;
}

this.changeName = changeName;
function changeName(name){
 this.name = name;
}
```



<br>
#### 六、 javaScript 类

javaScript 是面向对象(基于对象)的语言,但javaScript 不使用类.
在javaScript 中不会创建类, 也不会通过类来创建对象.

javaScript 是基于prototype, 而不是基于类的.


<br>
#### 七、 javaScript 中的for...in 可以用来遍历对象的属性, 也可以用来遍历数组的index



**javaScript 中的for...in 语句循环遍历对象的属性**



```
func Person(name , age , eyeColor){
 this.name = name;
 this.age = age;
 this.eyeColor = eyeColor;
}

var pson = new Person("zhangsan", 18, "blue");

for(propertyName in pson){ // 会将属性名,一个一个的遍历出来
 
 //取出对象中 对应属性的值
 alert(pson[propertyName]); 
}

```


**javaScript 中的for...in 语句循环遍历数组的 序号**




```
var cars = new Array("audi", "bmw", "volvo");

    for (index in cars ){  // 遍历序号
        console.log(cars[index]);
    }
```





