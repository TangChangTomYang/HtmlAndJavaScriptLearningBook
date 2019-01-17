#### DOM 网页加载事件


#### 一、**onload 和 onunload 事件**

1、onload 和 onunload 事件会在用户进入或者离开页面时被触发.
2、onload 事件可用于检测访问者的浏览器类型和浏览器版本, 并基于这些信息来加载页面的正确版本.
3、onload 和 onunload 事件可用于处理 cookie.

示例:

```
<script>
    function checkCookies() {
        if (navigator.cookieEnabled == true){
            alert("已启用 Cookie");
        }
        else {
            alert("未  启用 cookie");
        }
    }
</script>
    
...

<body onload="checkCookie()">
</body>
```

