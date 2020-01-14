JS字符串的概念

```
字符串的概念
JS中将所有单引号或者双引号括起来的都叫做字符串

字符串创建的方法：
1、通过new运算符创建
2、省略new
3、通过常量创建字符串

字符串的属性
length 返回的是当前字符串中字符的个数

charAt()
字符串.charAt(下标)
返回值：对应下标的字符
可以直接通过字符下标去访问该字符

ECMAScript中的字符串是不可改变的，也就是说，字符串一旦创建，它们的值就不能改变。
要改变某个变量保存的字符串，首先要销毁掉原来的字符串，然后再用另一个包含新值的字符串填充该变量
```

```javascript
//1、
let str = new String("hellow world!");
alert(typeof str);//输出object object是复合数据类型
alert(str);

//2、
let str1 = String(true);
alert(typeof str1);
alert(str1);

//3、
let str2 = "hello";
alert(str2);

//字符串的属性
alert(str.length);
alert(str.charAt(1));
alert(str[1]);//与上面的一样的意思

//注意事项
let num = "啦啦啦";
num[1] = "1";
alert(num);//输出啦啦啦 无法修改
num = "1啦啦";
alert(num);//输出1啦啦
```