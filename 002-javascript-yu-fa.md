#### javaScript 语法


<br>
#### 一、javascript 的书写位置 (其实javascript 可以写在html 的任何位置)


**方式一: 内嵌**
1、写在head里面 
(不推荐这种做法, 前面的js 没做完就会一直卡住不执行后面的代码) 

![](/assets/Snip20190111_7.png)

2、写在HTML 的最后面, 这样后面的javascript代码的执行就不会影响前面的html代码的执行,推荐这种

![](/assets/Snip20190114_3.png)



**方式二: 外部链接**

1、先创建一个`xxx.js` 文件, 将javascript 写在里面.
2、通过 <script src="xxx.js"> </script> 导入javascript 代码调用
1> 在head里面导入, 和内嵌在head里的javascript 代码一样,容易卡住
![](/assets/Snip20190114_5.png)
2> 在html 的尾部导入, 推荐方式
![](/assets/Snip20190114_4.png)

