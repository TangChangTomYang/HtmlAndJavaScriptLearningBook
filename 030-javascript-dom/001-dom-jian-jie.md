#### javaScript HTML DOM简介


<br>
**通过 HTML DOM, 可以访问 javaScript HTML 文档的所有的元素**


<br>
#### 一、HTML DOM (文档对象模型)

当网页被加载时, 浏览器会创建页面的**文档对象模型 (Document Object Model)**


![** HTML DOM 模型被构造为对象树**](/assets/Snip20190116_11.png)

通过可编程的对象模型, javaScript 获得了足够的能力来创建 动态的HTML

- HTML 能够改变页面中所有的 HTML 元素
- HTML 能够改变页面中所有的 HTML 属性
- HTML 能够改变页面中所有的 CSS 样式
- javaScript 能够对页面中的所有事件作出反应.


<br>
#### 二、查找HTML 元素

通常, 通过javaScript , 你需要操作 HTML 元素.

为了做到这件事情, 你必须先找到该元素, javaScript 中有3种方式来查找对应的标签

 - **通过Id 找到对应的 HTML 标签**
 - **通过类名找到HTML 标签**
 - **通过标签名找到 HTML标签**
 

<br>
##### (一)、通过Id 查找HTML 标签

在 DOM 中查找HTML 元素最简单的方式,就是通过元素 的Id来查找.

```
// 查找 id = "demo" 的元素/ 标签
var element = document.getElementById("demo");

// 如果能找到对应的标签, 则element 就位对应的标签(对象), 否则 element = null;
```


<br>
#### (二)、通过类名查找HTML 标签


<br>
#### (三)、通过标签名查找对应的 标签
















