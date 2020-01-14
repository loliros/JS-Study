#### JS定时器

```
setInterval()
setInterval(函数,毫秒数)
功能：每隔所传参数得毫秒数，就调用一次所传参数得得函数
返回值：当前页面上对于定时器的唯一标识，就是定时器的ID
当多次点击的时候会触发多个定时器 所以判断下定时器的id
使其不要高与1 且清除的时候需要注意清除干净

clearInterval()取消定时器
参数：定时器的ID
```

```javascript
    <script>
        let i = 0;
        window.onload = function () {
            let btn = document.getElementById('btn');
            btn.onclick = function () {
                let time = setInterval(function(){
                    document.write(i++ + '<br>');
                    if (time > 1){
                        clearInterval(time);
                    }
                    if (i >= 5){
                        clearInterval(time);
                    }
                },1000);
            }
        }
    </script>
    <body>
<input type="button" id="btn" value="按钮">
</body>
```

```
innerHTML
test.innerHTML = '<h1>啦啦啦</h1>'
如果在innerHTML包含标签，标签会被识别，并且会解析，呈现对应的效果
```

```javascript
window.onload = function () {
     let btn = document.getElementById('btn');
     let test = document.getElementById('test');

     btn.onclick = function () {
         test.innerHTML = '<h1>啦啦啦</h1>'
     }
}
```

```html
<body>

<div id="test"><em>啦啦啦</em></div>

<input type="button" id="btn" value="按钮">
</body>
```

