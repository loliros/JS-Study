#### JSBOM的search处理

```
封装函数解析search
?id=5&search=ok
获取url中search,通过传入对应key，返回对应的value。
例子 传入id 返回5
```

```javascript
function getValue(search,key) {
    //1、获取key的下标
    let str = search.indexOf(key);
    if (str === -1){
        return null;
    }else{
        //2、找出键值对，结束的位置
        let end = search.indexOf('&',str);
        if (end === -1){
            //最后一个键值对
            end = search.length;
        }
        //3、将键值对提取出来
        let str1 = search.substring(str,end);
        //4、key=value 获取value
        alert(str1);
        let str2 = str1.split('=');
        for (let i=0;i<str2.length;i++){
            alert(str2[i]);//str2 = ['id',5];
        }
        alert(str2[1]);
    }
}
let search = '?id=5&search=ok';
getValue(search,'id');
```