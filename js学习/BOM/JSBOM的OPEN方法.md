#### JSBOM的OPEN方法

```
window.open()
1、要加载URL
2、窗口的名称或者窗口的目标
3、一串具有特殊意义的字符串
```

```javascript
window.onload = function () {
    let oBtn = document.getElementById('btn');
    oBtn.onclick = function () {
        //open('http://www.baidu.com');
        //只有第一个参数的时候，调用open方法会打开新的窗口，加载url
        open('http://www.baidu.com','百度','width=200,height=200,top=200,left=200');
        //第二个参数，是给打开的新窗口一个名字，然后以后，再加载url，就再这个已经起好
        //名字的目标窗口加载url
        //第三个参数是新窗口的设置，比如宽高之类的
    }
}
```

```html
<input type="button" value="按钮" id="btn">
```