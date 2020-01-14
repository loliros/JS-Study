#### JS日期对象的方法的练习

```
1、显示当前的时间
2、setDate()和getDate()，封装一个函数，可以根据输入的数值n(天数)显示n天后的时间
```

```javascript
function nowDate() {
    let nowTime = new Date();
    let nowYear = nowTime.getFullYear();//获取年
    let nowMonth = nowTime.getMonth() + 1;//获取月
    let nowDay = nowTime.getDate();//获取日
    let nowWeek = nowTime.getDay();//获取周数
    switch(nowWeek){
        case 0:
            nowWeek = '日';
            break;
        case 1:
            nowWeek = '一';
            break;
        case 2:
            nowWeek = '二';
            break;
        case 3:
            nowWeek = '三';
            break;
        case 4:
            nowWeek = '四';
            break;
        case 5:
            nowWeek = '五';
            break;
        case 6:
            nowWeek = '六';
            break;
    }
    let nowHours = nowTime.getHours();
    let nowMinutes = nowTime.getMinutes();
    let nowSeconds = nowTime.getSeconds();
    alert(nowYear + '年' + nowMonth + '月' + nowDay + '日 星期' + nowWeek + nowHours + '时' + nowMinutes + '分' + nowSeconds + '秒');
}
nowDate();

function time(n) {
    let time = new Date();
    let data = time.getDate();
    time.setDate(data + n);
    alert(time);
}
time(2);
```