#### JS数组栈方法和队列方法

```
 栈结构：从一个口进从同一个口出（先进后出）
 push()
 给数组末尾添加元素
 参数：我们要添加的元素，参数个数随意
 返回值是数组的长度

 pop()
 数组.pop()
 移除数组末尾的元素
 返回值：移除的元素
```

```javascript
let arr = [1,2,3,4,6,7,8];
let res = arr.push(10);
alert(arr);
alert(res);

let arr1 = [1,2,3,4];
let res1 = arr1.pop();//使用一次移除一次
alert(res1);//4
alert(arr1);//1,2,3
```

```
 队列结构
 从一头进从另一头出（先进先出）
 push()进入
 shift()出去
 从数组的头部去下一个元素
 返回值是取下的元素

 unshift()
 数组.unshift()
 从数组的头部插入元素
 参数：我们插入数组的元素（参数的个数）随意
 返回值：数组的长度
```

```javascript
let num = [1,2,3,4,5];
let num1 = num.push(10);
let num2 = num.shift();
alert(num);//2,3,4,5,10
alert(num1);//6
alert(num2);//1
```