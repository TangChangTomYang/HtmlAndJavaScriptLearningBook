

#### javaScript 计时器



通过javaScript , 我们可以做到在一个设定的时间间隔之后来执行代码, 而不是在函数被调用后立即执行, 我们称之为计时器事件

在javaScript 中使用计时事件, 有2个关键的方法:

- setTimeOut("doSomeThing()", timeInterval); //  timeInterval 毫秒后 做 doSomeThing() 这件事情

- clearTimeOut() // 取消 setTimeOut()


示例:
```
<script>

        var timer = null;
        //设置定时器
        function displayWebUrl() {
            console.log("==============");
            timer = setTimeout("alert(location.href)",5000);  /*5000毫秒(5s)后显示 网页的网址*/
        }

        //清除定时器
        function clearTimer() {
            console.log("---------------");
            clearTimer(timer);
        }

</script>


<button type="button" onclick="displayWebUrl()"> 5s 后 显示 web 的 url</button>

<button type="button" onclick="clearTimer()"> 点击清除定时</button>
```