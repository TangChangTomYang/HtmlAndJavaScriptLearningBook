#### javaScript Window Location


**1、window.location 对象用于获取当前页面的地址(URL), 并把浏览器重定向到新的页面.**



<br>
#### 一、window location


**1、window.locatiom 对象在编写时可以不使用 window 这个前缀**
 
 如下:
 ```
 location.hostname // 返回web 主机的域名
 location.pathname // 返回当前页面的路径和文件名
 location.port // 返回web 主机的端口 (80 或 443)
 location.protocal // 返回所使用的 web 协议(http:// 或 https://)
 ```
 
 
 
 <br>
 #### 二、window location href
** 2、location.href 属性返回当前页面的 URL **
```
location.href // 返回当前页面的 url
```







<br>
#### 三、window location assign

location.assign() 方法加载新的文档



综合示例如下:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>

    <script>

//        获取web主机域名
        function currentHostName() {
            alert(location.hostname);
        }

//        获取当前页面的路劲
        function currentPathName() {
            alert(location.pathname);
        }

//        获取当前的主机端口号 (80 或 443)
        function currentPOrt() {
            alert(location.port);
        }

//        获取当前的协议 (http:// 或 https:// )
        function currentProtocol() {
            alert(location.protocol);
        }

//        获取当前网页的URL
        function currentUrl() {
            alert(location.href);
        }

//        加载新的文档
        function loadNewPage() {
            location.assign("http://localhost:63342/JS/window/001-window.html?_ijt=lvmem050f9mo42ohcom7sej6c");
        }

    </script>

</head><br>
<body>

<button type="button" onclick="currentHostName()"> 获取web主机域名 </button><br>
<button type="button" onclick="currentPathName()"> 获取当前页面的路劲 </button><br>
<button type="button" onclick="currentPOrt()"> 获取当前的主机端口号 (80 或 443) </button><br>
<button type="button" onclick="currentProtocol()"> 获取当前的协议 (http:// 或 https:// ) </button><br>
<button type="button" onclick="currentUrl()"> 点击获取当前的 URL </button><br>

<button type="button" onclick="loadNewPage()"> 加载新的文档 </button><br>
</body>
</html>
```













