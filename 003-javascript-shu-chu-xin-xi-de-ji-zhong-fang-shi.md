#### javascript 中输出信息的几种方式

1、**alert("输出信息"); ** 在页面显示一个弹窗,早期的js调试使用

![](/assets/Snip20190114_6.png)

2、**confirm("输出的对话信息");** 在页面弹出一个对话框, 常配合 if 做条件判断

  ![](/assets/Snip20190114_7.png)
  
3、**console.log("输出信息");** 将信息输出到控制台, 用于在js中调试

![](/assets/Snip20190114_8.png)

4、 **prompt();**, 弹出对话框, 用于接收用户输入的信息

![](/assets/Snip20190114_9.png)

5、**document.write("在页面上输出信息");**, 

![](/assets/Snip20190114_10.png)

**document.write(); 标签除了可以输出文字内容, 还可以输出标签**,如下图
```
document.write("document.write() 可以输出文字,<br> <strong>也可以输出标签</strong>");

document.write("<div style=\"background-color: red; width: 120px; height: 20px\" ></div>");
```

![](/assets/docmentwrite.png)