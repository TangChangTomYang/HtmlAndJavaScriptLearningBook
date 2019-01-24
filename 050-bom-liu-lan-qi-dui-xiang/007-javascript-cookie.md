

#### javaScript Cookie

Cookie 是用来识别用户的



<br>
#### 一、认识cookie
 
 
 <br>
**1、什么是Cookie?**

1> cookie 是存储在访问者的计算机中的变量. 
2> 每当同一台计算机通过浏览器请求某个页面时, 就会发送这个cookie. 你可以使用javaScript 来创建和取回 cookie.



<br>
**2、名字cookie**
当访问者首次访问页面时, 他或她也许会填写他/她的名字. 名字会存储在cookie 中. 当访问者再次访问网站时, 他们会收到类似 "welcome rose" 的欢迎词. 名字则是从 cookie 中取回的.




<br>
**3、密码cookie**
当访问者首次访问页面时, 她或他也许会填写他们的密码. 密码也可被存储在cookie 中. 当他们再次访问网站时, 密码就会从cookie中取出.


<br>
**4、日期cookie**
当访问者首次访问你的网站时, 当前的日子可存储于cookie 中. 当他们再次访问网站时, 他们会收到类似这样一条消息: "your last visit was 2018-1-1 12:02" 日期也是从




<br>
#### 二、设置、获取、清除 cookie 封装成一个 cookie.js

**1、设置cookie **
```
function setCookie(name,value,hours){  // 名字 值 过期时长
    var d = new Date();
    d.setTime(d.getTime() + hours * 3600 * 1000);
    document.cookie = name + '=' + value + '; expires=' + d.toGMTString();
}
```


<br>
**2、获取cookie**
```
function getCookie(name){  
    var arr = document.cookie.split('; ');
    for(var i = 0; i < arr.length; i++){
        var temp = arr[i].split('=');
        if(temp[0] == name){
            return temp[1];
        }
    }
    return '';
}
```
<br>

**3、删除cookie**
清除 cookie 其实很简单，只要使过期时间为过去时间就可以了。
```
function removeCookie(name){
    var d = new Date();
    d.setTime(d.getTime() - 10000);
    document.cookie = name + '=1; expires=' + d.toGMTString();
}
```




















