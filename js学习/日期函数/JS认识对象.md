#### JS认识对象

```
对象是引用数据类型

对象里面可以存储数据和函数

对象用于将数据和功能组织在一起

对象的创建
1、使用new运算符
对象中存储的数据，叫做对象的属性
对象中存储的函数，叫做对象的方法

2、new运算符可以省略

3、使用常量/自变量去创建对象
let person = {};
person.name = '啦啦啦';
person['name'] = '啦啦啦;
person.age = 18;
person.showName = function(){
    alert(person.name);
    alert(person['name']);
}

person["showName"] = function(){
    alert(person.name);
    alert(person['name']);
}

可以用过delete删除对象的属性
如delete person.name;

声明函数
function show(){}
可以写成
let show = function(){}
等号右边因为没有名字可以称之为匿名函数

函数是复合数据类型
所有函数名相当于函数所在的地址
```

```javascript
//使用new运算符
import person from "../../VUE/TestVue/webpack";

let porson = new Object();
//给对象添加属性
porson.name = '啦啦啦';
delete porson.name;//删除对象的属性
porson.age = 18;
//给对象添加函数
porson.showName = function(){
    alert(porson.name);
}
//想要访问上述对象的属性和函数
//alert(porson.name);
//调用对象的方法
//person.showName();
```