####一 CSS 文字属性
- 1 **规定文字样式的属性** `font-style`
    ```
    p{
        // 字体样式属性,常用属性值2个
        font-style: italic; // 倾斜的
        font-style: normal; // 正常的
    }
    // 快捷键
    fs --> font-style: italic;
    fsn --> font-style: normal;
    ```

- 2 **规定文字粗细的属性** `font-weight`

    ```
    p{
       // 字体粗细属性,除了下面四个常用的属性还有可以通过 数字来设置具体的粗细
        font-weight: lighter;
        font-weight: normal;
        font-weight: bold;
        font-weight: bolder;
        font-weight: 100; // 通过具体数字设置 字体的粗细
    }  
    // 快捷键
    fwl -->  font-weight: lighter;  
    fwn -->  font-weight: normal;
    fwb -->  font-weight: bold;
    fwbr -->  font-weight: bolder;
    fw300 -->  font-weight: 300;   // 数值在100~900 之间 取整百
    ```

- 3 **规定文字大小的属性** `font-size`

    ```
    p{
    // 格式:
    font-size: 30px; 
    // 注意: 通过font-size设置大小一定要带单位px
    
    //快捷键
    fz --> font-size: 30px; 
    fz30 -->  font-size: 30px; 
    }
    ```

- 4 **规定文字字体的属性**`font-family`

    ```
    p {
        // 默认就是宋体,在以后的开发中用的最多的也是宋体
        font-family:"宋体";
        // 快捷键 
        ff -->  font-family:
        // 注意点: 
        (1)如果取值是中文,那么需要使用双引号`""` 或者单引号`''` 将字体括起你.
        (2)设置的字体必须是用户电脑里面包含的字体
        
    }
    ```
    



<br>
****
####二 字体属性(字体名字)补充
- 1 如果设置的字体不存在,那么系统使用默认的字体来替代, 中文默认是 `宋体`

- 2 如果设置的字体不存在,而我们又不想使用默认的字体
```
// 前面没有就用后面的
font-family:"字体1","备选字体1","备选字体2";
```

- 3 中文和英文单独设置字体
```
特点:
(1)但凡是中文字体,里面都包含了英文字体
(2)但凡是英文字体,里面都没包含中文字体
// 中文和英文设置不同的字体
font-family:"英文字体","中文字体";
// 注意点:
如果给界面中的英文单独设置字体,那么英文必须写在中文的前面
```

- 4 在企业开发中常见的字体主要有:
```
中文: 宋体(英文名: SimSun)/黑体(英文名: SimHei)/微软雅黑(英文名: Microsoft YaHei)
英文: Times New Roman/ Arial(一般这两个在浏览器中都有)
注意点: 并不是英文名称,就一定是英文的字体,中文字体都有对应的英文名
```


<br>
****
####三 文字属性的缩写

- 字体属性连写(缩写)格式
```
 p {
    /*字体属性缩写格式
    注意点:
    (1) 在这种缩写格式中有的属性可以省略(字体样式style(italic),字体粗细weight(blod)),
    有的属性还可以交换位置(字体样式style(italic),字体粗细weight(blod)).
    (2) 在这种缩写格式中有的属性是不能省略的(字体大小size(10px),字体名称family(宋体))
    (3) 有些属性的位置是不能修改的, 字体样式style(italic),字体粗细weight(blod) 必须写在字体大小size 的前面,且字体大小必须写在字体名称的前面
    */
    font: italic bold 10px "楷体";
}
```

<br>
****
####四 文字属性 

- 1 文本装饰的属性 `text-decoration`(下划线,删除线)
![](/assets/Snip20180827_1.png)
```
常用取值:
text-decoration: overline; //上划线
text-decoration: underline;// 下划线
text-decoration: line-through; // 删除线
text-decoration: none; // 默认就是这个
// 快捷键:
td -->  text-decoration:
tdu --> text-decoration: underline;
tdl --> text-decoration: line-through;
tdn -->text-decoration: none;
```
**说明: **<br>
虽然 `text-decoration: none;` 是文字默认的取值,但是`text-decoration: none;` 我们用的是很多的,**最主要的用途就是去除 `a标签`的下划线**
```
a{
    text-decoration: none;
}
<a href="#">我是超链接</a>
```


<br><br>
- 2 文本水平对齐的属性`text-align`
```
tac --> text-align: center;
tal --> text-align: left;
tar --> text-align: right;
```

<br><br>
- 3 文本缩进的属性` text-indent`
```
//
text-indent: 2em;
// em 是单位,1个em 代表1个文字的宽度
// 也可以使用像素
text-indent: 200px; // 缩进200个像素
```


<br>
****
####五 文字的颜色属性 
```
格式:
color: red;
color: #ffffff;
color: #fff;
color: rgb(255,255,255);
color: rgba(255,255,255,1);
```





    
