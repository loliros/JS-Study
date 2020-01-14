#### JS字符串的方法

```
sub()把字符串显示为上标

sup()把字符串显示为下标

link()把字符串显示为链接

fontsize()使用指定尺寸来显示字符串

fontcolor()使用指定颜色来显示字符串

strike()使用删除线来显示字符串

fixed()以打印机文本来显示字符串

bold()使用粗体显示字符串

blink()显示闪动字符串

big()用大号字体显示字符串

在document.write()中使用

charCodeAt()
字符串.charCodeAt(下标)
返回值：返回字符串中对应下标字符的ASCII码值

String.fromCharCode();
String.fromCharCode(ASCII码值)
参数：ASCII码值，个数任意
返回值：ASCII码值对应字符组成的字符串

concat()
字符串.concat()
返回值：拼接成的字符串,对源字符串没有影响
一般情况下很少用 都是用+号来进行字符串的拼接
```

```javascript
//sub()
document.write("啦啦啦" + "hello".sub() + '<br>');
let str = "1";
document.write("啦啦啦" + str.sub()+ '<br>');

//sup()
document.write("啦啦啦" + "hello".sup() + '<br>');

//fixed()
document.write("啦啦啦".fixed() + "<br>");

//blink()
document.write("啦啦啦".blink() + '<br>');

//link()
document.write("啦啦啦".link('https://www.bilibili.com/') + '<br>');

//charCodeAt()
let arr = 'hello';
alert(arr.charCodeAt(1));//101;

//String.fromCharCode()
let str1 = String.fromCharCode(97,98,99)
alert(str1);//abc

//concat()
let str2 = 'hellow';
let str3 = 'world';
let arr1 = str2.concat(str3);
alert(arr1);
```