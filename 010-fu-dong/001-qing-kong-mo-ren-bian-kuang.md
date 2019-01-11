#### 清空默认边框

1、 为什么要清空默认边距(外边距和内边距)

在企业开发中, 为了更好的控制盒子的宽高和计算盒子的宽高等等.所以在企业开发中,编写代码前的第一件事就是清空默认的边距



2、如何清空默认的边距
```
*{
    margin : 0px;
    padding : 0px;
}

这种通配符选择器, 来清空默认的边距, 因为会遍历所有的标签, 所以性能要差一些
```

性能更高一点的做法
```
body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,textarea,p,blockquote,th,td{
    margin:0;padding:0
}
```

百度`yui css reset` 可以找到解决方法
