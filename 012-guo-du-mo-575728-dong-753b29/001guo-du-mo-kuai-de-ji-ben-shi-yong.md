#### 过度模块的基本使用

`:hover` 伪类选择器除了可以在 `a 标签` 上使用也可以在其他标签上使用.


#### 过渡效果三要素
1 必须要有属性发生变化
2 必须要告诉标签(元素)那个属性要变化
3 必须要告诉标签(元素)过渡执行的时长

单个属性要过渡效果的实现方式
```
 div{
    width: 100px;
    height: 50px;
    background-color: red;
    
    /*告诉系统那个属性需要执行过渡效果*/
    transition-property: width; 
    /*高度系统过渡效果要执行的时长*/
    transition-duration: 1s;  
}

/*触发过渡效果*/
div:hover{
    width: 200px; 
}
```


如果有多个属性要执行过渡效果,就这样执行
```
 div{
    width: 100px;
    height: 50px;
    background-color: red;
    
    /*告诉系统那  些属性需要执行过渡效果*/
    transition-property: width, height; 
    /*告诉系统 哪个过渡效 要执行多长的时长*/
    transition-duration: 1s,2s;  
}

/*触发过渡效果*/
div:hover{
    width: 200px; 
    height:300px;
}
```

注意点:
如果有多个属性需要过渡, 那么多个属性之间使用逗号隔开
```
多个属性需要过渡
transition-property: width, height; 
```
如果要设置各个过渡属性的过度时长, 那过度时间使用逗号隔开,顺序一致即可.
```
多个属性需要各自的过度时长
transition-property: width, height; 
按顺序与过度属性对应
```



