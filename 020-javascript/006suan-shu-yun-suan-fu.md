#### 算数运算



<br>
#### 一、相加
1、两个数字类型的变量相加, 得到的是数字类型
2、一个数字类型(数字会被转换成对应的字符串) 和 一个字符串类型相加得到一个字符串类型

```
数字+数字= 数字
var n1 = 10;
var n2 = 20;
var n3 = n1 + n2; // 结果是30;

数字+字符串=字符串
var num1 = 10;
var str1 = "abc";
var rst = num1 + str1 ; // 结果为10abc
```

<br>

#### 二、相减
1、两个数字类型相减,得到的是数字类型
2、一个数字类型和另一个字符串(字符串会被转换成对应的数字)相减得到的是数字类型

```
数字 - 数字 = 数字
var n1 = 10;
var n2 = 30;
var n3 = n1 -n2 ; // 结果为-20

数字 - 字符串 = 可能为数字 / 可能为NaN(NaN 也是Number 数据类型)
var num = 20;
var str = 'abc'; // 不能转换成数字
var rst = num - str; // 结果是NaN

var num = 20;
var str = '12345'; // 能转换成数字
var rst = num - str; // 结果是 -12325
 
```

<br>

#### 三、相乘 (相除类似于相乘)
1、两个数字类型相乘,得到的是数字类型
2、一个数字类型和另一个字符串(字符串会被转换成对应的数字)相乘得到的是数字类型

```
数字 - 数字 = 数字
var n1 = 10;
var n2 = 30;
var n3 = n1  * n2 ; // 结果为300

数字 * 字符串 = 可能为数字 / 可能为NaN(NaN 也是Number 数据类型)
var num = 20;
var str = 'abc'; // 不能转换成数字
var rst = num * str; // 结果是NaN

var num = 20;
var str = '12345'; // 能转换成数字
var rst = num * str; // 结果是 246900
```

3、一个数字 除以 0, 得到的输一个数字类型, 但数值是一个 Infinity (无限大)
```
var n1 = 10;
var n2 = 0;
var rst = n1 / n2 ; // 结果为 Infinity
```
![](/assets/Snip20190115_1.png)




<br>
#### 四、带操作的赋值运算符

|运算符|实例|等价于|
|-|-|-|
|+=|a+=b;|a= a + b;|
|-=|a-=b;|a= a - b;|
|*=|a*=b;|a= a * b;|
|/=|a/=b;|a= a / b;|






<br>
#### 五、 NaN  Not a Number 表示不是一个数字

```
判断是不是一个数字, 使用 isNaN(x);
```











