#### JS字符串的查找方法

```
indexOf()
字符串.indexOf(子串，开始查找的位置);
返回值：如果在字符串中查找到了子串第一次出现的位置，返回子串出现的位置
否则则返回-1（没有查找到的意思）

lastIndexOf()
字符串.lastindexOf(子串)
返回值：子串在字符串中最后一次出现的位置，如果没有，返回-1

search()
参数可以是正则表达式
“abc" /abc/ig
正则表达式可以t添加修饰符，i代表忽略大小写，g代表q全局匹配
```

```javascript
//indexOf（）
let str = 'ateabcabcabc';
alert(str.indexOf("abc"));//3

//lastIndexOf()
alert(str.lastIndexOf('abc'));//9

//search()
let arr = 'ABSREWGsdwqczAbs';
alert(arr.search('abs'));//-1
alert(arr.search(/abs/i));
```