####一 div 和 span 

- 什么是div?
一般用于配合CSS完成网页的基本布局
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title> 
    <style>
        .head{
            width: 500px;
            height: 100px;
            background: red;
            margin: 0 auto;
            margin-bottom: 10px;
        }
        .content{
            width: 500px;
            height: 500px;
            background: green;
            margin: 0 auto;
            margin-bottom: 10px;
        }
        .footer{
            width: 500px;
            height: 100px;
            background: blue;
            margin: 0 auto;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
<div class="head"></div>
<div class="content"></div>
<div class="footer"></div>
</body>
</html>
```
![](/assets/Snip20180904_5.png)

- 什么是span?
**一般用于配合CSS修改网页中的一些局部信息.**
```
span{
    color: red;
}
<p>努力到<span>无能为力</span>,拼搏到<span>感动自己</span></p>
```
![](/assets/Snip20180904_6.png)

- 什么是div 和 span?
(1) div 会独占一行,而span不会独占一行.
(2) div 是一个容器标签,而span 是一个文本级的标签.

- **容器级的标签和文本级的标签区别?**
(1) **容器级别的标签可以嵌套其它所有的标签**
(2) **文本级的标签只能嵌套 文字/超链接 /图片**


- 容器级标签
**div, h, ul, ol, dl, li... **

- 文本级标签
**span, p, buis, strong, em, ins, del ...**

- 我们可以通过google 开发者工具来查看标签的嵌套是否正确
```
// 正确写法
<h1>我是标题
<div>我是h1中的div</div>
</h1>
```
![](/assets/Snip20180904_7.png)

```
// 错误写法
<p>我是段落
<div>我是p中的div</div></p>
```
![](/assets/Snip20180904_10.png)






***
<br>
####二 CSS 元素显示模式

- 1 什么是html标签的显示模式呢?
在html 中将所有的标签分为2类,分别是容器级和文本级标签,
在CSS中CSS也将标签分为2类,分别是块级标签和行内标签, 行内块级标签

- 2 什么是块级标签, 什么是行内标签, 什么是行内块级标签

