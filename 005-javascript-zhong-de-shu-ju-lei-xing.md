#### 一、javascript 中的数据类型

**1、简单的数据类型(number 数字类型), 包含正数/ 负数/ 小数. 不区分整数和浮点数.**

1> 十进制 
2> 十六进制 0x 开头
3> 八进制 0开头

```
var n1 = 12;
var n2 = -10;
var n3 = 15.5;
```



**2、字符串数据类型, 字符串由单引号或者双引号括起来**

```
var name = 'zhangsan';
var name1 = "lisi";
```

**3、布尔数据类型 **

```
var isMan = false;
var isTrue = true;

var n1 = 10;
var n2 = 20;
var isBig = n1 > n2;
```
**4、定义了变量,未给变量初始化, undefined **
```
var num;
typeof(num); // undefined 变量未初始化
```

**5、 null 变量值为空**

```
var name = "zhangsan";
name = null; // 主要的作用,把已经定义的变量清空
```

**null:**
javascript 中的关键字, 它表示一个特殊值.通常用来描述"控制".

**undefined:**
表示的是值的空缺. 他是变量的一种取值,表示变量未被初始化.
在ECMAScript3中, undefined 是可读写的变量,可以给它赋任意值. 在ECMAScript5中将这个错误进行了修改. 只有undefined 这一个值.




<br>
#### 二、判断数据类型 
```
var age = 10;
var type = typeof(age);
alert(type);
```