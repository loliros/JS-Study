JS数组的方法讲解

```
concat()
将两个数组合并成一个新的数组，源数组不会改变
返回值：合并好的新数组
参数：我们要合并的数组

slice()
基于当前数组获取指定区域元素并创建一个新的数组。源数组不变
参数：start开始获取区域的下标，end结束获取区域的下标(不包括end下标位置的那个元素)
返回值：指定区域元素生成的新数组

splice 可以完成删除，插入，替换操作
参数：参数1 截取的开始下标
    ：参数2 截取的长度
    ：参数3 在截取的开始下标位置，我们要插入的元素，插入的元素的个数随意。
    会对源数组进行修改
    返回值：被截取了的元素所组成的数组

join()
使用拼接符将数组中元素拼接成字符串
参数：拼接符
返回值：拼接好的字符串
```

```javascript
let arr = [1,2,3];
let arr1 = [4,5,6];
//concat
let arr2  = arr.concat(arr1);
//alert(arr2);//1,2,3,4,5,6

//slice
let arr3 = arr2.slice(1,3);
//alert(arr3);//2,3

//splice删除
let arr4 = arr2.splice(1,2);
//alert(arr2);//1,4,5,6
//alert(arr4);//2,3

//splice插入
arr2.splice(1,0,2,3);//因为没有截取长度 所以返回值是一个空的数组
//alert(arr2);//1,2,3,4,5,6

//splice替换 先删除 再添加
arr2.splice(1,1,10);
alert(arr2);//1,10,3,4,5,6
let arr5 = arr.join("");
alert(arr5);//123
```