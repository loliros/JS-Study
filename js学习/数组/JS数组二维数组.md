#### JS数组二维数组

```
通过循环按行顺序为一个5x5的二维数组a赋1到25的自然数，然后输出该数组的左下半三角。
1,  2,  3,  4,  5
6,  7,  8,  9,  10
11, 12, 13, 14, 15
16, 17, 18, 19, 20
21, 22, 23, 24, 25

所谓的二维数组 就是在数组中还有数组
```

```javascript
let count = 0;
let arr = [];
for (let i=0;i<5;i++){
    let newArry = [];
    for (let j=0;j<5;j++){
        newArry.push(++count);
    }
    arr.push(newArry);
}
alert(arr);//输出1~25
alert(arr[0][0]);//输出1 这么写的意思是获取arr数组中第一个数组的第一个元素 由此可知
for (let i=0;i<5;i++){//用来换行
    for (let j=0;j<=i;j++){//用来打印每一行需要显示的数据
        document.write(arr[i][j]+" ");
    }
        document.write('<br>');
}
```