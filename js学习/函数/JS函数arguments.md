#### JS函数arguments

```
计算所有传入参数的和。具体传入多少参数不确定。
            arguments：
                在每一个函数的内部都有一个内置的数组，是一个变量，叫做arguments
                arguments可以存储当前函数传入的所有参数，而且是通过传参的顺序进行排列

            arguments.length    输出传入参数的个数
            访问arguments里面的数据，需要通过对应的房间号/下标进行访问
            下标可以配合循环去使用
```

```javascript
function sum(){
    //alert(arguments);//[object Arguments]
    let sum = 0;
    for (let i = 0;i<arguments.length;i++){
        sum = sum + arguments[i];
    }
    alert(sum);
}

sum(3,4,5);
```