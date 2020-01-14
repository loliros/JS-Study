JSBOM的location方法

```
            assign() 跳转到指定url

            reload() 重载当前的url
            如果传参，参数为true的时候，强制加载，从服务器的源头重新进行加载
            加载浏览器的时候，浏览器会给一些数据进行缓存
            如果强制加载则会忽略掉缓存，重新加载

            replace() 用新的Url替换当前页面，可以避免产生跳转前的历史记录
```

```javascript
window.onload = function () {
    let oBtn = document.getElementById('btn');
    oBtn.onclick = function () {
        location.assign('http://www.baidu.com');
        location.reload();
        location.replace('http://www.baidu.com')
    }
}
```

```html
<input type="button" value="按钮" id="btn">
```