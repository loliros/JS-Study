#### ecma5新增的数组方法

```
indexOf() 数组
数组.indexOf(元素,开始查找的位置);（与字符串的方法一样）
返回值：如果在字符串中查找到了元素第一次出现的位置，返回元素出现的位置
否则则返回-1（没有查找到的意思）

foreach()
遍历数组
数组.foreach(function(item,index,array){
    item 当前遍历到得元素 index 当前遍历到得下标 array当前遍历到得数组
})


map的方法是映射 操作过程是遍历->操作->返回

reduce 归并
数组.reduce(function(pre,next,index,array){
    pre 上一次遍历return后所得到的值
    next 当前遍历到的元素
});

filter 过滤
数组.filter(function(item,index,array){

})

some 某些 用来判断return后面的条件是否成立，如果成立返回true，否则返回false
some不会从头到尾都遍历一遍，如果匹配成功一次，就会返回true，剩下的就不会进行遍历了
否则则全部遍历 显示false

every 使用方式跟some一样，但是要求每一项都符合，才返回true，有一项不符合就返回false
如果判断有元素不符合条件则直接返回false 终止循环
```

```javascript
//indexOf()
let arr = ['啦啦啦','啦啦','啦啦啦'];
let arr1 = arr.indexOf('啦啦啦',1);
//alert(arr1);

//forEach()
arr.forEach(function (item,index,array) {
    //document.write(item + "," + index + "," + array + "<br>");
});
//arr.forEach(alert);//也可以这么遍历数组

//map()
let arr2 = arr.map(function (item,index,array) {
    return item;
})
//alert(arr2);

//reduce()
let arr3 = arr.reduce(function (pre,next,index,array) {
    document.write(pre + "," + next + '<br>');//第一个遍历pre返回啦啦啦,next是啦啦,则下一次遍历 pre是啦啦啦啦啦，next是啦啦啦
    return pre + next;
})
//document.write(arr3);//把数组的元素合并起来 如果是数字则相加起来 如果是字符串则合并起来

//filter()
let arr4 = [10,20,30,40,50];
let arr5 = arr4.filter(function (item,index,array) {
    return item>30;//输出能大于30的元素
})
//alert(arr5);

let str = arr4.some(function (item,index,array) {
    return item>50;//false 数组里面没有大于50的元素
    //判断return后面的表达式，在当前数组是否成立，如果成立则返回true,否则false
})
//alert(str);

str = arr4.every(function (item,index,array) {
    return item>=10;
})
alert(str);//true
```