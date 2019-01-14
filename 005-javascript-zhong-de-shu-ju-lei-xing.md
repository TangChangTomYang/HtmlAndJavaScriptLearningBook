#### javascript 中的数据类型

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
**4、变量未初始化 **
```
var num;
typeof(num); // undefined 变量未初始化
```



**2、判断数据类型**
```
var age = 10;
var type = typeof(age);
alert(type);
```