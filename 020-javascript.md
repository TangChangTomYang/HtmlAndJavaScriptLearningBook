#### javascript


[javascript 学习网址](http://www.w3school.com.cn/js/js_objects.asp)



在 javascript 中, 程序执行的过程是从上而下, 遇到错误不会再往下执行.


```
<script>

        function appendNode() {

            var p = document.createElement("p");
            var pNode = document.createTextNode("新增的段落3");
            p.append(pNode);
            p.style.backgroundColor="purple";
            p.style.width = "200px";


            var div = document.getElementById("box");
            div.appendChild(p);
        }
    </script>
    
    ...
    
    <div id="box">
        <p>我是段落1</p>
        <p>我是段落2</p>

    </div>
    <button type="button" onclick="appendNode()">点击增加一个段落 </button>
```