#### JS字符串分割

```
replace()
字符串.replace(匹配的字符串/正则表达式,替换成新字符串)
返回值：替换完成以后生成的新字符串。

想替换所有符合条件的字符串，就必须使用正则表达式完成

substring()
字符串.substring(start,end);
作用:字符串提取，在指定范围内，提取字符串，生成新字符串
返回值：生成的新字符串。不包含j结束位置的（与数组的元素的提取一样）

 split()
 字符串.split(分割符,生成的数组的长度)
 返回值:通过分割符，分割成的装有子串的数组
 分割符是分割整体
 分割符会割出空字符串
 如果分割符是空字符"",那么我们字符串会分割成单个字符
 字符串=>数组通过split完成 数组=>字符串通过join完成

 toLowerCase()用于把字符串转换成小写
 toUpperCase()用于把字符串转换成大写
```

```javascript
//replace()当str里面有两个are时只能替换第一个are
let str = 'how are are you';
//alert(str.replace('are','old are'));
alert(str.replace(/are/g,'old are'));

//substring()
alert(str.substring(2,5));//w a

//split（）
let arr = str.split(' ');
alert(arr);//how,are,are,you
let arr1 = str.split(' ',2);
alert(arr1);//how,are

let str1 = 'how  are are you';
//let str2 = str1.split("  ");//how,are are you
//let str2 = str1.split(" ");//how,,are,are,you
let str2 = str1.split("");//h,o,w, , ,a,r,e, ,a,r,e, ,y,o,u
alert(str2);
```