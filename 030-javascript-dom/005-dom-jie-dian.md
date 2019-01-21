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
    
        //1. 创建新的 <p> 标签
        var p = document.createElement("p");
        
        // 如需向<p>标签添加文本, 你必须首先创建文本节点
        //2. 创建文本节点
        var pNode = document.createTextNode("新增的段落3");
        
        //3. 向<p>标签 追加文本节点
        p.append(pNode);
        //4. 修改元素的 样式
        p.style.backgroundColor="purple";
        p.style.width = "200px";
        
        var div = document.getElementById("box");
        
        //4. 向已经存在的节点 追加新元素
        div.appendChild(p);
    }
</script>

... ...

<div id="box">
<p>我是段落1</p>
<p>我是段落2</p>

</div>
<button type="button" onclick="appendNode()">点击增加一个段落 </button>
```










<br>
##### 二、删除已有的 HTML 元素 

如需删除 HTML 元素, 你必须首先获得该元素的父元素

<br>
删除子节点

```
<script>

    function deleteP() { 
        //找出父节点
        var divEle = document.getElementById("box"); 
        //找出子节点
        var pEle = document.getElementById("para1");
        //删除子节点
        divEle.removeChild(pEle);   
    }

</script>

 <div id="box">
        <p id="para1">我是段落1</p>
        <p id="para2">我是段落2</p>
        <p id="para3">我是段落3</p>
        <p id="para4">我是段落4</p>
    </div>

<button type="button" onclick="deleteP()" >点击删除标签 </button>
```




<br>
删除自己
```
<script>
    function deleteSelf(){
        var self = document.getElementById("box");
        self.remove();
    }
</script>
```
