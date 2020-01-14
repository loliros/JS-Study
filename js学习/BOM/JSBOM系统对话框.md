#### JSBOM系统对话框

```
BOM(Browser Object Model)
BOM是浏览器的对象模型
可以通过window对象来控制BOM
在客户端JavaScript中，Window对象是全局对象，所有的表达式都在当前的环境中计算

系统对话框
浏览器可以通过调用系统对话框，向用户显示信息
系统提供了三个函数，可以完成系统对话框的操作
alert()弹出警告框
参数：警告框显示的内容
可以通过window.alert()调用
所以alert()是window的函数
只不过window下的函数都可以省略window不写

confirm()弹出一个带有确定和取消的警告框
返回值 点击确定则返回true 点击取消则返回false

prompt()弹出一个带输入框的提示框
第一个参数：要在提示框上显示的内容
第二个参数：输入框内默认的值
点击确定：返回值是我们输入的内容
点击取消：返回值是null
```

```javascript
alert(window);//[object Window] window对象 相当于在浏览器中打开的一个窗口
confirm('请选择确定或者取消');
prompt('请输入一个数',0);
```