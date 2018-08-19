## 怎么在一台树莓派上安装Postgres数据库

本教程介绍了怎么在一个树莓派上去安装 Postgres；创建一个表；写简单查询；在树莓派、PC，或者 Mac 上使用 pgAdmin 图形用户界面；从 Python 中与数据库交互。

作者：Ben Nuttall来源：[Linux中国](https://linux.cn/article-9056-1.html)|_2017-11-23 08:30_

[![怎么在一台树莓派上安装Postgres数据库](http://s3.51cto.com/oss/201711/22/4cabfb132e5d927f0baa737b3b725a9d.png-wh_651x-s_2204032566.png "怎么在一台树莓派上安装Postgres数据库")](http://s3.51cto.com/oss/201711/22/4cabfb132e5d927f0baa737b3b725a9d.png-wh_651x-s_2204032566.png)

在你的下一个树莓派项目上安装和配置流行的开源数据库 Postgres 并去使用它。

保存你的项目或应用程序持续增加的数据，数据库是一种很好的方式。你可以在一个会话中将数据写入到数据库，并且在下次你需要查找的时候找到它。一个设计良好的数据库可以做到在巨大的数据集中高效地找到数据，只要告诉它你想去找什么，而不用去考虑它是如何查找的。为一个基本的 CRUD （创建、记录、更新、删除）应用程序安装一个数据库是非常简单的， 它是一个很通用的模式，并且也适用于很多项目。

为什么 PostgreSQL 一般被为 Postgres？ 它被认为是功能和性能最好的开源数据库。如果你使用过 MySQL，它们是很相似的。但是，如果你希望使用它更高级的功能，你会发现优化 Postgres 是比较容易的。它便于安装、容易使用、方便安全， 而且在树莓派 3 上运行的非常好。

本教程介绍了怎么在一个树莓派上去安装 Postgres；创建一个表；写简单查询；在树莓派、PC，或者 Mac 上使用 pgAdmin 图形用户界面；从 Python 中与数据库交互。

你掌握了这些基础知识后，你可以让你的应用程序使用复合查询连接多个表，那个时候你需要考虑的是，怎么去使用主键或外键优化及最佳实践等等。

**安装**

一开始，你将需要去安装 Postgres 和一些其它的包。打开一个终端窗口并连接到因特网，然后运行以下命令：

1. >sudo apt install postgresql libpq-dev postgresql-client 
2. >  
3. >postgresql-client-common -y 

[![installing postgres](http://s1.51cto.com/oss/201711/22/9a0fade6fc8f33093d7db26169ea1513.png-wh_600x-s_2292993688.png "installing postgres")](http://s1.51cto.com/oss/201711/22/9a0fade6fc8f33093d7db26169ea1513.png-wh_600x-s_2292993688.png)

installing postgres

当安装完成后，切换到 Postgres 用户去配置数据库：

> 1.  sudo su postgres 

现在，你可以创建一个数据库用户。如果你创建了一个与你的 Unix 用户帐户相同名字的用户，那个用户将被自动授权访问该数据库。因此在本教程中，为简单起见，我们将假设你使用了默认用户 pi 。运行 createuser 命令以继续：

> 1.  createuser pi -P --interactive 

当得到提示时，输入一个密码 （并记住它）， 选择 n 使它成为一个非超级用户（LCTT 译注：此处原文有误），接下来两个问题选择 y（LCTT 译注：分别允许创建数据库和其它用户）。

[![creating a postgres user](http://s5.51cto.com/oss/201711/22/b47569b83006e2cf244f7ab78869f4cb.png-wh_600x-s_3993708890.png "creating a postgres user")](http://s5.51cto.com/oss/201711/22/b47569b83006e2cf244f7ab78869f4cb.png-wh_600x-s_3993708890.png)

creating a postgres user

现在，使用 Postgres shell 连接到 Postgres 去创建一个测试数据库：

1. > $ psql 
2. > 
3. >&gt;**create  database** test; 

按下 Ctrl+D 两次从 psql shell 和 postgres 用户中退出，再次以 pi 用户登入。你创建了一个名为 pi 的 Postgres 用户后，你可以从这里无需登录凭据即可访问 Postgres shell：

1.  >$ psql test 

你现在已经连接到 "test" 数据库。这个数据库当前是空的，不包含任何表。你可以在 psql shell 里创建一个简单的表：

1.  test=> create  table people (name text, company text); 

现在你可插入数据到表中：

1.  test=> insert  into people values ('Ben Nuttall', 'Raspberry Pi Foundation'); 

3.  test=> insert  into people values ('Rikki Endsley', 'Red Hat'); 

然后尝试进行查询：

1.  test=> select * from people; 

3.   name |         company 

5.  ---------------+------------------------- 

7.   Ben Nuttall   | Raspberry Pi Foundation 

9.   Rikki Endsley | Red Hat 

11.  (2 rows) 

[![a postgres query](http://s5.51cto.com/oss/201711/22/0791468dd687b5bbe56dceda2c32b9ca.png-wh_600x-s_3589010324.png "a postgres query")](http://s5.51cto.com/oss/201711/22/0791468dd687b5bbe56dceda2c32b9ca.png-wh_600x-s_3589010324.png)

a postgres query

1.  test=> select  name  from people where company = 'Red Hat'; 

3.   name | company 

5.  ---------------+--------- 

7.   Rikki Endsley | Red Hat 

9.  (1 row) 

**pgAdmin**

如果希望使用一个图形工具去访问数据库，你可以使用它。 PgAdmin 是一个全功能的 PostgreSQL GUI，它允许你去创建和管理数据库和用户、创建和修改表、执行查询，和如同在电子表格一样熟悉的视图中浏览结果。psql 命令行工具可以很好地进行简单查询，并且你会发现很多高级用户一直在使用它，因为它的执行速度很快 （并且因为他们不需要借助 GUI），但是，一般用户学习和操作数据库，使用 pgAdmin 是一个更适合的方式。

关于 pgAdmin 可以做的其它事情：你可以用它在树莓派上直接连接数据库，或者用它在其它的电脑上远程连接到树莓派上的数据库。

如果你想去访问树莓派，你可以用 apt 去安装它：

1.  sudo apt install pgadmin3 

它是和基于 Debian 的系统如 Ubuntu 是完全相同的；如果你在其它发行版上安装，尝试与你的系统相关的等价的命令。 或者，如果你在 Windows 或 macOS 上，尝试从 pgAdmin.org 上下载 pgAdmin。注意，在 apt 上的可用版本是 pgAdmin3，而最新的版本 pgAdmin4，在其网站上可以找到。

在同一台树莓派上使用 pgAdmin 连接到你的数据库，从主菜单上简单地打开 pgAdmin3 ，点击 new connection 图标，然后完成注册，这时，你将需要一个名字（连接名，比如 test），改变用户为 “pi”，然后剩下的输入框留空 (或者如它们原本不动）。点击 OK，然后你在左侧的侧面版中将发现一个新的连接。

[![connect your database with pgadmin](http://s2.51cto.com/oss/201711/22/04a22b2cefe26532eae0b442bb3b745f.png "connect your database with pgadmin")](http://s2.51cto.com/oss/201711/22/04a22b2cefe26532eae0b442bb3b745f.png)

connect your database with pgadmin

要从另外一台电脑上使用 pgAdmin 连接到你的树莓派数据库上，你首先需要编辑 PostgreSQL 配置允许远程连接：

1、 编辑 PostgreSQL 配置文件 /etc/postgresql/9.6/main/postgresql.conf ，取消 listen_addresses 行的注释，并把它的值从 localhost 改变成 *。然后保存并退出。

2、 编辑 pg_hba 配置文件 /etc/postgresql/9.6/main/postgresql.conf，将 127.0.0.1/32 改变成 0.0.0.0/0 （对于IPv4）和将 ::1/128 改变成 ::/0 （对于 IPv6）。然后保存并退出。

3、 重启 PostgreSQL 服务： sudo service postgresql restart。

注意，如果你使用一个旧的 Raspbian 镜像或其它发行版，版本号可能不一样。

[![edit the postgresql configuration to allow remote connections](http://s3.51cto.com/oss/201711/22/85ccb824ca57e503f31657abf937d168.png "edit the postgresql configuration to allow remote connections")](http://s3.51cto.com/oss/201711/22/85ccb824ca57e503f31657abf937d168.png)

edit the postgresql configuration to allow remote connections

做完这些之后，在其它的电脑上打开 pgAdmin 并创建一个新的连接。这时，需要提供一个连接名，输入树莓派的 IP 地址作为主机（这可以在任务栏的 WiFi 图标上悬停鼠标找到，或者在一个终端中输入 hostname -I 找到）。

[![a remote connection](http://s3.51cto.com/oss/201711/22/99ce620e3a026ebbda7bf324cd1856fa.png "a remote connection")](http://s3.51cto.com/oss/201711/22/99ce620e3a026ebbda7bf324cd1856fa.png)

a remote connection

不论你连接的是本地的还是远程的数据库，点击打开 Server Groups > Servers > test > Schemas > public > Tables，右键单击 people 表，然后选择 View Data > View top 100 Rows。你现在将看到你前面输入的数据。

[![viewing test data](http://s2.51cto.com/oss/201711/22/0eb54492d47f839c4dca48e62ccb0abc.png "viewing test data")](http://s2.51cto.com/oss/201711/22/0eb54492d47f839c4dca48e62ccb0abc.png)

viewing test data

你现在可以创建和修改数据库和表、管理用户，和使用 GUI 去写你自己的查询了。你可能会发现这种可视化方法比命令行更易于管理。

**Python**

要从一个 Python 脚本连接到你的数据库，你将需要 Psycopg2 这个 Python 包。你可以用 pip 来安装它：

1.  sudo pip3 install psycopg2 

现在打开一个 Python 编辑器写一些代码连接到你的数据库：

1.  import psycopg2 

3.   conn = psycopg2.connect('dbname=test') 

5.   cur = conn.cursor() 

7.   cur.execute('select * from people') 

9.   results = cur.fetchall() 

11.   for result in results: 

13.   print(result) 

运行这个代码去看查询结果。注意，如果你连接的是远程数据库，在连接字符串中你将需要提供更多的凭据，比如，增加主机 IP、用户名，和数据库密码：

1.  conn = psycopg2.connect('host=192.168.86.31 user=pi 

3.  password=raspberry dbname=test') 

你甚至可以创建一个函数去运行特定的查询：

1.  def get_all_people(): 

3.   query = """ 

5.   SELECT 

7.   * 

9.   FROM 

11.   people 

13.   """ 

15.   cur.execute(query) 

17.   return cur.fetchall() 

和一个包含参数的查询：

1.  def get_people_by_company(company): 

3.   query = """ 

5.   SELECT 

7.   * 

9.   FROM 

11.   people 

13.   WHERE 

15.   company = %s 

17.   """ 

19.   values = (company, ) 

21.   cur.execute(query, values) 

23.   return cur.fetchall() 

或者甚至是一个增加记录的函数：

1.  def add_person(name, company): 

3.   query = """ 

5.   INSERT  INTO 

7.   people 

9.   VALUES 

11.   (%s, %s) 

13.   """ 

15.   values = (name, company) 

17.   cur.execute(query, values) 

注意，这里使用了一个注入字符串到查询中的安全的方法， 你不希望被 小鲍勃的桌子 害死！

[![Python](http://s5.51cto.com/oss/201711/22/bd0ea083be96f561c2421b3de8ef6b85.png "Python")](http://s5.51cto.com/oss/201711/22/bd0ea083be96f561c2421b3de8ef6b85.png)

Python

现在你知道了这些基础知识，如果你想去进一步掌握 Postgres ，查看在 Full Stack Python 上的文章。

（题图：树莓派基金会）
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY4MzYyMjQxMCwtMTk0MzA0MzY3MV19
-->