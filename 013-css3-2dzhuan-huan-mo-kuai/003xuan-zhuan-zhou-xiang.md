#### 旋转轴向



![](/assets/zbx.png)

1、 围绕Z轴旋转 (2种写法)
```
li:nth-child(1){
    transform:rotate(45deg); // 默认情况下, 旋转就是围绕Z轴旋转
    //
    transform:rotateZ(45deg); // 围绕Z轴旋转
}
```
![](/assets/ratateZ.png)


2、围绕X轴旋转

```
li:nth-child(2){
    transform: rotateX(30deg);
}
```
![](/assets/rotateX.png)


3、围绕Y轴旋转
```
li:nth-child(3){
    transform:rotateY(45deg);
}
```
![](/assets/rotateY.png)
