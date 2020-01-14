#### JS数组系统排序

```
系统提供的排序方法
reverse() 逆向排序

sort()
将数组中的元素升序排序
注意：sort默认按照字符串进行排序

需求：一般情况下需要自己编写排序算法，系统提供给的排序函数，用得比较少
```

```javascript
//reverse()
let arr = [1,2,3,4,5];
arr.reverse();
alert(arr);//5,4,3,2,1

//sort()
arr.sort();
alert(arr);//1,2,3,4,5
let arr1 = [10,1,5,15];
arr1.sort();
alert(arr1);//1,10,15,5
```