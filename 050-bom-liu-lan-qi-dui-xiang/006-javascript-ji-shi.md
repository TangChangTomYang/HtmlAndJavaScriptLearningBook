

#### javaScript 计时器





<br>
**1、通过javaScript , 我们可以做到在一个设定的时间间隔之后来执行代码, 而不是在函数被调用后立即执行, 我们称之为计时器事件**

**2、在javaScript 中使用计时事件, 有2个关键的方法:**

- setTimeOut("doSomeThing()", timeInterval); //  timeInterval 毫秒后 做 doSomeThing() 这件事情

- clearTimeOut() // 取消 setTimeOut()




<br>
**一次性定时器示例:**
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


<br>
**无限 循环 定时器示例**

要创建一个运行于无穷循环中的定时器, 我们只需要编写一个函数来调用其自身

```
<script>
        var count = 0;
        var timer = null;

        function timerCount() {
            count += 1;
            timer = setTimeout("timerCount()", 1000);
            console.log(count);
        }

        function stopTimerCount() {
            clearTimeout(timer);
        }

</script>
    
    
<button type="button" onclick="timerCount()"> 点击循环计数</button><br>
<button type="button" onclick="stopTimerCount()"> 点击 停止循环计数</button>


```