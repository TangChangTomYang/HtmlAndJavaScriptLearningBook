#### onchange 事件

onchange 常结合对输入字段的验证来使用
```
 <script>
        function myFunc() {
            var inputField = document.getElementById("inputField");
            inputField.value = inputField.value.toUpperCase();
        } 
</script>

...

请输入英文字符: <input id="inputField" type="text" onchange="myFunc()" style="width: 200px; height: 50px; background-color:purple;" >

<p>当你离开输入字段时, 会触发将输入的文本转换成大写函</p>
```