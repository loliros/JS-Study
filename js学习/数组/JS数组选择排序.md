#### JS数组选择排序

```
选择排序法
通过比较首先选出最小的数放在第一个位置上，然后在其余的数中选择次小数放在第二个位置，以此类推，直到所有的数成为有序序列
9,8,7,6,5,4
打擂台法
```

```javascript
let arr = [9,8,7,6,5,4];
for (let i=0;i<arr.length-1;i++){
    for (let j=i+1;j<arr.length;j++){
        if (arr[i]>arr[j]){
            let tmp = arr[i];
            arr[i] = arr[j];
            arr[j] = tmp;
            document.write(arr + '<br>');
        }
    }
}

document.write(arr);
```