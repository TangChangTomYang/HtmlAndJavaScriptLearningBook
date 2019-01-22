#### javaScript 正则表达式



<br>
#### 一、javaScript RegExp 对象

**RegExp** 对象用于**匹配**文本中的内容

**1、什么是RegExp ? **

RegExp 是正则表达式的缩写
当你检索某个文件时,可以使用一种模式来描述要检索的内容.


<br>
**2、定义RegExp 对象 (检索规则)**

```
// 定义一个正则 要求字符串必须包含 'abc'
var regExp1 = new RegExp("abc"); 


// 定义一个正则, 要求检索字符串中的 'abc', 'g' 参数的意思是全局检索(当第一个位置检索到后会被记住,下次从上次检索完毕位置继续检索)
var regExp2 = new RegExp("abc","g"); 
```






<br>
**3、RegExp 正则表达式的对象方法(3个)**

1> **test()** 检查是否包含, 返回bool值
```
var regExp = new RegExp("abc"); //匹配 'abc'
var rst = regExp.test("abcdefg"); // 检测'abcdefg'中是否包含'abc' 返回bool 值
```

2> **exec()** 检索出包含的字符串


情景1, 只检测一次

```
var regExp = new RegExp("abc"); //匹配 'abc'
var rst = regExp.exec("abcdabc"); // 检测'abcdabc'中是否包含'abc' 返回包含的字符串 'abc', 只检测一次, 找到就结束
```
情景2, 可检测多次
```
var regExp = new RegExp("abc","g"); //全局匹配 'abc'

var rstStr = "";
do{
  var rst = regExp.exec("abcdabc");
  if(rst != null){
    rstStr = rstStr + " " + rst ;
  }
}while(rst != null);  // 一直找, 直到找完为止

结果为: 'abc abc'
```






