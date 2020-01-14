#### JSBOM的history对象

```
history是window对象的属性，它的作用是保存这个用户上网的记录（历史记录）

属性
history.length 返回当前history对象中记录数
历史记录的条数

方法
history.back()  返回上一条历史记录
history.forward() 前进到下一条历史记录
history.go()
参数：0重载当前页面
    正数 前进对应数量的记录
    负数 后退对应数量的记录
```

```javascript
window.onload = function () {
    let oBtn = document.getElementById('btn');
    let backBtn = document.getElementById('backBtn');
    let advance = document.getElementById('advance');
    let go = document.getElementById('go');
    let num = history.length;
    oBtn.onclick = function () {
        alert(history.length);//修改url进行加载的时候会增加历史记录
    };
    backBtn.onclick = function () {
        history.back();
    };
    advance.onclick = function () {
        history.forward();
    };
    go.onclick = function () {
        //history.go(-num + 1);第一条记录
        //history.go(num - 1);最后一条记录
        history.go(0);
    };
}
```

```html
<input type="button" value="记录" id="btn">
<input type="button" value="返回上一条历史记录" id="backBtn">
<input type="button" value="前进到下一条历史记录" id="advance">
<input type="button" value="go" id="go">
```

