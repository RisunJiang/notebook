电脑
===
[2019-04-12]
--------------
#### VScode, pgsql插件使用说明:
1. 打开编辑pgsql文件, 按 Ctrl+F5执行;
2. For snippets press Ctrl_Space, type 'pg'

[2019-10-04] 
---------------
#### PC显示器做手机投影: 
1. 点菜单栏最下面的通知icon. 
2. 单击连接icon. 
3. 选 "投影到此电脑". 
4. 手机上启动"Screen mirroring assistant"单击START. 选择无线显示, 搜索到设备后选择相应设备, 如 "RISUNPC"

#### node.js 安装, 运行  
1. 官网下载: nodejs.org => download LTS(最新稳定版)
2. 安装 .msi 文件 (node-v10.16.3-x64.msi);
3. 运行: 进cmd, 输入 "node -v", 查看版本号. 输出: "v10.16.3";

#### 微软便笺在Android上运行
1. 在Android手机上安装OneNote;
2. 登录, 运行, 下边栏有 "便笺", 切换后即可显示和编辑便笺;
3. 在Android 平板上, 要使用网页版, OneNote安装后没有下边栏, 无法切换到便笺;
4. 网页版地址: https://www.onenote.com/stickynotes#

#### 热键 
1. 系统属性: Windows + Pause(Break)

[2019-10-05]
---------------
#### VS Code 快速输入HTML 
1. 创建保存.html文件; 
2. 只要输入"HTML:5", 空的HTML框架即可创建;

#### VS Code 运行 HTML文件
1. 安装Live Server 插件: 

[2019-10-06]
--------------
上海产线反应辅助系统的sn 不良信息无法查到, 经过郭首君诊断, 是48ping不同31.
1. 请Link找资讯如何ping通;
2. 临时请上海工程师发出不良SN, 请郭到数据库查后,发出来;

[2019-10-07]
--------------
#### VS Code 安装 nodejs相关插件
1. npm: 
https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script

#### VS Code 命令行启动:
$ code .

#### VS Code手册之Node.js 教程
教程很不错, 包括javascript, Node.js, Express, Vue等等:
https://code.visualstudio.com/docs/nodejs/nodejs-tutorial
1. 从 "Node.js tutorial in Visual Studio Code" 开始,  按教程步骤操作.

[2019-10-08]
--------------
#### 研究测试ICT F3 file server 10.99.106.48 网络问题:
1. 从外面 ping 10.99.106.48 成功;
2. 据张兴龙和郭首君说, 从48 上ping 其它机器, 如 10.99.170.62, 10.99.106.31 都ping不通;
与Link 微信联系, 告知他情况. 他已经知道, 并正在请FIS的人找IT人员来处理中.

#### twitter search API -- twitter 数据分析
1. Twitter提供Restapi: https://developer.twitter.com/en/docs/tweets/search/overview
2. 一篇中午介绍文中: [Twitter数据挖掘：如何使用Python分析大数据
](http://www.itran.cc/2017/06/15/twitter-data-mining-using-python/)
3. 一篇英文: [Python Twitter Search API](https://twitterdev.github.io/search-tweets-python/)
4. 不用开发的方式搜索twitter: [Twitter搜索网站：最好的三个，其余所有](https://www.cnet.com/news/twitter-search-sites-the-three-best-and-all-the-rest/)
  文章是2009年的, 文中介绍了多个应用, 但多数已经不能使用, 原因之一是twitter search api修改了.
  - twitter自己的搜索网站: http://search.twitter.com/
  - Twazzup: http://new.twazzup.com/
  - Collecta: http://collecta.com/ , 已经removed了.
  
[2019-10-13]
--------------
#### Google Chart API 与 Google Charts
1. Google Chart API: https://en.wikipedia.org/wiki/Google_Chart_API
2. Google Charts: https://developers-dot-devsite-v2-prod.appspot.com/chart
3. Google Chart API 已经被淘汰, 代之以 Google Charts
4. 百度charts是否也是学google的?
5. eCharts: https://echarts.apache.org/examples/en/
6. ECharts 5 分钟上手: https://echarts.apache.org/zh/tutorial.html#5%20%E5%88%86%E9%92%9F%E4%B8%8A%E6%89%8B%20ECharts
7. Vue-ECharts: https://ecomfe.github.io/vue-echarts/demo/

#### npm
1, npm 全称为 Node Package Manager 是Node.js的包管理器, 以 JavaScript编写的软件包管理系统.
2. npm 随着 Node.js 自动安装;
3. 通过 npm 下载 ECharts: npm install echarts --save

[2019-19-14]
--------------
#### GraphQL
1. 科普, 什么是GraphQL -- 一种采用类似SQL的语法, 从前端访问数据库的语言, 代替RESTful API;
2. 参考文: https://ithelp.ithome.com.tw/articles/10200678
3. GraphQL怎么用: https://www.infoq.cn/article/i5JMm54_aWrRZcem1VgH

[2019-19-15]
--------------
#### psql
1. greenplum 中string 函数, 没有left, right函数, 只能用 substring.

[2019-19-16]
--------------
#### VSCode 用正则表达式搜索:
1. 搜索两个字符串, 中间间隔任意内容的方法: 用 ".*" 代表任何内容. 如, 搜索'pca_sno'与'model'同时出现: "pca_sno.*model".
#### GoldenGate
1. 用来做实时数据同步
2. 官网: https://www.oracle.com/middleware/technologies/goldengate.html
3. 中文介绍: https://www.oracle.com/technetwork/cn/community/developer-day/3-goldengate-289794-zhs.pdf
#### Node,js
参考: https://scriptverse.academy/tutorials/nodejs-render-html.html

[2019-19-16]
--------------
#### CentOS 7x86_64 bbr 什么是bbr?
1.  为解决TCP网络丢包 google开发的一种算法. 全称: BBR（Bottleneck Bandwidth and RTT）
2. https://tech.jandou.com/CentOS7-Google-BBR.html

#### 重装Bandwagon VPS 104.129.183.162
1. OS 换成 CentOS 7x86_64 bbr
2. root/T7iDyweZP1yY
3. SSH Port: 28361

[2019-19-17]
--------------
#### VS code 热键
1. 切换到终端 (terminal): Ctrl+`
2. 热键全集: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf

#### Node.js 与 HTTP消息结构
1. 介绍: https://www.runoob.com/http/http-messages.html
2. MIME 类型: https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Basics_of_HTTP/MIME_types
3. Content-Type: "text/html" 与 "text/plain" 的区别: html表示后面的内容是html格式, 里面的<>标签会被解释, 而 "text/plain" 后面应该是纯文本, 即便有html tag也不被解释, 会原样显示.
4. 一个简单的Node.js 例子:
> var http = require("http");
> var server = http.createServer(function(req, response){
>     var d = new Date();
>     var n = d.toString();
>     //response.writeHead(200, {"Content-Type": "text/html;charset=utf-8"});
>     response.writeHead(200, {"Content-Type": "text/html;charset=utf-8"});//plain -> html
>     response.write("<!doctype \"html\"> <html lang=\"en\"> <head><title>Hello, world!</title> </head> <body><h1> 我的第一个 Node.js程序. 今天是" + n + "</h1> </body></html>");
>     response.end();
> });
> //监听:
> server.listen(3000,"127.0.0.1");

[2019-10-18]
--------------
https://twitter.com/nishuang/status/1184137359308312576?s=09https://twitter.com/nishuang/status/1184137359308312576?s=09

[2019-10-19]
--------------
#### 用node.j做proxy的研究
1. https://github.com/chimurai/http-proxy-middleware
2. node-http-proxy: https://github.com/http-party/node-http-proxy
3. 中文介绍，https://www.jianshu.com/p/94e86e2c5874
4. 中文例子，https://cnodejs.org/topic/530f41e75adfcd9c0f1c8c16

#### 虚拟S 变化:
1. 扔掉: 149.248.50.170 (Ca), 增加: 202.182.125.63 (Jap)

#### node.js 
1. 一个js程序可以创建多个server, 只要端口不同即可;

#### vscode 改变样式主题
1. 菜单 "文件" - "首选项(P)" - "颜色主题(C)" 或 Ctrl+K, Ctrl+T

#### VPS Vultr SSH无法连接
1. 修改SSH端口: vim /etc/ssh/sshd_config
2. port 22 => port 1819 
3. 试试是否能连, 如果还连不上, 从另一个VPS上连这台. 使用ssh命令:
4. 从另一台VPS上SSH:
    指定用户: > # ssh -l root 192.168.0.11
    指定端口: > # ssh -p 12333 192.168.0.11
5. 新VPS: 202.182.125.63
    服务器IP：202.182.125.63
    主端口：31451
    UUID：a3f4c514-f26e-11e9-a68d-5600025f8e2b
    加密方式：aes-128-gcm
    传输方式：tcp
    TLS：关闭
    欢迎使用 V2ray.fun 管理程序 Author:雨落无声
6. 最后还是不行, v2ray没反应. 
7. 看来JAP的不行了

#### VPS Singapore
1. 149.28.136.38
2. 5ad2e0f8-f27a-11e9-a9d9-5600025f9cb5
3. 31451
4. aes-128-gcm
5. www.yahoo.com
```
{
 "outbound": {
  "streamSettings": {
   "network": "tcp", 
   "kcpSettings": null, 
   "wsSettings": null, 
   "tcpSettings": {
    "header": {
     "type": "http", 
     "request": {
      "path": [
       "/"
      ], 
      "version": "1.1", 
      "method": "GET", 
      "headers": {
       "Host": "www.yahoo.com", 
       "User-Agent": [
        "Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/55.0.2883.75 Safari/537.36", 
        "Mozilla/5.0 (iPhone; CPU iPhone OS 10_0_2 like Mac OS X) AppleWebKit/601.1 (KHTML, like Gecko) CriOS/53.0.2785.109 Mobile/14A456 Safari/601.1.46"
       ], 
       "Connection": [
        "keep-alive"
       ], 
       "Pragma": "no-cache", 
       "Accept-Encoding": [
        "gzip, deflate"
       ]
      }
     }, 
     "response": {
      "status": "200", 
      "headers": {
       "Transfer-Encoding": [
        "chunked"
       ], 
       "Connection": [
        "keep-alive"
       ], 
       "Content-Type": [
        "application/octet-stream", 
        "video/mpeg"
       ], 
       "Pragma": "no-cache"
      }, 
      "reason": "OK", 
      "version": "1.1"
     }
    }, 
    "connectionReuse": true
   }, 
   "tlsSettings": {}, 
   "security": ""
  }, 
  "tag": "agentout", 
  "protocol": "vmess", 
  "mux": {
   "enabled": true
  }, 
  "settings": {
   "vnext": [
    {
     "users": [
      {
       "alterId": 100, 
       "security": "aes-128-gcm", 
       "id": "5ad2e0f8-f27a-11e9-a9d9-5600025f9cb5"
      }
     ], 
     "port": 31451, 
     "address": "149.28.136.38"
    }
   ]
  }
 }, 
 "log": {
  "access": "", 
  "loglevel": "info", 
  "error": ""
 }, 
 "outboundDetour": [
  {
   "tag": "direct", 
   "protocol": "freedom", 
   "settings": {
    "response": null
   }
  }, 
  {
   "tag": "blockout", 
   "protocol": "blackhole", 
   "settings": {
    "response": {
     "type": "http"
    }
   }
  }
 ], 
 "inbound": {
  "streamSettings": null, 
  "settings": {
   "ip": "127.0.0.1", 
   "udp": true, 
   "clients": null, 
   "auth": "noauth"
  }, 
  "protocol": "socks", 
  "port": 1082, 
  "listen": "0.0.0.0"
 }, 
 "inboundDetour": null, 
 "routing": {
  "settings": {
   "rules": [
    {
     "ip": [
      "0.0.0.0/8", 
      "10.0.0.0/8", 
      "100.64.0.0/10", 
      "127.0.0.0/8", 
      "169.254.0.0/16", 
      "172.16.0.0/12", 
      "192.0.0.0/24", 
      "192.0.2.0/24", 
      "192.168.0.0/16", 
      "198.18.0.0/15", 
      "198.51.100.0/24", 
      "203.0.113.0/24", 
      "::1/128", 
      "fc00::/7", 
      "fe80::/10"
     ], 
     "domain": null, 
     "type": "field", 
     "port": null, 
     "outboundTag": "direct"
    }
   ], 
   "domainStrategy": "IPIfNonMatch"
  }, 
  "strategy": "rules"
 }, 
 "dns": {
  "servers": [
   "8.8.8.8", 
   "8.8.4.4", 
   "localhost"
  ]
 }
}
```

#### Bandwagon 换IP:
https://bwh88.net/ipchange.php
付款后等待, 24内, 人工处理...不会马上变.

[2019-10-20]
--------------
#### Bandwagon 
1. root password: Bandwagon password 是在 KiWiVM管理界面中由用户自己创建的: 进入https://bwh1.net/ -> Register -> Client Area -> Services -> My Services -> KiwiVM Control Panel -> Root password modification
2. 新换的 IP:104.129.183.96, SSH Port: 28361, OS: CentOS 7x64, root pw:T7iDyweZP1yY
3. v2ray: 
 主端口：31451
 UUID：f054eeca-f340-11e9-b2a0-aaaa000eb29a
 加密方式：aes-128-gcm
 传输方式：tcp
 TLS：关闭

[2019-10-25]
--------------
#### ansible 是一种 Linux 自动化运维工具
1. 中文介绍: [ansible总结](https://www.jianshu.com/p/c82737b5485c)
2. 中文 [Ansible中文权威指南](https://ansible-tran.readthedocs.io/en/latest/index.html)
 
[2019-10-26]
--------------
#### Windows 快捷键
1. 鼠标右键的键盘快捷键: Win + F10
2. 部分快捷键定义: https://en.wikipedia.org/wiki/Windows_key

#### VScode 快捷键
1. 折叠, 展开 (folding and unfolding): 折叠 "ctrl + shift + [" 展开: "ctrl + shift + ]" : https://zellwk.com/blog/useful-vscode-keyboard-shortcuts/

#### VScode Markdown Preview Enhanced 插件的 css样式设置
1. ctrl+shift+p: 设置markdown-preview.markdown-preview
2. 文件路径: C:\Users\risun_jiang\.mume\style.less
3. mermaid 流程图框图内部黑色问题修改: 
需要修改插件的package.json文件：
https://github.com/shd101wyy/vscode-markdown-preview-enhanced/issues/151
    * 文件路径：C:\Users\itc940077\.vscode\extensions\shd101wyy.markdown-preview-enhanced-0.3.12\package.json
    * 原文本：
--------------------------------------------------------------------------
```json
				"markdown-preview-enhanced.mermaidTheme": {
					"description": "Mermaid theme, you can choose one from [\"mermaid.css\", \"mermaid.dark.css\", \"mermaid.forest.css\"]",
					"default": "mermaid.css",
					"type": "string",
					"enum": [
						"default",
						"dark",
						"forest"
					]
				},
```
--------------------------------------------------------------------
    * 修改为：“default”:"mermaid.css" -> "default": "default"
------------------------------------------------------------------------
```json
         				"markdown-preview-enhanced.mermaidTheme": {
					"description": "Mermaid theme, you can choose one from [\"mermaid.css\", \"mermaid.dark.css\", \"mermaid.forest.css\"]",
					"default": "default",
					"type": "string",
					"enum": [
						"default",
						"dark",
						"forest"
					]
				},
```
------------------------------------------------------------------------
    * 存盘重启后，软件右下角提示更新插件，点确定。

[2019-10-29]
--------------
#### Java解析Excel 2003
1. Java解析Excel: 解析2003及以下使用HSSFWorkbook类，解析2007及以上使用XSSFWorkbook.
2. 中文参考: https://blog.csdn.net/javaloveiphone/article/details/9499159
3. 获取Cell 样式: [CellStyle workbook.getCellStyle()](https://poi.apache.org/apidocs/dev/org/apache/poi/hssf/usermodel/HSSFCell.html#getCellStyle--);
4. 获取前景颜色: [CellStyle.getFillForegroundColorColor()](https://poi.apache.org/apidocs/dev/org/apache/poi/hssf/usermodel/HSSFCellStyle.html#getFillForegroundColor--);
5. 接口说明: https://poi.apache.org/apidocs/dev/org/apache/poi/ss/usermodel/CellStyle.html;
6. 中文参考: [POI获取excel单元格红色字体，淡蓝色前景色的内容](https://www.cnblogs.com/DurantSimpson/p/3966472.html)
7. 上文摘要: 如果是Microsoft Excel 97-2003 工作表 (.xls)
>if(31 == cell.getCellStyle().getFillForegroundColor()) //判断单元格前景色为淡蓝色
>if(10 == book.getFontAt(cell.getCellStyle().getFontIndex()).getColor()) //判断单元格字体颜色为红色


[2019-10-31]
--------------
#### VScode  快捷键
1. 焦点进入资源管理器 (文件列表) -- ctrl + shift + E

#### python 调用 MySql 的存储过程 stored Procedure
1. 基本过程:
try:
    connection = mysql.connector.connect(host='localhost',
                                         database='Electronics',
                                         user='pynative',
                                         password='pynative@#29')
    cursor = connection.cursor()
    cursor.callproc('get_laptop', [1, ])
2. 参考: https://pynative.com/python-mysql-execute-stored-procedure/

#### postgres 如何取消正在执行的查询
1. 先查出正在执行的查询:
    What I did is first check what are the running processes by
> SELECT * FROM pg_stat_activity WHERE state = 'active';
2. 找到要删的process 执行以下函数删除:
    Find the process you want to kill, then type:
> SELECT pg_cancel_backend(<pid of the process>)
3. 如果上述函数没有删除成功, 执行下面这个函数:
    If the process cannot be killed, try:
> SELECT pg_terminate_backend(<pid of the process>)

#### REST api 如何进行身份认证和授权
1. 参考: RESTful API身份验证基础 (https://blog.restcase.com/restful-api-authentication-basics/)


[2019-11-2]
--------------
#### 用Python解析日志log文件
1. 参考: https://pythonicways.wordpress.com/2016/12/20/log-file-parsing-in-python/

#### 使用Python处理电子表格 (Excel)
1. 参考: https://hackernoon.com/working-with-spreadsheets-using-python-part-1-380a120387f
2. 新旧两种Excel, The package **xlwt** supports the .xls; The package **openpyxl** supports the .xlsx
3. 中文参考: [Python使用xlwt模組操作Excel的方法詳解](https://codertw.com/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80/358550/)
4. 中文参考: [python使用xlrd与xlwt对excel的读写和格式设定](https://www.jb51.net/article/103780.htm)
   python操作excel主要用到xlrd和xlwt这两个库，即xlrd是读excel，xlwt是写excel的库。本文主要介绍了python使用xlrd与xlwt对excel的读写和格式设定，下面话不多说，来看看详细的实现过程。
5. xlrd库 API参考手册: [xlrd API Reference](https://xlrd.readthedocs.io/en/latest/api.html)
6.获取文字颜色: 在那里，您只需要挖掘一点即可。 有了工作表（打开工作簿，获取工作表的引用）之后，可以使用cell_xf_index（rowx，colx）获取单元格的xf（eXcel格式）索引，您可以将其用作工作簿的索引 xf_list。 XF告诉您使用什么字体定义。 字体定义具有颜色索引。 如果颜色索引转换为红色，则说明已找到所需的内容。(https://stackoverflow.com/questions/39814842/how-to-get-the-text-colour-of-excel-cell-using-xlrd-or-openpyxl?rq=1)
7. 获取文字颜色: https://groups.google.com/forum/#!topic/python-excel/0csvcjhJk8o
8. xlrd库


[2019-11-3]
--------------
#### 关于Python Twisted 库
1. JY本期实习(Evertz)用到 PythonTwisted 开发.
2. JY当前工作系统架构: e:\Programming\JY20191103实习\structure.pptx
3. Python Twisted Book: e:\Books\编程\Python\Twisted\Oreilly Twisted Network Programming Essentials 2 Nd Edition 2013 Retail Ebook Elohi M.pdf
4. 中文介绍: [Twisted 入门教程](https://wiki.jikexueyuan.com/project/twisted-intro/p01.html)
  - 原文: [**Twisted Introduction**](http://krondo.com/an-introduction-to-asynchronous-programming-and-twisted/)
5. Twisted 可以做proxy:
   - 参考: [HTTP Debug Proxy with Twisted](http://sujitpal.blogspot.com/2010/03/http-debug-proxy-with-twisted.html)
   - 参考: [Python - Twisted, Proxy and modifying content](https://stackoverflow.com/questions/9465236/python-twisted-proxy-and-modifying-content)

#### Python 的类
1. 中文参考: [Python中self用法详解](https://blog.csdn.net/clhugh/article/details/75000104)
2. Python 定义一个Class:
   - 其中, (Object) 表示该类从哪个类继承下来的, Object是所有类都会继承的类;
```python
class Student(Obejct):
    pass
```
3. 实例:
```python
student = Student()
```
4. 构造函数或叫初始化方法, 以及self 用法:
   - __init__方法的第一个参数永远是self, 表示创建的类实例本身.
   - self参数不需要传入, Python解释器自己把实例变量传进去.
```python
class Student(object):
    def __init__(self, name, score):
        self.name = name
        self.score = score
```
```python
>>>student = Student("Hugh", 99)
>>>student.name
"Hugh"
>>>student.score
99
```

#### Python 检查文件是否closed
1. 以下是Python 2.x的代码:
```python
f = open('file.py')
if f.closed:
    print 'file is closed'
```
2. 来源: [check if a file is open in Python](https://stackoverflow.com/questions/6825994/check-if-a-file-is-open-in-python)

[2019-11-6]
--------------
#### pgsql 获取时间函数 now()与clock_timestamp() 的区别
1. now() 在单独的SQL中执行, 就是取当时时间, 但在一段函数中执行时, 取的时 transaction的起始时间, 在整个函数内, 每处执行now(), 返回都是同一时间;
2. clock_timestamp() 在函数内执行, 取的时间是不同的, 都是当时时刻的时间. 单独执行与now()是一样的.

[2019-11-7]
--------------
#### pgsql 获取索引列表和size
1. 执行以下命令可以获取索引列表和size:
```sql
ict=# \di+ ict.*
                                   关联列表
 架构模式 |     名称     | 类型 | 拥有者  |      数据表       |  大小   | 描述
----------+--------------+------+---------+-------------------+---------+------
 ict      | idx_testtime | 索引 | ictuser | ictlogtestpart_ao | 1922 MB |
(1 行记录)
```
2. 执行函数pg_table_size() 可以获取特定索引的size:
```sql
select pg_table_size('ict.idx_testtime');
  pg_table_size
 ---------------
    2016002048
(1 行记录)
```

[2019-11-8]
--------------
#### Markdown 转ppt
1. [5分鐘製作 MARKDOWN POWERPOINT](https://calpa.me/2017/06/01/create-markdown-powerpoint-in-5-mins/)

[2019-11-9]
--------------
#### pgsql 如何在where条件中加上case when
问题说明: 假设我有一个参数_pdline, 字符串, 当它有值时, 那它当过滤条件, 而当它等于空串时, 过滤条件不起作用. 
方案说明: 当参数_pdline等于''时, 栏位pdline等于自身; 而当_pdline有值时, pdline=_pdline.
```sql
DO $$
DECLARE
  _pdline character varying(10) := 'P21';
BEGIN 
    create temp table aaa as select * from dwict.fact_rt_failpartpin where pdline = (case _pdline when '' then pdline  else _pdline end);
END $$;
select * from aaa;
```

[2019-11-16]
--------------
#### Linux命令大全
1. 原文: https://www.codercto.com/tutorial/linux-commands/manual.html
#### Markdown中使用内嵌HTML，增加Markdown的功能
1. 原文: https://blog.csdn.net/u010987458/article/details/71272854
2. md插入字体标签设置字号字体颜色: 
```html
<font face="verdana" color="green" size="3">This is some text!</font>
```

#### HTML color codes names
1. 原文: https://www.computerhope.com/htmcolor.htm
2. color="SteelBlue" 铁灰蓝

[2019-11-17]
--------------
#### VSCode 写Python
1. 文章: [用 VSCode 愉快地写 Python](https://zhuanlan.zhihu.com/p/66157046);
2. 上文推荐安装Anaconda, 一个Python发行版, 带Conda包管理软件和一堆库, 用于 数据处理, 预测分析, 和科学计算.
3. Anaconda官网下载: https://www.anaconda.com/distribution/#download-section
4. VSCode 要安装插件 Python
5. 要让VSCode使用Anaconda, 需要在VSCode中设置, 在VSCode中, 点击状态栏左下角的Python图标, 然后先择安装的Anaconda.

[2019-11-25]
--------------
#### win10 中添加快捷方式到开始菜单
1. 原文: https://blog.csdn.net/u010814849/article/details/77413479
2. 要点: 先将快捷方式文件放入 C:\ProgramData\Microsoft\Windows\Start Menu\Programs 目录. 再从左侧快捷方式用右键执行 "固定在开始屏幕".

#### Paint.net 添加icon文件格式
1. 下载IcoCur.zip: https://forums.getpaint.net/applications/core/interface/file/attachment.php?id=10208
2. 解压文件IcoCur.dll
3. 将IcoCur.dll copy到 c:\Program Files\paint.net\FileTypes\IcoCur.dll

[2019-11-26]
--------------
#### PowerShell 介绍
1. [PowerShell 与 cmd 有什么不同](https://www.zhihu.com/question/22611859)
2. PowerShell 还有一个IDE: Windows PowerShell ISE

#### VSCode Python 如何启动 Jupyter Server
1. 介绍启动JupyterNotebooks [Working with Jupyter Notebooks in Visual Studio Code](https://code.visualstudio.com/docs/python/jupyter-support)
2. 如何启动 Jupyter Server还不知道......

[2019-12-7]
--------------
https://link.resilio.com/#f=Books&sz=0&t=1&s=PATBUEVXJI6YUOPHCTBRNHZKBIIPGYR3&i=CR2I2QSJMNN7CUBZ7BM3XQ6GOGA3EVKMD&e=1576077618&v=2.6&a=2
r/w: A3VRHDGANBNBV6RDMEQURCLDLPPUASKND
ro: BDGKMBBTJ4WTXBDC63FBI7HA5M5WFDJ6Q


[2019-12-09]
------------------
#### Trojan 安装 GFW
https://youtu.be/eiI2e4gnO4w

[2019-12-11]
------------------
#### psql 取时间的秒值
1. 提取自1970-01-01 00:00:00算起秒值:
```sql
SELECT EXTRACT(EPOCH FROM TIMESTAMP WITH TIME ZONE '2001-02-16 20:38:40.12-08');
  date_part   
--------------
 982384720.12
select extract(epoch from now());
    date_part     
------------------
 1576043792.07316
```

[2019-12-13]
------------------
#### 用python程序下载youtube
1. 网文: https://blog.usejournal.com/how-to-download-youtube-videos-in-python-a48701e70389

[2019-12-14]
------------------
#### 几个有关chart 图表中的单词
metrics => 指标, 指chart关注的数据项, 字段或字段的运算
axis => 周标签, 指坐标轴的刻度文字
legend => 图例

#### Grafana vs Kibana 比较
1. youtube: https://youtu.be/xXmOmFyN3Hs;
2. 感觉grafana适合做时间变化的数据程序; Kibana更适合做统计,  分析,综合. 它有文字云图;

#### ElasticSearch ES 搜索引擎
1. youtube: https://www.youtube.com/watch?v=gHx0rzTfrOo&list=PLmOn9nNkQxJE066izME0gcfLnjaB3wfFm

#### ELK平台
1. ELK Stack = Elasticsearch + Logstash + Kibana, 也称Elastic Stack
2. 三者关系
  - logstash: 采集分析过滤数据
  - ElasticSearch: 存储, 搜索数据
  - Kibana: 计算处理呈现
3. Elasticsearch 介绍
   Elasticsearch 是一个基于Lucent库的搜索引擎. 文本搜索.
4. 树莓派中搭建ELK监控平台（可打造物联网监控平台、魔镜系统）
  - 文章: https://zhuanlan.zhihu.com/p/23111516
5. Kibana只能访问Elasticsearch 数据, 搭配使用, 无法访问别的数据库, 如postgresql.


[2019-12-18]
------------------
#### v2ray 手机端改用v2rayNG
1. 发现原来用的App —— BifrostV”偷流量”，2分钟耗掉了1G。
2. 因此换成v2rayNG.
3. 设置参数要手工填参数，类似电脑上的v2rayN. 直接导入json文件失败。


#### Grafana 设置link
1. 以Table为例, 在Visuelization阶段 (即完成Data数据源后) 的设置中, 对要创建Link的字段, 先建立一个 'Column Style';
2. 激活 "Render value as link" Check box, 即 "在值上创建链接", 右侧会出现Link配置项;

#### Grafana 时间条件全局变量时区问题
1. 在Grafana中, 用$__timeFrom(), $__timeTo()全局变量设置时间查询条件的值;
2. 而$__timeFrom(), $__timeTo()返回的时间是带时区的. 而数据库table中的testtime 栏位是without time zone 的所以查询出来的时间段不对.
3. 如何将带时区的查询条件, 转换成不带时区的北京时间 time string: 
```sql
  - $__timeFrom() at time zone 'Asia/Shanghai'
  - $__timeTo()  at time zone 'Asia/Shanghai'
```
4. 完整语句: 
```sql
select * from dwict.get_failpart('1395A3183401','A3183401A,A3183401B,T3183401A,T3183401B', $__timeFrom() at time zone 'Asia/Shanghai', $__timeTo() at time zone 'Asia/Shanghai', 1000) order by "Fixture", "Number"
```

2019-12-24
------------------
#### grafana variable value aggregate to string

Csv¶

Formats multi-value variable as a comma-separated string.

servers = ['test1', 'test2'] String to interpolate: '${servers:csv}' Interpolation result: 'test1,test2'
https://grafana.com/docs/grafana/latest/reference/templating/

2019-12-28
------------------
#### 优酷视频下载
1. 使用软件: "稞麦综合视频站下载器(xmlbar) v9.99"
2. https://www.xmlbar.net/

2020-01-05
------------------
#### 数据与人工智能全貌2019
DATA $ AI LANDSCAPE 2019
1. URL: http://mattturck.com/wp-content/uploads/2019/07/2019_Matt_Turck_Big_Data_Landscape_Final_Fullsize.png

2020-01-06
-------------
#### psql数字取整指定位数
1. URL:  https://stackoverflow.com/questions/48900936/postgresql-rounding-to-significant-figures
2. Function:
```sql
CREATE OR REPLACE FUNCTION dwict.sig_digits(n anyelement, digits int) 
RETURNS numeric
AS $$
    SELECT round(n, digits - 1 - floor(log(n))::int)
$$ LANGUAGE sql IMMUTABLE STRICT;
```
3.测试:
```sql
select dwict.sig_digits(0.012345, 2);
-- 0.012
select dwict.sig_digits(12345, 2);
--12000
select dwict.sig_digits(12567, 2);
--13000
select dwict.sig_digits(0.012567, 3);
--0.0126
```

2020-01-09
-------------
#### Grafana 生成PDF文件的方法
1. 原文: http://www.bujarra.com/generando-informes-con-grafana-y-programar-su-envio/?lang=en
2. 简介: 需要安装一个插件 [Reporter](https://github.com/IzakMarais/reporter). 此插件安装后提供一个链接, 对于每一个dashboard, 有一个独立的URL. 然后, 在dashboard中创建link, 在link中添加这个链接.

#### Grafana 创建动态panels
1. 原文: https://grafana.com/docs/grafana/latest/reference/templating/
2. 简介:Grafana本身可以创建动态panels, 根据variable查询出来的结果, 创建panel, 有多少, 创建多少.

#### 各种BI软件汇总比较
1. 原文: https://www.capterra.com/business-intelligence-software/
2. 竟然一共有 453种 包括 tableau和Qlikview


2020-01-14
-------------
####  不同的几种Join关系图
1. 原文: https://blog.jooq.org/2015/10/06/you-probably-dont-use-sql-intersect-or-except-often-enough/
2. left join 不包括交集的方法: 
```sql
select <fields> from Table A left join Table B on A.key = B.key where B.key is null;
```
3.上述yu'j已经用在实际程序中: TAO ICT pg DB, functon: dwict.get_fact_failpart2();
 

2020-01-22
-------------
#### VS Code 插件 SQLTools
1. 说明: https://vscode-sqltools.mteixeira.dev/features/sessions-and-multiple-connections

2020-01-28
-------------
#### PDF文本复制后乱码如何转换
* 问题: JY的一个PDF文件, 英文, 复制文本出来是乱码,  无法查询, 如何转为正常英文;
* 解决方法:
  1. 打开google 翻译: [https://translate.google.com/](https://translate.google.com/)
  2. 选择 "文档" 翻译 , 注意: 默认是 "文字" 翻译;
  3. 设置翻译的原和目的语言, 原设为 **"检查语言"** ; 目的设为 "英语";
  4. 上传PDF文件: 点击 "浏览您的计算机", 选择文件, 确定, 点击 "翻译" 按钮;
  5. 页面会自动显示出英文文本, (但不会有图). 页面可以直接搜索, 也可以另存为其它格式文件,建议存成"网页(单个文件)" *.mhtnl 文件. 可以用word或chrome, ie打开.

2020-01-29
-------------
#### 如何创建免费的CMS website 网站
https://themeisle.com/blog/best-free-blogging-sites/
https://itxdesign.com/the-top-5-free-cms-solutions-for-your-websites/

#### 在VPS上安装Web应用的面板
* [宝塔面板官网](https://www.bt.cn)
[宝塔面板安装后必做的几处安全设置选项](https://www.laozuo.org/11011.html)
[34个出色的Web应用程序管理面板](https://deliciousthemes.com/34-outstanding-admin-panels-for-your-web-applications/)
国外的一个web应用面板 [CentOS Web Panel](http://centos-webpanel.com/). 不知道是谁抄谁的.


2020-01-31
-------------
#### Youtube - 用宝塔面板建WordPress
YouTube: [闲置VPS变废为宝/教你用宝塔面板一键搭建WordPress/搬瓦工秒变个人网站（上集）](https://www.youtube.com/watch?v=QGWYyGsxAPI)

#### VSCode 用HSS访问连接VPS 
1. 引入VSCode的 "终端" PowerShell
2.输入命令: 
```
ssh username@serverip(orname)
```
3. 例如:
```
PS C:\Users\risun_jiang> ssh root@149.28.136.38
The authenticity of host '149.28.136.38 (149.28.136.38)' can't be established.
ECDSA key fingerprint is SHA256:IJ3RFC7z6ZJw0um9HStCDQYrBwbuIl70rzO4+oys5SY.
Are you sure you want to continue connecting (yes/no)? y
Please type 'yes' or 'no': yes
Warning: Permanently added '149.28.136.38' (ECDSA) to the list of known hosts.
root@149.28.136.38's password:
Permission denied, please try again.
root@149.28.136.38's password:
Last failed login: Fri Jan 31 10:38:52 UTC 2020 from 218.92.0.204 on ssh:notty
There were 82 failed login attempts since the last successful login.
Last login: Fri Jan 31 10:06:57 2020 from 111.163.120.129
[root@vultr ~]# ls
config.json  install.sh
[root@vultr ~]# uname -a
Linux vultr.guest 3.10.0-957.27.2.el7.x86_64 #1 SMP Mon Jul 29 17:46:05 UTC 2019 x86_64 x86_64 x86_64 GNU/Linux
[root@vultr ~]# cat /etc/os-release
NAME="CentOS Linux"
VERSION="7 (Core)"
ID="centos"
ID_LIKE="rhel fedora"
VERSION_ID="7"
PRETTY_NAME="CentOS Linux 7 (Core)"
ANSI_COLOR="0;31"
CPE_NAME="cpe:/o:centos:centos:7"
HOME_URL="https://www.centos.org/"
BUG_REPORT_URL="https://bugs.centos.org/"

CENTOS_MANTISBT_PROJECT="CentOS-7"
CENTOS_MANTISBT_PROJECT_VERSION="7"
REDHAT_SUPPORT_PRODUCT="centos"
REDHAT_SUPPORT_PRODUCT_VERSION="7"

[root@vultr ~]#
```

#### VSCode 远程开发:
VSCode官方文章: [Remote Development tutorials](https://code.visualstudio.com/docs/remote/remote-tutorials)
安装插件: Remote Development
安装后点击左面终端 ICON, 提示错误信息:
```
WSL executable not found. Please make sure that WSL is installed.
来源: Remote - WSL (扩展)
```
  WSL是 "Windows Subsystem for Linux" -- windows上的linux虚拟机. 官网介绍 [https://docs.microsoft.com/en-us/windows/wsl/about](https://docs.microsoft.com/en-us/windows/wsl/about)
官文: [Remote Development using SSH](https://code.visualstudio.com/docs/remote/ssh)
连接远端server方法:
  1.在命令栏(F1)输入 ">remote-ssh: connect to Host" 回车后提示输入远程连接
  2. 输入: root@149.28.136.38
  3. VSC'o'de弹出一个新窗口, 提示zheng'zai连接, 过一会n秒后, 命令栏自动弹出, 但没有提示, 这时输入password.
  4. 之后连接成功. 但提示: "You seem to have git 1.8.3.1 installed. Code works best with git >= 2"


2020-02-01
-------------
#### 查看"quan'guo新型fei'yan疫情s最新动态"公众号的Js程序
1. 有两个网址: 
  * [丁香园](https://ncov.dxy.cn/ncovh5/view/pneumonia)
  * [腾讯新闻](https://news.qq.com/zt2020/page/feiyan.htm)
2. F12查看代码, 发现他们都是用 "BootStrap" 实现的. [w3schools.com bootstrap](https://www.w3schools.com/bootstrap/bootstrap_ver.asp)
3. 其中的可展开收起的表格可能是 [jQuery Expand Collapse Panels](https://www.yogihosting.com/creating-expandable-collapsible-panels-in-jquery/) 实现的;
4. 滚动表格超出一屏时表头固定在最上方, 是用 [StickyTableHeaders](https://github.com/jmosbech/StickyTableHeaders) 实现的

#### VPS Linux 管理面板
1. 知乎上的一个讨论: [](https://www.zhihu.com/question/52951080)
2. 其中2017年有人推荐以下平台:
  Ajenti：Linux和BSD控制面板。官网
  Feathur：VPS供应和管理软件。官网
  ISPConfig：Linux主机控制面板。官网  
  VestaCP：用于Linux和Nginx的主机面板。官网
  Virtualmin：基于webmin的Linux控制面板。官网
  ZPanel：Linux BSD和Windows控制面板。官网
  作者：摘星辰Li
  链接：https://www.zhihu.com/question/52951080/answer/170430513

#### 什么是Nginx
[Nginx是什么](https://www.jianshu.com/p/a4cc44202cf5)
文章还对比了三种WEB服务器: lighttpd, Apache, Nginx


2020-02-02
-------------
#### Vesta -- Simple & Clever Hosting Control Panel
http://www.vestacp.com/
这个看上去不错, 能装Apache, postgreSQL, FTP..
它好像Softaculous Aoto Install.
它具有Softaculous 自动安装程序的精美 外观，能够一键安装439个以上的应用程序，我们希望我们的经验不足的用户能够欣赏它，并且一般而言，它会让vesta更加易于使用和构建网站。

#### softaculous
https://www.softaculous.com/softaculous/
安装各种web app service

#### 代码真香 -- YouTube课程
https://www.youtube.com/channel/UCmlhPmTdqYhRWwWZWSIBwGw
讲到Git. 讲到在VPS上安装Nginx.
他讲了一个博客软件: Jekyll,静态博客, 使用markdown编写!

#### Textpattern 一个小的内容管理xi't
https://textpattern.com/
支持markdown

#### cPanel -- 国外最流行的虚拟主机管理系统
[VPS安装cPanel & WHM教程](https://www.vpsjz.com/jianzhan/685.html)
[cPanel安装小技巧 如何在512M内存VPS上成功安装cPanel并运行](https://www.wn789.com/7618.html)
[VPS服务器上安装cPanel控制面板教程](https://www.idcspy.com/cpanel-installation.html)
视频: https://www.youtube.com/watch?v=vr2bDyDfsvQ

#### Plesk -- 另一个强大的虚拟主机控制面板
Plesk(79%)比cPanel(19.5%)用的还多, 
[Plesk vs cPanel：比较世界上最受欢迎的虚拟主机控制面板](https://www.webhostingsecretrevealed.net/zh-CN/blog/web-hosting-guides/compare-web-hosting-control-panel-cpanel-vs-plesk/)
它们统称WHCP -- web host control panels(?)Web主机控制面板.
它们都是收费的.
由于cPanel是收费产品，国内真正为自己的VPS安装cPanel控制面板的比较少，我们大多使用国内免费VPS控制面板进行建站管理，比如宝塔、wdCP、LNMP、OneinStack等

#### 国内五款常用免费VPS建站控制面板使用及SSL部署介绍
https://www.wn789.com/4475.html


2020-02-07
-------------
#### excel 批量转 csv
[How To Batch Convert Multiple Excel Files To CSV Files In Excel?](https://www.extendoffice.com/documents/excel/5537-excel-batch-convert-to-csv.html)


 2020-02-10
-------------
#### VSCode 启动Jupyter Note 执行Python的方法
1. To work with Jupyter notebooks, you must activate an Anaconda environment in VS Code, or another Python environment in which you've installed the Jupyter package. To select an environment, use the Python: Select Interpreter command from the Command Palette (Ctrl+Shift+P).
    要使用Jupyter notebooks前提是，必须在VS Code中激活Anaconda环境，或者激活安装Jupyter软件包的另一个Python环境。要选择环境，请在命令面板（Ctrl + Shift + P）中选择 Python: Select Interpreter 命令。 
2. You define Jupyter-like code cells within Python code using a #%% comment
   在.py文件中, 开头写上 "＃%%" 注释就能够启动Jupyter note;

#### Import/Export from/into Excel to postgresql with Python

#### 发现有inventec的人把代码传到网上
1. 网址: https://www.geek-share.com/detail/2731905473.html
2.其中带有邮件信息: SELECT @MailTo='Peng.Tao@inventec.com.cn;Wang.FeiWF@inventec.com.cn;Cheng.Shao-jie@inventec.com.cn';  
3. 但这几个人在公司mail address中找不到了

2020-02-11
-------------
#### VSCode 列选择(column select)功能在rdp时不管用解决办法
1. 文件->首选项->快捷方式
2. 找到 "cursorColumnSelectDown", 点击左边的铅笔Icon, 弹出修改界面
3. 我改为Ctrl+Shift+DownArror, 即去掉了Alt. 会与另一个功能的hotkey重合, 但可以用,不影响;
 

2020-02-12
-------------
#### Python 笔记
逗号赋值概念
   - 等号左边可以是多个变量,右边结果应该是多个返回, 分别赋给左边的变量
   - https://blog.csdn.net/wang_weina/article/details/69361641
   ```python
   rv, data = M.login(EMAIL_ACCOUNT, 'j2i7a1N8g')
   ```
文件名带中文, open报错
   ```python
   book = xlrd.open_workbook("d:\SHELF\EB\xinyang_ict\1 资料\APS-430 2019.10.12\APS-430 2019.10.12#1.xls")
                                ^
   SyntaxError: (unicode error) 'unicodeescape' codec can't decode bytes in position 11-12: truncated \xXX escape
   ```
   - 解决: prefix the string with r (to produce a raw string)   
   - https://stackoverflow.com/questions/1347791/unicode-error-unicodeescape-codec-cant-decode-bytes-cannot-open-text-file

2020-02-17
----------
#### VSCode 设置语言(中文)
1. Ctrl+shift+P 进入命令区
2. 输入 "configure display language"
3. 选择 "zh-cn"

2020-02-18
----------
