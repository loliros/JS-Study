#### JS数组属性和遍历

```
数组元素的访问和赋值，都是通过数组的下标完成
下标就是索引，即元素的序号，从0开始，下标最大值是数组的长度-1
下标可以是变量或表达式

数组可以通过循环来遍历

for...in进行快速遍历
for(let 变量 in 数组){}
将数组里面的元素全部遍历一遍
循环效率比for高
```

```javascript
let arr = [];
for (let i=0;i<10;i++){
    arr[i] = Math.random();//循环随机输出0~1之间的任意数数
}
alert(arr);
let arr = [10,20,30,40];
for(let i in arr){
    document.write(arr[i] + '<br>');
}
```