#### JSBOM的opener方法的使用

sup页面

opener 打开当前窗口的父窗口的window对象

IE不支持

```css
body{
    background: red;
}
```

```javascript
window.onload = function () {
    let oBtn = document.getElementById('btn');
    oBtn.onclick = function () {
        opener.document.write('子窗口点击输出的内容');
    }
}
```

```html
<input type="button" value="按钮" id="btn">
```

sub页面

```css
body{
    background: #2ecc71;
}
```

```javascript
window.onload = function () {
    let oBtn = document.getElementById('btn');
    oBtn.onclick = function () {
        open('sup.html','测试','width=200,height=200,left=200,top=200');
    }
}
```

```html
<input type="button" value="按钮" id="btn">
```