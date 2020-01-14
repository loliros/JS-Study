#### JS日期对象的方法

```
日期对象格式化的方法
日期对象.方法();
let time = new Date();
alert(time.toDateString());//以特定的格式显示星期几 月 日 年
alert(time.toTimeString());//以特定格式显示时、分、秒、区
alert(time.toLocaleDateString());//以特定地区格式显示星期几、月、日、年
alert(time.toLocaleTimeString());//以特定地区格式显示时、分、秒、时区
alert(time.toUTCString());//以特定格式显示完整的UTC日期

如果不满意上面的输出格式
可以对年月日时分秒分别进行取出
set系列函数是设置值 get系列函数是获取值
没有UTC的函数是获取系统当前时间
有UTC的是输出格林尼治时间

获取一周中的某一天从0开始，星期0代表的是周日，而且只能获取，不能设置
getDay()
获取月份的时候也是从0开始
set/getMonth()

setTime()/getTime()的参照物都是从1970年开始 获取的是当前日期距离1970年的毫秒数

Date.parse()
参数：是一个日期格式的字符串
功能：返回这个日期距离1970年的毫秒数
```

```javascript
let time = new Date();
alert(time.toDateString());
alert(time.toTimeString());
alert(time.toLocaleDateString());
alert(time.toLocaleTimeString());
alert(time.toUTCString());
alert(time.getDay());
alert(time.getMonth());
let time1 = Date.parse('2020-1-8');
let time2 = new Date(time1);
alert(time2);
```