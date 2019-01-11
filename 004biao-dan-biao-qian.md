#### 004-表单标签

<br>

##表单标签

- 1 什么是表单?<br>
表单就是专门用来收集用户信息的,比如: 用户登录界面(里面主要就包含了表单)<br>
![](/assets/Snip20180815_3.png)


- 2 什么是表单元素?<br>
表单元素其实还是html中的一些标签,是不过这些标签比较特殊,在浏览器中所有的表单标签都有特殊的外观和默认的功能.

- 3 格式

```
<form action="https://www.baidu.com">

    账号:<input type="text"><br>
    密码:<input type="password"><br>
    <!--(2)默认请款下,单选框是不会互斥的, 只有个不同的单选框设置了相同的name属性,那么这些单选框才会互斥
    (2) 默认情况下单选框是没有默认选中的, 要想单选框默认被选中,那么需要个对应的单选框设置checked属性=checked
    (3) 默认情况下,单选框是没有值得,需要给对应的单选框设置value属性来赋值-->
    性别:
    男<input type="radio" name="sex" value="male" checked="checked">
    女<input type="radio" name="sex" value="female">
    保密 <input type="radio" name="sex" value="secret"> <br>

    爱好:
    足球 <input type="checkbox" value="football">
    篮球 <input type="checkbox" value="basketball">
    跑步 <input type="checkbox" value="run"><br>
    
    <!--如果要设置提交按钮的标题,就设置value 属性-->
    <input type="submit" value="xxxx"><br>
    
    <!--表单中的按钮的主要应用场景 一般是配合js 来使用的-->
    <input type="button" value="我是按钮"><br>
    <!--图片按钮-->
    <input type="image" src="regis.jpeg"><br>
    <!--重置按钮的作用就是用来清空表单中已经填写好的内容-->
    <input type="reset">
    
</form>
```
- 4  如果想要表单中填写的内容提交到服务器,那么必须做一下3件事情:<br>
(1) 不要给form 添加一个action属性,通过action 属性指定提交到服务器的地址
(2) 需要给必要提交的表单元素添加name 属性,指定要提交的字段名
(3) 所有的 input 元素都必须写在form 标签以内


- 5 绑定输入框<br>
(1)方式1: 通过input的id属性值与要绑定的内容关联
```
<form action="https://www.baidu.com">

    <label for="name" >账号:</label><input type="text" id="name"><br>
    <label for="pwd">密码:</label><input type="password" id="pwd"><br>
    <input type="submit">
</form>
```
![](/assets/Snip20180815_6.png)
(2)方式二, 直接使用label 标签把需要关联的input标签包裹起来
```
<form action="https://www.baidu2.com">
    <label>账号: <input type="text" ></label><br>
    <label>密码: <input type="password" ></label><br>
    <input type="submit">
</form>
```



***
<br>
#### datalist 标签 (待选列表)

- 作用:
定义一个待选列表,并将这个待选列表绑定给指定的输入标签(input 标签).

- 如何给输入框指定待选列表(datalist)
(1) 创建一个datalist标签,并填写好内容, 并设置好id 属性
(2) 创建一输入框(input 标签), 并指定这个输入框的list 属性为 datalist 的id 值.

- 格式:

```
<form action="thhps://wwwbaidu,.com">
    <!--通过list 属性来获取 指定的详细列表-->
    请输入地点名: <input type="text" list="address">
    <input type="submit">
</form>

<!--添加id属性,来提供给外界访问该list 的信息-->
<datalist id="address">
    <option  >"北京"</option>
    <option  >"上海"</option>
    <option  >"天津"</option>
    <option  >"广州"</option>
    <option  >"成都"</option>
    <option  >"深圳"</option>

</datalist>
```
![](/assets/Snip20180815_7.png)

- **注意:**
datalist 这个属性了解就可以了因为很多浏览器都不支持
![](/assets/Snip20180815_9.png)

***
<br>

#### input 标签在 HTML 5 新增的类型 (这个也是了解一下就可以了因为很多浏览器是不支持的)

```
    <input type="email">
    <input type="url">
    <input type="number">
    <input type="color">
    <input type="date">
    <input type="datetime">
    <input type="datetime-local">
    <input type="color">
```




***
<br>

#### select 标签 (下拉标签)

- 作用:
用于定义下拉列表(只能选择的标签)


- 格式:
(1)方式1

```
<select id="address">

    <option  >"上海"</option>
    <option  >"天津"</option>
    <option  >"广州"</option>
    <!-- 通过 selected 属性来设置下拉列表的默认值 -->
    <option  selected="selected">"北京"</option>
    <option  >"成都"</option>
    <option  >"深圳"</option>

</select>
```
![](/assets/Snip20180815_12.png)


(2)方式2

```
<select >
    <optgroup label="北京">
        <option>朝阳区</option>
        <option>昌平区</option>
        <option>通州区</option>
    </optgroup>

    <optgroup label="广州">
        <option >天河区</option>
        <option >越秀区</option>
        <option >黄浦区</option>
    </optgroup>
</select>
```
![](/assets/Snip20180815_15.png)

- 注意: <br>
(1)虽然datalist标签 和 select 标签很像,但是datalist 和 select表的作用场景是不同的. datalist是用来定义一个待选列表 可以绑定给指定的 输入标签(input标签),但是select 并不是一个待绑定的列表, 它自己就是一个列表.
(2)下拉列表(select) 是不能输入的,但是它是可以选择的















***
<br>


#### textarea 标签

- 作用
定义一个多行的输入框

- 格式
(1)格式1
```
<textarea>
</textarea>
```
(2)格式2
```
<textarea name="" id="" cols="30" rows="10">
</textarea>
```

- 注意点:
(1) 默认情况下, 多行输入框textarea 是可以任意换行的.
(2) 默认情况下, 多行输入框textarea 是有默认的宽度和高度的.
(3) 可以通过  cols 和 rows 属性来指定输入框的宽度和高度.
(4) 默认情况下,输入框是可以手动拉伸的.(通过 resize 属性来控制)




***
<br>


#### form 表单实战

```
<form action="https://www.baidu.com">
    //  fieldset是用来设置表单的框线的, 表单内容必须写在这个标签内部
    <fieldset>
        // legend 是用来设置表单框线上的标题的
        <legend><h2>注册页面</h2></legend>
        
        <label>账号: <input type="text" name="account"></label><br><br>
        <label for="pwd">密码:</label> <input type="password" name="pwd" id="pwd" ><br><br>
        性别:
        <input type="radio" value="male" name="sex" checked="checked"> 男
        <input type="radio" value="female" name="sex"> 女
        <input type="radio" value="secret" name="sex"> 保密<br><br>

        爱好:
        <input type="checkbox" value="football" name="lover"> 足球
        <input type="checkbox" value="basketball" name="lover"> 篮球
        <input type="checkbox" value="run" name="lover">跑步 <br><br>

        <label>个人简介: <textarea name="introduce" id="introduce" cols="15" rows="5"></textarea></label> <br><br>

        <label>生日: <input type="date"></label><br><br>

        <label>邮箱: <input type="email"></label><br><br>

        <label>手机: <input type="number"></label><br><br>

        <input type="submit" value="注册"> &emsp;&emsp;&emsp; <input type="reset" value="清空">

    </fieldset> 

</form>
```
![](/assets/Snip20180815_16.png)




 





