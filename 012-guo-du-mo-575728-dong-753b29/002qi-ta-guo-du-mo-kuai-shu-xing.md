#### 其它过渡模块属性

1  `transition-delay: 2s;` 设置过渡动画的执行时间, 需不需要延时
2 `transition-timing-function: linear;` 设置过渡动画的效果, 开始块, 结束块, 匀速, 开始结束快, 开始结束慢等
![](/assets/过渡曲线.png)


```
div{
  width: 50px;
  height: 20px;
  background-color: red;

  /*告诉系统那个属性需要执行,过渡效果*/
  transition-property: width, height,background-color;
  transition-duration: 1s;

  transition-delay: 2s;
  /*设置过渡动画的效果  */
  transition-timing-function: linear;

}

div:hover{
  width: 100px;
  height: 50px;
  background-color:purple;
}

```
                
