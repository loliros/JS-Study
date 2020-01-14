#### JSBOM的location属性

```
location 我们浏览器上的地址栏输入框
它提供了与当前窗口的中加载的文档有关的信息，
还提供了一些导航功能

location中的属性

url 统一资源定位符（快递包上的一个地址）

hash 如果该部分存在，表示锚点部分
host 主机名：端口号
hostname 主机名
href 整个url
pathname 路径名
port 端口号
protocol 协议部分
search 查询字符串
```

```javascript
/* alert(location);
        alert(window.location);
        alert(window.document.location);*/

        /*
            alert(location.hash);//锚点是#号后面的部分 锚点一般用于业内跳转
            window.onload = function () {
            document.onclick = function () {
                location.hash = '#3';
            }
        }
            将#3拼接到url后面
            http://localhost:63342/Test/B%E7%AB%99%E8%87%AA%E5%AD%A6/%E5%8D%83%E5%B3%B01000%E9%9B%86/JS%E5%9F%BA%E7%A1%80%E8%AE%B2%E8%A7%A3/BOM%E7%9A%84location%E5%AF%B9%E8%B1%A1.html?_ijt=4n1kpmhdq0jctt0rdt0nfe0rm4#3
         */

        /*
            host ip拼上端口号 浏览器的端口号默认为8080
            alert(location.host);
         */

        /*
            hostname 主机名 域名/ip
            域名就是给ip起一个好记的名字
         */
            //alert(location.hostname)

        /*
            href 整个url
         */
            //alert(location.href);//输出整个url 与alert(location)的输出一样

        /*
            pathname 路径名
         */
        //alert(location.pathname);

        /*
            port 端口号
         */

        /*
            protocol 协议
         */
        //alert(location.protocol);//在本地文件加载显示file 在服务器加载文件是http

        /*
            search 查询字符串

            跟在?后面的部分

            比如https://www.bilibili.com/video/av45705742?p=82
            ?p=82 传输的检索的数据
         */
```