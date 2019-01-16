#### javaScript 中的错误


<br>
#### 一、javaScript 错误, Throw/ Try/ Cathch


- try 语句测试代码块错误 ❌.
- catch 语句处理代码错误 ❌.
- throw 语句创建自定错误 ❌.



<br>
#### 二、错误一定会发生
当javaScript 引擎执行 javaScript 代码时, 会发生各种错误.

- 可能是语法错误 ❌ ,通常是程序员造成的编码错误或者错别字.
- 可能是拼写错误 ❌ ,或语言中缺少的功能 (可能由于浏览器差异)
- 可能是由于来自服务器或用户的错误输出导致的错误 ❌
- 当然, 也可能是由于许多其他不可预测的因素. ❌







<br>
#### 三、javaScript 抛出错误 ❌

当错误发生是, 当事情出问题时, javaScript 引擎通常会停止,并生成一个错误消息.

描述这种情况的技术术语是: javaScript 将抛出一个错误.









<br>
#### 四、javaScript 测试和捕捉



**1、 try 语句允许我们定义 (执行时) 进行错误测试的代码块** , 简单的说就是, **使用try 语句定义 错误测试代码块**


**2、 catch 语句允许我们当 try 语句代码块发生错误时, 所执行的代码块**


**3、javaScript 中 try 语句和 catch 语句是成对出现的**


**4、try{...} catch(err){...} 示例,如下:** 

```
<!DOCTYPE html>
<html lang="en">


<head>
    <meta charset="UTF-8">
    <title>javascript </title>
    <script >
            function myFunc(){

                try { /*测试要执行的代码, 防止错处*/

                    lert(" try 错误");   /*我们这里故意将 'alert' 写错为 'lert' 报错*/
                }
                catch (err){ /*当上面的try 检测到错误就会来到catch, 并说明错误原因*/

                    var msg = "这里检测到错误:\n";
                    msg += err.message ;    /*通过 err 的 message 属性,获取具体的错误信息*/
                    msg += "\n";
                    alert(msg);
                }
            }

    </script>

</head>

<body>

<button type="button" onclick="myFunc()"> 点击 按钮 测试 try catch 错误</button>
</body>
</html>
```
![](/assets/Snip20190116_2.png)


**5、Throw 语句,** throw 语句允许我们创建自定义错误**(术语: 创建或抛出异常(exception) )**

如果把 **throw** 与 **try** 和 **catch** 一起使用, 那么你能够控制程序流, 并生成自定义的错误消息.




