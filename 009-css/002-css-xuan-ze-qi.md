####CSS 选择器
- **标签选择器** --> (a、p...)
- **id选择器和类选择器** --> (#identity、.person)
- **后代选择器和子元素选择器** --> (选择器1 选择器2、选择器1>选择器2)
- **交集选择器和并集选择器** --> (选择器1选择器2、 选择器1,选择器2)
- **相邻兄弟选择器和通用兄弟选择器** --> (选择器1+选择器2、 选择器1~选择器2)
- **同级别第几个和同级别同类型第几个** --> (标签名:nth-child(1)、标签名:nth-of-type(2))
- **同级别倒数第几个,同级别同类型倒数第几个** --> (标签名:nth-last-child(2)、标签名:nth-last-of-type(2))
- **唯一子元素选择器和唯一类型子元素选择器** --> (p:only-child、 p:only-o-type)
- **属性名选择器, 属性值选择器** --> (标签名[属性名]、标签名[属性名=属性值])
- **通配符选择器**  --> (*)




<br>
****

####一 标签选择器
- 什么是标签选择器?
根据指定的标签名称,在当前的页面中找到所有该名称的标签,然后设置属性.

- 格式:
```
标签名称 {
    属性名:属性值;
}
// 注意点:  
(1) 标签选择器选择的是当前页面中的所有的标签,而不能单独选中某个标签
(2) 标签选择器,无论标签藏的有多深都能找到
(3) 只要是html中的标签, 都能作为标签选择器
```






<br>
****
####二 id 选择器
- 什么是id 选择器?
(1) 根据指定的id名称找到对应的标签,然后设置属性. 任何一个html 标签都有一个id属性.
(2) id 选择器是唯一的,一个页面中id的名称是不能重复的.

- 格式:
```
#id名称{
    属性名称: 属性值;
}
```
- 注意点:
(1) 每一个html 标签都有一个属性叫做`id`, 也就是说每个标签都可以设置`id`属性.
(2) 在一个界面中`id`的名称是不能重复的.
(3) 在编写id选择器时一定要在id的名称前面添加`#`号
(4) `id`的名称只能由字母 数字 下划线 组成.
(5) `id`的名称不能以数字开头,只能以字母和下划线开头
(6) `id` 的名称不能是html 中的标签名称
**(7) 在企业开发中一般情况下如果仅仅是为了设置样式,我们不会使用id, 因为在前端开发中 `id` 是留给`js` 使用的.**

- 
 
<br>
****
####三 类选择器

- 什么是类选择器?
类选择器就是通过指定的类名,找到指定的标签然后设置属性

- 格式:
```
.类名{
    属性名: 属性值;
}
// 一个类名
<p class="chengdu">我是段落</p>
// 二个类名
<p class="chengdu pixian">我是段落</p>
//错误写法
<p class="chengdu"  class="pixian">我是段落</p>
```

- 注意点:
(1) 每一个html 标签都有一个属性叫做`class`, 也就是说每个标签都可以设置`class`属性.
(2) 在一个界面中`class`的名称是 可以重复的.
(3) 在编写`class`选择器时一定要在`class`的名称前面添加`.`号
(4) `class`的名称只能由字母 数字 下划线 组成.
(5) `class`的名称不能以数字开头,只能以字母和下划线开头
(6) `class`的名称不能是html 中的标签名称
(7) 类选择器,就是专门用来给某一类标签设置样式的.










<br>
****
####四 id选择器和class选择器对比

- 1 id 相当于人的身份证,不可以重复. class 相当于人的名称可以重复.
- 2 一个html标签中只能绑定一个id选择器, 一个网页中id选择器的名称是不能重复的. 一个html标签可以绑定多个class 名称, 多个标签的class名称可以重复相同.
- 3 id选择器以`#`开头,class 选择器以 `.` 开头, id 选择器一般情况下是给js 使用的,所以除非特殊情况下不要使用id去设置样式.
- 4 在企业开发中一个开发人员对类的使用,可以看出开发水平.<br>
**一般情况下在企业开发中要注重冗余代码的抽取,可以将一些公共的代码抽取到一个类选择器中,然后让标签和这个类绑定即可.**

 






<br>
****
####五  后代选择器
![](/assets/Snip20180828_4.png)

- 什么是后代选择器
找到指定标签的所有后代标签,设置属性

- 格式:
```
标签名称1 后代标签名称{
    属性名: 属性值;
}
// 上面的含义是,先找到`标签名称1`选择器对应的所有的标签,
// 然后在这个标签里面去查找所有的 后代名称标签并设置属性
// 也可以这样
//
选择器1 选择器2 后代标签名称{
    属性名: 属性值;
}
//比如:
.man .ageLess20 p{
    color:red;
}
//注意: 后代不仅仅是儿子, 孙子 重孙子 ....只要是后代即可
``` 

- 注意点:
(1) 后代选择器必须用空格隔开,即 `选择器名称 后代标签`
(2) 后代选择器不仅仅可以使用标签选择器,还可以使用其它选择器, 其实后代选择器的工作原理是找到`指定标签`(父标签), 然后从`指定标签`(父标签) 里面的找出后代标签并设置其属性, 指定的标签具体怎么找到无所谓只要能找到即可.








<br>
****
####六  子元素选择器
- 什么是子元素选择器?
找到指定标签中所有特定的`直接子元素`,然后设置属性

- 格式:
```
标签名称1>标签名称2{
    属性名:属性值;
}
先找到标签名称1, 然后在这个标签中查找所有的直接子元素(儿子),然后再找出名称为 标签名称2 的元素(儿子)并设置属性. 
```

- 注意点:
(1) 子元素选择器只会查找儿子,不会查找其他后代
(2) 子元素选择器之间需要使用`>`符号连接,且选择器之间不能接有空格或其它符号.
(3) 子元素选择器不仅可以使用标签,还可以使用其它选择器,只要是能找到子元素的父元素的选择器都可以.
```
div>p{
    color:red;
}
// 或者
#stu>p{
    color:blue;
}
// 或者
.man>p{
    color:orange
}
// 等等...
```

- 说明 `div>ul>li>p` 的含义如下:
(1) 找到div 标签 (可能有多个)
(2) 找到div的亲儿子ul (可能有多个)
(3) 找到ul的亲儿子li (可能有多个)
(4) 找到li的亲儿子p并设置属性 (可能有多个)

- 子元素选择器可以通过`>`符号 一直延续下去



<br>
****
####七 后代选择器 和 子元素选择器

- 1 后代选择器和子元素选择器之间的区别?
(1) 后代选择器使用空格作为连接符号, 子元素选择器使用`>`作为连接符号.
(2) 后代选择器会选择所有的后代,而子元素选择器只会选择儿子.

- 2 后代选择器和子元素选择器的共同点
(1) 后代选择器和子元素选择器都可以使用各自的链接符号一直l连接下去
```
// 后代选择器
选择器1 选择器2 选择器3 选择器4 ... ...
// 子元素选择器
选择器1>选择器2>选择器3>选择器4> ... ...
```

- 3 在企业开发中如何选择




<br>
****
####八 交集选择器

- 1 什么是交集选择器?
给所有选择器选中的标签中, 相交的那部分标签设置属性.

- 2格式
```
选择器1选择器2{
    属性名:属性值;
}
```

- 3 注意点
(1) 选择器与选择器之间紧紧的挨在一起没有任何符号
(2) 选择器可以使用标签选择器,也可以使用id选择器,类选择器等
(3) 交集选择器在企业开发中用的并不多,仅作为了解就可以了.
```
// 表示选择平标签和.stu选择器的交集
p.stu{
    color:red;
}
```

- 4 应用场景
其实有这么一个应用场景,应为我们不同的标签可以使用相同的类,如果这是我们用标签选择器或者用类名选择器去设置对应的属性,其实都是不方便的, 这时我们就可以用 标签+类名组合的方式来 筛选出具体的标签并设置属性.
```
p.student.man{
    color:red;
}
//
p.student.girl{
    color:blue;
}
```
![](/assets/Snip20180828_5.png)











<br>
****
####八 交集选择器

- 1 什么是并集选择器?
给所有选择器选中的标签设置属性

- 2 格式
```
选择器1,选择器2,选择器3{
    属性名:属性值;
}
//比如
a,p,#identity,.girl{
    color:red;
}
```

- 3 注意点
(1)并集选择器必须使用`,` 号分开.

- 4 主要的应用场景
就是给不同的标签设置相同的属性







<br>
****
####九 兄弟选择器

##### 相邻兄弟选择器 CSS2

![](/assets/Snip20180828_8.png)
- 1 什么是相邻兄弟选择器
给指定选择器后面紧跟的那个选择器选中的标签设置属性.

- 2 格式
```
选择器1+选择器2{
    属性名:属性值;    
}
```
- 3 注意点:
(1) 相邻兄弟选择器,选择器之间必须用`+`号相连.
(2) 相邻兄弟选择器只能选择相邻的紧跟的标签

#####通用兄弟选择器 CSS3

![](/assets/Snip20180828_11.png)
- 1 什么是通用兄弟选择器?
给指定选择器后面的所有选择器选中的所有标签设置属性.

- 2 格式
```
选择器1~选择器2{
    属性名:属性值;
}
```

- 3 注意点:
(1) 通用兄弟选择器必须使用`~`相连
(2) 通用兄弟选择器选中的是指定选择器后面的某个选择器选中的所有的标签,无论有没有被隔开都可以选中





<br>
****
####十 序 选择器

CSS3 中新增的选择器中,最具代表性的就是序选择器

##### (1)同级别中的第几个 选择器( )

![](/assets/Snip20180828_15.png)
- 格式:
```
// 同级别第一个
标签选择器:first-child{
    color:red;
}
//同级别第几个
p:nth-child(1){
    color:blue;
}
// 比如:
p:first-child{
    color:red;
}
//他的工作原理是这样的
他会把当前网页中的不同的级别的标签的第一个标签都找出来, 然后看下第一个标签是否是p标签,如果是就设置对应的属性,也就是说先找出同级别的第几个,在判断是不是对应的类型.
```
- 注意点:
(1) `:first-child` 只管取出同级别的第一个,它不管类型, 取出后再根据前面的选择器来区分是否满足条件

##### (2)同级别中同类型的第几个 选择器( )

![](/assets/Snip20180828_20.png)

- 格式:
```
p:nth-of-type(1){
    color:red;
}
//他是这样运作的
(1) 找到所有的同级别的第几个
(2) 判断找到的这个标签是否是对应的类型,如果是就设置属性.
```


##### (4)同级别同类型的倒数第几个 选择器( )

- 格式:
```
p:nth-last-child(2){
    color:red;
}
```

##### (4)同级别中的倒数第几个 选择器( )

- 格式:
```
p:nth-last-of-type(2){
    color:red;
}
```

#####(5) 唯一子元素选择器

- 格式
```
p:only-child{
    属性名:属性值;
}
比如:
<body>
    <h1>我是镖标题</h1>
    <div>
        <p>我是段落</p>
    </div>
</body>
// 他是这样工作的
(1)找到只有一个子元素的标签中的只元素(这里就是p标签)
(2)检查这个唯一的子元素,是否是对应类型的元素,是就设置对应的属性
```




#####(6) 唯一类型子元素选择器

- 格式
```
p:only-o-type{
    属性名:属性值;
}
比如:
<body>
    <p>我是段落</p>
    <h1>我是镖标题</h1>
    <div>
        <p>我是段落</p>
    </div>
</body>
// 他是这样工作的
(1)找到所有的子标签,看这个子标签的类型是否是在当前标签内是唯一的类型
(2)如果这个唯一类型的标签是对应的标签类型,是就设置对应的属性
```



#####(7) 同级别奇数选择器, 同级别偶数选择器

- 格式:
```
// 同级别奇数选择器
p:nth-child(odd){
    color:red;
}
// 同级别偶数选择器
p:nth-child(even){
    color:red;
}
```

#####(8) 同级别同类型奇数选择器, 同级别同类型偶数选择器
- 格式:
```
// 同级别奇数选择器
p:nth-of-type(odd){
    color:red;
}
// 同级别偶数选择器
p:nth-of-type(even){
    color:red;
}

- 注意:
(1) 第几个还可以自定义 xn+Y
```
P:nth-child(2n+1){
    color:red;
}
// 或者
p:nth-of-type(3n+5){
    color:blue;
}
```

- 




<br>
****
####十一 属性 选择器


#####(1) 给设置了属性且属性名为xxx的标签统一设置样式
![](/assets/Snip20180828_24.png)

- 1 什么是属性选择器?
根据指定的属性名称找到对应的标签,然后设置属性.

- 格式:

```
// 给所有设置了id属性的p标签设置对应的属性
p[id]{
    color=red;
}
```
#####(2) 给设标签名为xxx且属性职位yyy的标签统一设置样式
![](/assets/Snip20180828_25.png)
 - 格式
 ```
 p[class=cc]{
     color:red;
 }
 ```
 
 - 最主要的应用场景:
 (1) 区分input标签的属性
 ```
 input[type=password]{
     color:red;
 }
 ```





<br>
****
####十二 通配符选择器

- 1 什么是通配符选择器?
给当前界面的所有标签设置属性值.

- 格式:
```
*{
    属性名:属性值;
}
```

- 注意点:
由于通配符选择器是设置界面上所有的标签的属性.所以在设置之前会遍历所有的标签,如果当前界面标签过多,那么性能就比较差,所以在企业开发中一般不会使用通配符选择器.












































法####CSS 选择器
- **标签选择器** --> (a、p...)
- **id选择器和类选择器** --> (#identity、.person)
- **后代选择器和子元素选择器** --> (选择器1 选择器2、选择器1>选择器2)
- **交集选择器和并集选择器** --> (选择器1选择器2、 选择器1,选择器2)
- **相邻兄弟选择器和通用兄弟选择器** --> (选择器1+选择器2、 选择器1~选择器2)
- **同级别第几个和同级别同类型第几个** --> (标签名:nth-child(1)、标签名:nth-of-type(2))
- **同级别倒数第几个,同级别同类型倒数第几个** --> (标签名:nth-last-child(2)、标签名:nth-last-of-type(2))
- **唯一子元素选择器和唯一类型子元素选择器** --> (p:only-child、 p:only-o-type)
- **属性名选择器, 属性值选择器** --> (标签名[属性名]、标签名[属性名=属性值])
- **通配符选择器**  --> (*)




<br>
****

####一 标签选择器
- 什么是标签选择器?
根据指定的标签名称,在当前的页面中找到所有该名称的标签,然后设置属性.

- 格式:
```
标签名称 {
    属性名:属性值;
}
// 注意点:  
(1) 标签选择器选择的是当前页面中的所有的标签,而不能单独选中某个标签
(2) 标签选择器,无论标签藏的有多深都能找到
(3) 只要是html中的标签, 都能作为标签选择器
```






<br>
****
####二 id 选择器
- 什么是id 选择器?
(1) 根据指定的id名称找到对应的标签,然后设置属性. 任何一个html 标签都有一个id属性.
(2) id 选择器是唯一的,一个页面中id的名称是不能重复的.

- 格式:
```
#id名称{
    属性名称: 属性值;
}
```
- 注意点:
(1) 每一个html 标签都有一个属性叫做`id`, 也就是说每个标签都可以设置`id`属性.
(2) 在一个界面中`id`的名称是不能重复的.
(3) 在编写id选择器时一定要在id的名称前面添加`#`号
(4) `id`的名称只能由字母 数字 下划线 组成.
(5) `id`的名称不能以数字开头,只能以字母和下划线开头
(6) `id` 的名称不能是html 中的标签名称
**(7) 在企业开发中一般情况下如果仅仅是为了设置样式,我们不会使用id, 因为在前端开发中 `id` 是留给`js` 使用的.**

- 
 
<br>
****
####三 类选择器

- 什么是类选择器?
类选择器就是通过指定的类名,找到指定的标签然后设置属性

- 格式:
```
.类名{
    属性名: 属性值;
}
// 一个类名
<p class="chengdu">我是段落</p>
// 二个类名
<p class="chengdu pixian">我是段落</p>
//错误写法
<p class="chengdu"  class="pixian">我是段落</p>
```

- 注意点:
(1) 每一个html 标签都有一个属性叫做`class`, 也就是说每个标签都可以设置`class`属性.
(2) 在一个界面中`class`的名称是 可以重复的.
(3) 在编写`class`选择器时一定要在`class`的名称前面添加`.`号
(4) `class`的名称只能由字母 数字 下划线 组成.
(5) `class`的名称不能以数字开头,只能以字母和下划线开头
(6) `class`的名称不能是html 中的标签名称
(7) 类选择器,就是专门用来给某一类标签设置样式的.










<br>
****
####四 id选择器和class选择器对比

- 1 id 相当于人的身份证,不可以重复. class 相当于人的名称可以重复.
- 2 一个html标签中只能绑定一个id选择器, 一个网页中id选择器的名称是不能重复的. 一个html标签可以绑定多个class 名称, 多个标签的class名称可以重复相同.
- 3 id选择器以`#`开头,class 选择器以 `.` 开头, id 选择器一般情况下是给js 使用的,所以除非特殊情况下不要使用id去设置样式.
- 4 在企业开发中一个开发人员对类的使用,可以看出开发水平.<br>
**一般情况下在企业开发中要注重冗余代码的抽取,可以将一些公共的代码抽取到一个类选择器中,然后让标签和这个类绑定即可.**

 






<br>
****
####五  后代选择器
![](/assets/Snip20180828_4.png)

- 什么是后代选择器
找到指定标签的所有后代标签,设置属性

- 格式:
```
标签名称1 后代标签名称{
    属性名: 属性值;
}
// 上面的含义是,先找到`标签名称1`选择器对应的所有的标签,
// 然后在这个标签里面去查找所有的 后代名称标签并设置属性
// 也可以这样
//
选择器1 选择器2 后代标签名称{
    属性名: 属性值;
}
//比如:
.man .ageLess20 p{
    color:red;
}
//注意: 后代不仅仅是儿子, 孙子 重孙子 ....只要是后代即可
``` 

- 注意点:
(1) 后代选择器必须用空格隔开,即 `选择器名称 后代标签`
(2) 后代选择器不仅仅可以使用标签选择器,还可以使用其它选择器, 其实后代选择器的工作原理是找到`指定标签`(父标签), 然后从`指定标签`(父标签) 里面的找出后代标签并设置其属性, 指定的标签具体怎么找到无所谓只要能找到即可.








<br>
****
####六  子元素选择器
- 什么是子元素选择器?
找到指定标签中所有特定的`直接子元素`,然后设置属性

- 格式:
```
标签名称1>标签名称2{
    属性名:属性值;
}
先找到标签名称1, 然后在这个标签中查找所有的直接子元素(儿子),然后再找出名称为 标签名称2 的元素(儿子)并设置属性. 
```

- 注意点:
(1) 子元素选择器只会查找儿子,不会查找其他后代
(2) 子元素选择器之间需要使用`>`符号连接,且选择器之间不能接有空格或其它符号.
(3) 子元素选择器不仅可以使用标签,还可以使用其它选择器,只要是能找到子元素的父元素的选择器都可以.
```
div>p{
    color:red;
}
// 或者
#stu>p{
    color:blue;
}
// 或者
.man>p{
    color:orange
}
// 等等...
```

- 说明 `div>ul>li>p` 的含义如下:
(1) 找到div 标签 (可能有多个)
(2) 找到div的亲儿子ul (可能有多个)
(3) 找到ul的亲儿子li (可能有多个)
(4) 找到li的亲儿子p并设置属性 (可能有多个)

- 子元素选择器可以通过`>`符号 一直延续下去



<br>
****
####七 后代选择器 和 子元素选择器

- 1 后代选择器和子元素选择器之间的区别?
(1) 后代选择器使用空格作为连接符号, 子元素选择器使用`>`作为连接符号.
(2) 后代选择器会选择所有的后代,而子元素选择器只会选择儿子.

- 2 后代选择器和子元素选择器的共同点
(1) 后代选择器和子元素选择器都可以使用各自的链接符号一直l连接下去
```
// 后代选择器
选择器1 选择器2 选择器3 选择器4 ... ...
// 子元素选择器
选择器1>选择器2>选择器3>选择器4> ... ...
```

- 3 在企业开发中如何选择




<br>
****
####八 交集选择器

- 1 什么是交集选择器?
给所有选择器选中的标签中, 相交的那部分标签设置属性.

- 2格式
```
选择器1选择器2{
    属性名:属性值;
}
```

- 3 注意点
(1) 选择器与选择器之间紧紧的挨在一起没有任何符号
(2) 选择器可以使用标签选择器,也可以使用id选择器,类选择器等
(3) 交集选择器在企业开发中用的并不多,仅作为了解就可以了.
```
// 表示选择平标签和.stu选择器的交集
p.stu{
    color:red;
}
```

- 4 应用场景
其实有这么一个应用场景,应为我们不同的标签可以使用相同的类,如果这是我们用标签选择器或者用类名选择器去设置对应的属性,其实都是不方便的, 这时我们就可以用 标签+类名组合的方式来 筛选出具体的标签并设置属性.
```
p.student.man{
    color:red;
}
//
p.student.girl{
    color:blue;
}
```
![](/assets/Snip20180828_5.png)











<br>
****
####八 交集选择器

- 1 什么是并集选择器?
给所有选择器选中的标签设置属性

- 2 格式
```
选择器1,选择器2,选择器3{
    属性名:属性值;
}
//比如
a,p,#identity,.girl{
    color:red;
}
```

- 3 注意点
(1)并集选择器必须使用`,` 号分开.

- 4 主要的应用场景
就是给不同的标签设置相同的属性







<br>
****
####九 兄弟选择器

##### 相邻兄弟选择器 CSS2

![](/assets/Snip20180828_8.png)
- 1 什么是相邻兄弟选择器
给指定选择器后面紧跟的那个选择器选中的标签设置属性.

- 2 格式
```
选择器1+选择器2{
    属性名:属性值;    
}
```
- 3 注意点:
(1) 相邻兄弟选择器,选择器之间必须用`+`号相连.
(2) 相邻兄弟选择器只能选择相邻的紧跟的标签

#####通用兄弟选择器 CSS3

![](/assets/Snip20180828_11.png)
- 1 什么是通用兄弟选择器?
给指定选择器后面的所有选择器选中的所有标签设置属性.

- 2 格式
```
选择器1~选择器2{
    属性名:属性值;
}
```

- 3 注意点:
(1) 通用兄弟选择器必须使用`~`相连
(2) 通用兄弟选择器选中的是指定选择器后面的某个选择器选中的所有的标签,无论有没有被隔开都可以选中





<br>
****
####十 序 选择器

CSS3 中新增的选择器中,最具代表性的就是序选择器

##### (1)同级别中的第几个 选择器( )

![](/assets/Snip20180828_15.png)
- 格式:
```
// 同级别第一个
标签选择器:first-child{
    color:red;
}
//同级别第几个
p:nth-child(1){
    color:blue;
}
// 比如:
p:first-child{
    color:red;
}
//他的工作原理是这样的
他会把当前网页中的不同的级别的标签的第一个标签都找出来, 然后看下第一个标签是否是p标签,如果是就设置对应的属性,也就是说先找出同级别的第几个,在判断是不是对应的类型.
```
- 注意点:
(1) `:first-child` 只管取出同级别的第一个,它不管类型, 取出后再根据前面的选择器来区分是否满足条件

##### (2)同级别中同类型的第几个 选择器( )

![](/assets/Snip20180828_20.png)

- 格式:
```
p:nth-of-type(1){
    color:red;
}
//他是这样运作的
(1) 找到所有的同级别的第几个
(2) 判断找到的这个标签是否是对应的类型,如果是就设置属性.
```


##### (4)同级别同类型的倒数第几个 选择器( )

- 格式:
```
p:nth-last-child(2){
    color:red;
}
```

##### (4)同级别中的倒数第几个 选择器( )

- 格式:
```
p:nth-last-of-type(2){
    color:red;
}
```

#####(5) 唯一子元素选择器

- 格式
```
p:only-child{
    属性名:属性值;
}
比如:
<body>
    <h1>我是镖标题</h1>
    <div>
        <p>我是段落</p>
    </div>
</body>
// 他是这样工作的
(1)找到只有一个子元素的标签中的只元素(这里就是p标签)
(2)检查这个唯一的子元素,是否是对应类型的元素,是就设置对应的属性
```




#####(6) 唯一类型子元素选择器

- 格式
```
p:only-o-type{
    属性名:属性值;
}
比如:
<body>
    <p>我是段落</p>
    <h1>我是镖标题</h1>
    <div>
        <p>我是段落</p>
    </div>
</body>
// 他是这样工作的
(1)找到所有的子标签,看这个子标签的类型是否是在当前标签内是唯一的类型
(2)如果这个唯一类型的标签是对应的标签类型,是就设置对应的属性
```



#####(7) 同级别奇数选择器, 同级别偶数选择器

- 格式:
```
// 同级别奇数选择器
p:nth-child(odd){
    color:red;
}
// 同级别偶数选择器
p:nth-child(even){
    color:red;
}
```

#####(8) 同级别同类型奇数选择器, 同级别同类型偶数选择器
- 格式:
```
// 同级别奇数选择器
p:nth-of-type(odd){
    color:red;
}
// 同级别偶数选择器
p:nth-of-type(even){
    color:red;
}

- 注意:
(1) 第几个还可以自定义 xn+Y
```
P:nth-child(2n+1){
    color:red;
}
// 或者
p:nth-of-type(3n+5){
    color:blue;
}
```

- 




<br>
****
####十一 属性 选择器


#####(1) 给设置了属性且属性名为xxx的标签统一设置样式
![](/assets/Snip20180828_24.png)

- 1 什么是属性选择器?
根据指定的属性名称找到对应的标签,然后设置属性.

- 格式:

```
// 给所有设置了id属性的p标签设置对应的属性
p[id]{
    color=red;
}
```
#####(2) 给设标签名为xxx且属性职位yyy的标签统一设置样式
![](/assets/Snip20180828_25.png)
 - 格式
 ```
 p[class=cc]{
     color:red;
 }
 ```
 
 - 最主要的应用场景:
 (1) 区分input标签的属性
 ```
 input[type=password]{
     color:red;
 }
 ```





<br>
****
####十二 通配符选择器

- 1 什么是通配符选择器?
给当前界面的所有标签设置属性值.

- 格式:
```
*{
    属性名:属性值;
}
```

- 注意点:
由于通配符选择器是设置界面上所有的标签的属性.所以在设置之前会遍历所有的标签,如果当前界面标签过多,那么性能就比较差,所以在企业开发中一般不会使用通配符选择器.











































