#### ecma5严格模式

```
ECMA标准 ECMAJavascript

ECMA5 第五版

严格模式
会让浏览器对js的要求更加苛刻

严格模式通过use strict来进行声明的
use strict写在哪个作用域下，这个作用域下就会严格遵从严格模式
不要轻易在全局范围内增加use strict;
建议在作用域内使用
```

```javascript
function m1(){
    max = 10;
    //如果在给变量赋值的时候，没有声明该变量，那么这个变量会进行全局变量来处理
}
m1();
alert(max);

function m2() {
    "use strict";
    let max = 10;//不进行max的声明，会报错
}
m2();
alert(max);
```