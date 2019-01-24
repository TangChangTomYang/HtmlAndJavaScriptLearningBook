

#### javaScript Window Navigator

1、window.navigator 对象包含有关访问者浏览器的信息

2、windor.navigator 对象在编写时可不使用 window 这个前缀

```
 <script>
        function displayNavigatorInfo() {
            console.log("appCodeName: " + navigator.appCodeName);
            console.log("appName: " + navigator.appName);
            console.log("appVersion: " + navigator.appVersion);
            console.log("cookieEnabled: " + navigator.cookieEnabled);
            console.log("platform: " + navigator.platform);
            console.log("userAgent: " + navigator.userAgent);
            console.log("systemLanguage: " + navigator.systemLanguage);


        }
</script>
```

![](/assets/Snip20190124_1.png)