#### 过渡效果的连写

1、 过渡属性主要有以下4个

```
transition-property:width , height; // 指明(告诉)元素,需要做过渡效果的属性, 多个属性之间使用逗号分隔.

transition-duration: 1s, 2s;  // 指明对应需要过渡的属性的过度时长.

transition:delay: 1s, 2s; // 指明对应需要过渡的属性 开始执行的时间, 是否需要延时

transition-timing-function: linear, ease-in; // 过渡的动画效果
```


2、过渡效果的连写,格式下:

```
transition: property, duration, timing-function,delay;

如果有多个属性需要连写,可以这样
transition: width 1s linear 0s,backgroundColor 1s linear 0s ;

多个过渡属性之间使用逗号隔开
```


3、连写的注意点;
(1)、其实连写的属性里面,保证有 属性 和 动画时间即可, 后面的属性可以省略
```
比如: 
transition:width 1s;
```
(2)、如果有很多属性要过度,也可以这样写
```
transition: all 1s;
这样在触发的时候, 要过度那些属性就 修改即可
```
