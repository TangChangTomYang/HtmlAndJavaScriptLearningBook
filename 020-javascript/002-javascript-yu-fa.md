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







<br>
#### 二、javascript 执行过程中的小原理

**html 页面** 中出现 **&lt; script &gt; ** 标签后, 就会让页面暂停等待脚本的解析和执行. 无论当前的脚本是内嵌还是外链, 页面的下载和渲染必须都停下来等待脚本的执行完成才能继续, 这在页面的声明周期内是必须的.


下图是通过外链式 js 文件,查看时长
![](/assets/rqjst.png)
从上图可以发现, 外链式的js使用方式,网页的加载时间较内嵌式的长, 其本质原因是,外链的是一个文件,没多一个外链文件就会多一次请求.


<br>
**结论: **
**1、为了减少在执行javascript 代码时,阻塞其它资源的下载/ 页面的渲染,推荐将 script 标签放在body标签之后**


**2、为了提高网页的访问速速推荐以下做法**

1> 不论是CSS 文件 还是 js 文件, 尽量使用 内嵌方式,减少服务器请求次数
2> 多个CSS 文件, 或是 js 文件, 尽量合并在一个CSS 文件内, 或者一个js 文件内, 减少服务器请求次数.
3> 能用精灵图的地方, 尽量使用精灵图, 减少服务器的请求次数.





<br>
#### 二、javascript  中的注释

当行注释 '//'

多行注释 '/* */'

