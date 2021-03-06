####CSS 3 大特性



****
<br>
####一 CSS 的继承性 (color,font,text,line 开头属性)

- 1 什么是继承性?
给父元素设置一些属性,子元素也可以使用,这个特性我们就称为继承特性.

- **注意点:**
(1) 并不是所有的属性都可以继承,只有以 `color`, `font`,`text`, `line` 开头的属性才可以继承.我们可以通过谷歌开发者工具来验证和检查某个元素的某个属性是不是继承来的,以及从哪个标签继承来的.
![](/assets/Snip20180829_13.png)
检查其他的属性依次类推,当你在布局时发现了错误就可以这样来检查.
(2) 在CSS的继承中,不仅仅是儿子可以继承,只要是后代都可以继承
![](/assets/Snip20180829_17.png)
**(3) a 标签的文字颜色和下划线是不会继承父标签的样式, 也就是说a标签的文字颜色和下滑线不会因为继承而发生变化.
(4) h 标签的文字大小是不能继承的,即h标签的文字大小不会受继承的影响而变化.(但是, h标签的文字和父标签的文字的大小是有倍数关系)**




****
<br>
####二 CSS 的层叠性

- 1 什么是CSS 的层叠性?
层叠性就是CSS 处理冲突的一种能力

- 2 注意点:
层叠性只有在多个选择器,选择了同一个标签且设置了相同的属性才会生效(层叠)**(注意: 并不是后写的就一定会把先写的层叠掉)**




****
<br>
####三 CSS 的优先级

- 1.什么是CSS的优先级?
当多个选择器选中同一个标签,并且给同一个标签设置了相同的属性时,如何层叠就由优先级来确定.优先级高的会把优先级低的层叠掉.

- **优先级的3种方式:**(是否是直接选中,是否是相同的选择器, 不同选择器直接选中  )<br>
(1)   **是否是直接选中(间接选中指的就是继承)**
如果是间接选中,那么就是谁离目标标签近就听谁的.
```
div{
   color: red;
}
ul{
    color: green;
}
li{
    color: blue;
}
//间接选中, li 离得最近听li的
<div>
    <ul>
        <li>
            <p>我是段落</p>
        </li>
    </ul>
</div>
```
(2) **是否是相同的选择器,谁写在后面就听谁的**
```
相同选择器,后面的层叠掉前面的.
p{
    color:red;
}
p{
    color:blue;
}
// 或者
.person{
    color:orange;
}
.person{
    color:red;    
}
```
(3) 如果都是直接选中,并且不是相同类型的选择器,那么就会按照选择器的优先级来层叠.<br>
**id>类>标签>通配符>继承>浏览器默认**
```
#identity{
    color: pink;
}
//
.man{
    color: cyan;
}
//
p{
    color: orange;
}
//
*{
    color: blue;
}
//
div{
    color: red;
}
//
//
<div>
    <p id="identity" class="man">我是段落</p>
</div>
```

- 




##### CSS 优先级提升(important)

- 1 什么是important?
用于提升某个直接选中的标签的选择器的某个属性的优先级,可以将被指定的属性的优先级提升为最高.

- 2 注意点:
(1) important 只能用于直接选中,不能用于间接选中.
(2) !important只能提升被指定的属性的优先级,其他的熟悉经的优先级不会被提升.
(3) `!important` 必须写在属性值之后, `;`分号之前.
```
 p{
     // 将p标签选中的color 属性设置为最高
    color: orange !important;
    font-size:30px; // 这个属性不能被提升
 }
 
 *{
     // 将所有标签选中的color 属性设置为最高
     color: orange !important;
     // 注意通配符,选中的标签也是直接选中的.
 }
```






****
<br>
####四 CSS 优先级的权重问题

- 什么是优先级的权重?
当多个选择器混合在一起使用时, 我们可以通过计算权重来判断谁的优先级最高.

- 权重的计算规则  
(1) 首先计算选择器中有几个id 选择器,id 选择器多的有线级最高.
(2) 如果id选择器的个数一样,那么在看类名,类名个数多的,优先级最高.
(3) 如果类名的个数一样,那么再看标签名称个数,标签名称个数多的优先级最高.
(4) 如果id个数一样,类名个数一样,标签名称个数也一样,就不会往下计算了, 谁写在后面听谁的.

- **注意点:**
(1) 权重只有在直接选中的情况下才会有效.
(2) 在权重计算中,通配符是不参与权重计算的,统配符的权重是0.

















































