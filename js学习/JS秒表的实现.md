#### JS秒表的实现

```css
body>div{
    background: #2ecc71;
    width: 200px;
    height: 300px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    text-align: center;
}
input{
    display: block;
    text-align: center;
    margin: 15px auto;
    width: 100px;
    height: 50px;
}
body>div>div{
    margin: 15px;
}
body>div>div>span{
    margin: 0 5px;
}
```

```javascript
        /*
            1、将查找标签id的操作进行简化
            2、实现开始按钮的功能
            3、使其10以下的时候显示两位数
            4、实现暂停按钮的功能
            5、实现停止按钮的功能
         */

function $(id) {
                return document.getElementById(id);
            }

            window.onload = function () {
                let count = 0;//开始计数后，累加的秒数
                let timer = null;
                $('start').onclick = function () {
                    timer = setInterval(function () {
                        count++;
                        //改变时分秒的值
                        $('id_S').innerHTML = showNum(count % 60);
                        $('id_M').innerHTML = showNum(parseInt(count / 60) % 60);
                        $('id_H').innerHTML = showNum(parseInt(count / 3600));
                    },1000);
                }

                $('stop').onclick = function () {
                    //取消定时器
                    clearInterval(timer);
                }

                $('clear').onclick = function () {
                    //清除定时器的时间
                    clearInterval(timer);
                    count = 0;
                    $('id_S').innerHTML = '00';
                    $('id_M').innerHTML = '00';
                    $('id_H').innerHTML = '00';
                }
            }

            //处理单个数字
            function showNum(num) {
                if (num < 10){
                    return '0' + num;
                }else{
                    return num;
                }
            }
```

```html
<div>
    <div><span id="id_H">00</span><span id="id_M">00</span><span id="id_S">00</span></div>
    <input type="button" id="start" value="开始">
    <input type="button" id="stop" value="暂停">
    <input type="button" id="clear" value="停止">
</div>
```