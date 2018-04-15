---
layout:     post
title:      PHP runtime 组件
subtitle:   PHP runtime 组件
date:       2018-04-15
author:     bright
header-img: img/post-bg-coffee.jpeg
catalog: true
tags:
- 编程语言
- php
---

> 组件

### ampq  
Advanced Message Queuing Protocol 高级消息队列协议，异步消息传递，例如：RabbitMQ
AMQP publishers send to exchanges, which route messages to queues. Subscribers consume from the queues.
参考：
https://github.com/rabbitmq/rabbitmq-tutorials/blob/master/php-amqp/worker.php
http://www.cnblogs.com/lchb/articles/2889923.html


### apache
Apache HTTP Server  网页服务器,是最流行的Web服务器软件之一

参考：
https://wiki.archlinux.org/index.php
/Apache_HTTP_Server_(%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87)
http://www.jianshu.com/p/2fb9a3bb12f6


### apc
指APC把PHP文件源码的编译结果缓存起来，然后在每次调用时先对比时间标记。 
如果未过期，则使用缓存的中间代码运行。 默认缓存3600s(一小时)。 
但是这样仍会浪费大量CPU时间。

解决：因为php特性，每次执行完页面后，所有运行对象都会释放，
apc可以用于脚本，进程间共享，缓存数据

apc 是单机Cache，使用共享内存保存数据
memcache 实现多机共享，比如用于解决session共享问题

### apcu
apc的去掉opcode caching版本

### bcmath
二级制计算器

### bz2
bzip2 压缩解压组件

### calendar
日历组件

### Core
couchbase
面向文档的数据库，是基于 Membase 与 CouchDB 开发
Couchbase Server is an open source, distributed, NoSQL document-oriented engagement database
https://developer.couchbase.com/documentation/server/5.0/
introduction/intro.html

### csprng
密码学安全伪随机数生成器，常被作为密码学原件，用以搭建更复杂的密码学应用

### ctype
数据类型检测，比如字符，数字等

### cubrid
数据库组件

### curl
能够连接通讯各种服务器、使用各种协议，目前支持的协议有 http、https、ftp、gopher、telnet、dict、file等等

### date
日期组件

### dba
数据库抽象层，如pdo，odbc等

### dom（Document Object Model）
xml操作，libxml等

### enchant
国际化与字符编码支持

### Ev
pecl新增扩展，进程控制,提供libev接口，其接口和libevent基本类似，libev是libevent之后的一个事件驱动的编程框架
事件循环，IO复用，处理高并发网络连接问题
创建所需的网络监听套接字 -> 注册在执行期间要调用的事件 -> 启动主事件循环- > 让 libev 处理过程的其余部分
http://www.jianshu.com/p/3299e19d9bf4
http://blog.csdn.net/yusiguyuan/article/details/18274313
https://www.ibm.com/developerworks/cn/aix/library/au-libev/index.html


### exif
 图像处理
ffmpeg
 图像处理

### fileinfo
文件系统相关扩展

### filter
变量与类型相关扩展，变量检查，过滤

### ftp
文件服务

### gd
图像生成和处理
gearman
Gearman提供了一个通用的应用框架，将工作外包给其他更适合做这项工作的机器或过程。
它允许您并行地工作，负载平衡处理，并调用语言之间的函数。
它可以用于各种应用程序，从高可用性web站点到数据库复制事件的传输。
换句话说，它是分布式处理通信的神经系统。

geoip
 Geo IP 定位

gettext
国际化与字符编码支持
gmagick
图像生成和处理

gmp
数学扩展

gnupg
非文本内容的 MIME 输出

hash
加密扩展
http
http协议

ibm_db2
数据库扩展

iconv
国际化与字符编码支持

imagick
图像处理

imap
邮件相关扩展



inotify
文件系统相关扩展

interbase
ibase数据库

intl
国际化与字符编码支持
json
其它基本扩展
ldap
LDAP server  轻量目录访问协议，LDAP目录以树状的层次结构来存储数据


libevent
进程控制扩展，Libevent是一个库，它提供了一种机制，当某个特定事件发生或超时时，它将执行回调函数。


libsodium
进程控制扩展

libxml
XML 操作

mbstring
国际化与字符编码支持 

mcrypt 加密扩展
memcache
memcached
其它服务

meta
mime_magic

ming
	非文本内容的 MIME 输出

mongo
mongodb
		针对各数据库系统对应的扩展

mssql  MS SQL server connection
mysql  MySQL Server 已经废弃

mysqli

ncurses
针对命令行的扩展，实验性，未来被修改风险高
newrelic
服务器性能监控工具
https://ruby-china.org/topics/22379


oauth
web服务，提供 OAuth 消费方和提供方之间的绑定。OAuth 是一种建立在 HTTP 之上的授权协议，用于允许应用程序安全访问数据而无需存储用户名和密码


oci8
oracle数据库访问，支持sql，pl/sql
odbc
通用数据库访问组件，支持 Adabas D,IBM DB2,iODBC,Solid,Sybase SQL

opcache
OPcache 通过将 PHP 脚本预编译的字节码存储到共享内存中来提升 PHP 的性能， 存储预编译字节码的好处就是 省去了每次加载和解析 PHP 脚本的开销


openssl
加密扩展，用OpenSSL 库来对称/非对称加解密，以及 PBKDF2、 PKCS7、 PKCS12、 X509 和其他加密操作
password
加密，密码散列算法，

pcntl
进程控制，PHP的进程控制支持实现了Unix方式的进程创建, 程序执行, 信号处理以及进程的中断。 
进程控制不能被应用在Web服务器环境，当其被用于Web服务环境时可能会带来意外的结果


pcre
PDO
数据库访问组件，为PHP访问数据库定义了一个轻量级的一致接口，不管使用哪种数据库，都可以用相同的函数（方法）来查询和获取数据
pdo_ibm
pdo_mysql
pdo_pgsql
pdo_sqlite

pgsql
PostgreSQL 数据库扩展

Phar
	压缩与归档扩展

posix
POSIX，Portable Operating System Interface
是UNIX系统的一个设计标准，遵循这个标准的好处是软件可以跨平台
提供访问定义在POSIX.1中的函数的接口


pspell
国际化与字符编码支持 

pthreads
进程控制扩展
在 PHP 中使用多线程技术的面向对象的 API,提供全套工具。 
通过使用 Thread， Worker，Threaded 对象，PHP 应用可以创建、读取、写入以及执行多线程应用，
并可以在多个线程之间进行同步控制

readline
	针对命令行的扩展

recode
国际化与字符编码支持

redis

Reflection
变量与类型相关扩展,对类、接口、函数、方法和扩展进行反向工程的能力

regex
文本处理 , 正则表达式匹配
rrd
pecl/rrd扩展提供了对RRDtool C库的绑定。
RRDtool是开放源码行业标准、高性能数据日志记录和时间序列数据绘图系统。

session
一个访问者访问你的 web 网站将被分配一个唯一的 id, 就是所谓的会话 id. 
这个 id 可以存储在用户端的一个 cookie 中，也可以通过 URL 进行传递.

shmop
提供一系列方法，php用于读写，建，删 unix的共享内存模块

SimpleXML
提供了一个非常简单和易于使用的工具集，能将 XML 转换成一个带有一般属性选择器和数组迭代器的对象

snmp
Simple Network Management Protocol
提供了一个非常简单和易于使用的工具集，能将通过简单网络管理协议来管理远程设备

soap
SOAP扩展可以用来编写SOAP服务器和客户端

sockets
Socket扩展实现了和socket通讯功能的底层接口，它可以和客户端一样当做一个socket服务器。
比如：构建简单的TCP/IP 客户端/服务器端


SPL
用于解决典型问题(standard problems)的一组接口与类的集合。
数据结构,迭代器(foreach等处理),接口,异常,SPL 函数,文件处理,各种类及接口

SplType
帮助人们使PHP成为一种更强的类型语言，并且可以成为标量类型提示的一个很好的替代品。它提供了不同的类型处理类，如整数、浮点数、bool、enum和字符串

SQLite
 数据库扩展，应用场景：需要数据库的小工具软件，一般用于对并发数量要求不高的本地查询，比如 个人博客（WordPress支持SQLite3）、本地工具软件、嵌入式系统用数据库（Android） 

sqlite3
实现与 SQLite 3 数据库对接的类。


sqlsrv
Microsoft SQL Server Driver for PHP ,allows you to access Microsoft SQL Server 
and SQL Azure databases when running PHP on Windows. 


ssh2
Secure Shell2,绑定到libssh2库，该库使用安全的加密传输，
提供对在远程机器上资源的访问(shell、远程exec、隧道、文件传输)。


standard
基本扩展 

suhosin
superglobals
对于全部脚本而言，PHP 提供了大量的预定义变量。
这些变量表示包含：从外部变量到内建环境变量，从最后一个错误消息到最后一个检索的头的所有内容。
比如：$_SESSION,$_SERVER,$_GET,$_POST,$GLOBALS

svn
该扩展实现了对Subversion(SVN)的PHP绑定，这是一个版本控制系统，
允许PHP脚本与SVN存储库通信

sybase
sybase数据库相关

sysvmsg
进程扩展，Semaphore, Shared Memory and IPC，
这个模块为System V IPC系列提供了包装器。它包括信号量、共享内存和进程间消息传递(IPC)。

sysvsem  进程扩展
sysvshm  进程扩展
tidy  HTML文档相关

tokenizer
提供访问在Zend引擎中嵌入的PHP标记器的接口,php源码解析

wddx   XML 操作 

wincache
Windows Cache for PHP
PHP的Windows缓存扩展是一个PHP加速器，用于提高在Windows和Windows服务器上运行的PHP应用程序的速度

xcache XCache是一个开源的 opcode 缓存器/优化器。

xdebug  

xhprof XHProf是一个轻量级的分层结构和基于仪表的分析器。
xml  XML 解析器 
xmlreader
xmlrpc   用来编写xml-rpc服务器和客户端。
xmlwriter
xsl   XSL扩展实现了XSL标准
yaml
扩展实现了(YAML) 数据序列化标准。 通过LibYAML 来解析和编码
zend   http://php.net/manual/en/internals2.ze1.zendapi.php
ZendCache
ZendDebugger
ZendUtils
zip  读写ZIP压缩文档以及它们里面的文件。
zlib 能够透明地读取和写入gzip(.gz)压缩文件
zmq   是一个能让你快速设计、开发基于消息应用的函数库
