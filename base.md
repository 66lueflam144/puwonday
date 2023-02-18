just record what i don't know and need to know



### 一个大致的<a href="https://zhuanlan.zhihu.com/p/268095343">安全术语</a>

### **what's the WEB**
>即全球广域网World Wide Web，也称万维网。
建立在Internet上的一种网络服务，其中的文档及超链接将Internet上的信息节点组织成一个互为关联的网状结构。


### **协议**
>规定好的通讯、交流方式。（类似语法）

### **WEB安全**
>前端、后端、协议、数据库的安全

### **服务器**
>一台电脑（？）

### **IP地址、端口**
>IP地址是指互联网协议地址，全球唯一<br>端口是每一个软件的一个通讯进出口。

### **各种网**
>局域网：Local Area Network<br>
广域网:Metropolitan Area Network<br>
内网、
外网

### **URL、MAC**
>URL：统一资源定位符<br>MAC：介质访问控制符，全球唯一性

### **桥接、NAT**
>桥接：虚拟机和主机是平级关系<br>NAT：虚拟机和主机是父子关系

### **正/反向shell**
>正向：黑客主动链接受害者<br>反向：受害者主动连接黑客


>字典指一系列密码

### **cookie/session**
>cookie数据存放在客户端<br>session数据存放在服务端<br>（其实就是一个保存状态的文件或者数据）

### **ByPass、0Day漏洞**
>绕过<br>最新产生的漏洞。

### **渗透、后渗透、攻击工具**
攻击。<br>攻击完成后建立持续连接。


  - Kali
  - Sqlmap
  - Burpsuite





# 基础1（常见网络设备）

---
---

### **网卡、网关、网桥**
>网卡，电脑硬件<br>网关，网络关口<br>网桥，也称桥接器，连接两个局域网的一种储存/转发设备，常用于扩展局域网。可以是专门硬件设备也可以是计算机加装的软件。

### 防火墙
一个<a href="https://blog.csdn.net/networktp/article/details/122658292?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167669538816782425614437%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167669538816782425614437&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-122658292-null-null.142^v73^insert_down2,201^v4^add_ask,239^v2^insert_chatgpt&utm_term=%E9%98%B2%E7%81%AB%E5%A2%99&spm=1018.2226.3001.4187">防火墙知识的整理</a>

### **虚拟机、Docker**
>虚拟机，虚拟出另一个系统<br>Docker，容器



### **靶机、DVWA、CMS**
>靶机就是搭建好漏洞测试环境的计算机<br>DVMA:漏洞集合软件<br>CMS是内容管理系统，也称**后台**

### 交换机、路由器

- 交换机：
  - 局域网交换机：组织局域网，用于连接终端设备。
  - 广域网交换机：应用于电信领域，提供通信基础平台。
- 路由器：连接两个或多个网络的硬件设备，在网络间起网关的作用，是读取每一个数据包中的地址然后决定如何传送的专用智能性的网络设备。
- ps:
  - <a href="https://www.cnblogs.com/wangchengshi/p/14049891.html">路由器和交换机的罗曼史</a>

### VPN服务器

<a href="https://www.jianshu.com/p/6f228390be22">VPN or VPS</a>

----
----


# 基础2（网络协议）

### 应用层


---

#### http/https

- <font color=red>**http**（超文本传输协议）</font>：<br>
  - 是一种用于分布式、协作式和超媒体信息系统的应用层协议。 简单来说就是一种发布和接收 HTML 页面的方法，被用于在 Web 浏览器和网站服务器之间传递信息。<br>
  - HTTP 协议以明文方式发送内容，不提供任何方式的数据加密，如果攻击者截取了Web浏览器和网站服务器之间的传输报文，就可以直接读懂其中的信息，因此，HTTP协议不适合传输一些敏感信息
- <font color=red>**https**（超文本传输安全协议）</font>：<br>
  - 是一种透过计算机网络进行安全通信的传输协议。HTTPS 经由 HTTP 进行通信，但利用 SSL/TLS 来加密数据包。HTTPS 开发的主要目的，是提供对网站服务器的身份认证，保护交换数据的隐私与完整性。
  
<a href="https://www.runoob.com/w3cnote/http-vs-https.html">关于http/https区别的具体内容</a>

----

#### DNS
>域名系统，因特网上作为域名和IP地址互相映射的一个分布式数据库。<br>

（通过主机名最终得到该主机对应的IP地址的过程称为域名解析）

- DNS系统的作用：
  - <font color=green>正向解析</font>：根据主机名称（域名）查找对应的IP地址
  - <font color=green>反向解析</font>：根据IP地址查找对应的主机域名

<a href="https://blog.csdn.net/qq_31930499/article/details/79767330">a thing about DNS</a>

----

#### FTP
>TCP/IP协议组中的协议之一。<br>由<br>
- <font color=red>FTP服务器</font>:存储文件，用户可以使用FTP客户端通过FTP协议访问位于FTP服务器上的资源。
- <font color=red>FTP客户端</font>

二者组成FTP协议。

<a href="https://www.jianshu.com/p/d764b68516df">具体的</a>

----

#### SSH
一种网络协议，用于计算机之间的加密登录。
<a href="https://blog.csdn.net/u013452337/article/details/80847113">click this to learn more</a>

----

### 传输层

#### TCP
传输控制协议，一种面向连接的、基于字节流的传输层通信协议。

---

#### UDP
用户数据报协议，是OSI（Open System Interconnection，开放式系统互联） 参考模型中一种无连接的传输层协议，提供面向事务的简单不可靠信息传送服务。

----

#### 上面两个东西的一些其他事

>UDP协议与TCP协议一样用于处理数据包，在OSI模型中，两者都位于传输层，处于IP协议的上一层。
UDP有不提供数据包分组、组装和不能对数据包进行排序的缺点，也就是说，当报文发送之后，是无法得知其是否安全完整到达的。
UDP用来支持那些需要在计算机之间传输数据的网络应用。包括网络视频会议系统在内的众多的客户/服务器模式的网络应用都需要使用UDP协议。
UDP协议从问世至今已经被使用了很多年，虽然其最初的光彩已经被一些类似协议所掩盖，但即使在今天UDP仍然不失为一项非常实用和可行的网络传输层协议。


-----
----

### 网络层

#### IP
TCP/IP体系中网络层协议。
- IP编址方案
- 分组封装格式
- 分组转发规则
  
----


### web通信流程

- 1.建立TCP连接
  :arrow_down:
- 2.web浏览器向web服务器发送请求行
  :arrow_down:
- 3.web浏览器向服务器发送请求头
  :arrow_down:
- 4.web服务器应答
  :arrow_down:
- 5.web服务器发送应答头
  :arrow_down:
- 6.web服务器发送数据
  :arrow_down:
- 7.web服务器关闭TCP连接

----

#### web常见编码

- ASCII编码
- URL编码
  - URL:<br>`scheme:[//[user[:password]@]host[:port]][/path][?query][#fragment]`即`[协议类型]://[用户名[:密码]]@[服务器地址]:[端口号]/[资源层级UNIX文件路径][文件名]?[查询]#[片段ID]`
  - 任何URL编码的字符都以`%`作为前缀。
- Unicode编码（与ASCII编码不兼容但可以转换）
- HTML编码
- Base编码
  - Base16
  - Base32
  - Base64

<a href="https://blog.csdn.net/lady_killer9/article/details/112167885">具体</a>
