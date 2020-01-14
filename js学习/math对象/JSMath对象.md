#### JSMath对象

```
Math对象用于执行数学计算
Math常用的属性 Math.PI约等于3.14159

Math对象常用的函数:
Math.round()四舍五入
Math.random()随机0~1之间的随机数
Math.max()返回较大数
Math.min()返回较小数
Math.abs()返回当前的数的绝对值
Math.ceil()向上取整
Math.floor()向下取整
Math.pow(x,y)求x的y次方 x是底数 y是指数
Math.sqrt()计算开平方


计算机计算小数的时候容易出错
Math对象的勾股函数
参数:都应该是弧度 Math.PI = 180弧度
1弧度 = Math.PI/180;
Math.sin()/cos()/tan() 正弦/余弦/正切
```

```javascript
alert(Math.round(3.5));//4
alert(Math.random());//0~1之间的随机小数
alert(Math.max(10,20,30));//30
alert(Math.min(10,20,30));//10
alert(Math.abs(-5));//5
alert(Math.ceil(0.1));//1
alert(Math.floor(0.9));//0
alert(Math.pow(2,5));//2的5次方=32
alert(Math.sqrt(4));//输出2
alert(Math.sin(30 * Math.PI / 180));//0.49999999999999994 正确应该输出0.5
alert(Math.cos(60 * Math.PI / 180));//0.5000000000000001 正确应该输出0.5
```