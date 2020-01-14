#### JS有参函数

```javascript
//输出n个hello world
        /*
        * 不知道输出多少个
        * 可以把函数中不确定的值当作形参（形式上的参数）进行声明
        *
        * 有参函数的封装过程：
        * function 函数名（形参）{
        *   函数体;
        * }
        * */
function print(num) {//num为形参
    for (let i=0;i<num;i++){
        document.write('hello world!');
    }
}

print(10);//10为实参 num为形参 实参给形参赋值
```