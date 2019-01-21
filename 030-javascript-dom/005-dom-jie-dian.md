#### DOM 节点

javaScript HTML DOM 元素(节点)



<br>
#### 添加和删除节点 (HTML 元素)


<br>
##### 一、创建新的 HTML 元素 

如需向 HTML DOM 添加新元素, 你必须首先创建该元素(元素节点), 然后向一个已存在的元素追加该元素.

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




