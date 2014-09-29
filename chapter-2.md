# 2、相关理论与文献综述
## 2.1 相关概念和理论回顾
### 2.1.1 [MVC模式](http://zh.wikipedia.org/wiki/MVC)
　　MVC模式(Model-View-Controller)是软件工程中的一种软件架构模式，把软件系统分为三个基本部分：模型(Model)、视图(View)和控制器(Controller)。
　　MVC模式最早由 Trygve Reenskaug 在1978年提出，是施乐帕罗奥多研究中心(Xerox PARC)在20世纪80年代为程序语言 Smalltalk 发明的一种软件设计模式。
MVC模式的目的是实现一种动态的程序设计，使后续对程序的修改和扩展简化，并且使程序某一部分的重复利用成为可能。
除此之外，此模式通过对复杂度的简化，使程序结构更加直观。
软件系统通过对自身基本部分分离的同时也赋予了各个基本部分应有的功能。
专业人员可以通过自身的专长分组：
* 控制器 (Controller) - 负责转发请求，对请求进行处理。
* 视图 (View) - 界面设计人员进行图形界面设计。
* 模型 (Model) - 程序员编写程序应有的功能(实现算法等等)、数据库专家进行数据管理和数据库设计(可以实现具体的功能)。

### 2.1.2 [REST 设计风格](http://zh.wikipedia.org/wiki/REST)

　　REST 含状态传输（英文：Representational State Transfer，简称REST）是 Roy Fielding 博士在2000年他的博士论文中提出来的一种软件架构风格。
目前在三种主流的 Web 服务实现方案中，因为 REST 模式与复杂的 SOAP 和 XML-RPC 相比更加简洁，越来越多的 web 服务开始采用 REST 风格设计和实现。

#### 含状态传输的 Web 服务 (RESTful Web Services)

　　含状态传输的 Web 服务 (RESTful Web Services)是一个使用 HTTP 并遵循 REST 原则的 Web 服务。
它从以下三个方面资源进行定义：
* 直观简短的资源地址：URI ，比如：http://jeremylinstore.herokuapp.com/products/。
* 传输的资源： Web 服务接受与返回的互联网媒体类型，比如：JSON，XML ，YAML 等。
* 对资源的操作： Web 服务在该资源上所支持的一系列请求方法（比如：POST，GET，PUT 或 DELETE）。
下表列出了在实现含状态传输的 Web 服务时HTTP请求方法的典型用途。

<table border="1">
    <caption><b>HTTP 请求方法在 RESTful Web 服务中的典型应用</b></caption>
    <tr>
        <th>资源</th>
        <th>GET</th>
        <th>PUT</th>
        <th>POST</th>
        <th>DELETE</th>
    </tr>

    <tr>
        <th>一组资源的URI，比如<code><a href="http://jeremylinstore.herokuapp.com/products/">http://jeremylinstore.herokuapp.com/products/</a></code></th>
        <td><b>列出</b> URI，以及该资源组中每个资源的详细信息（后者可选）。</td>
        <td>使用给定的一组资源<b>替换</b>当前整组资源。</td>
        <td>在本组资源中<b>创建/追加</b>一个新的资源。 该操作往往返回新资源的URL。</td>
        <td><b>删除</b> 整组资源。</td>
    </tr>
    
    <tr>
        <th>单个资源的URI，比如<code><a href="http://jeremylinstore.herokuapp.com/products/2/">http://jeremylinstore.herokuapp.com/products/2/</a></code></th>
        <td><b>获取</b> 指定的资源的详细信息，格式可以自选一个合适的网络媒体类型（比如：XML、JSON等）</td>
        <td><b>替换/创建</b> 指定的资源。并将其追加到相应的资源组中。</td>
        <td>把指定的资源当做一个资源组，并在其下<b>创建/追加</b>一个新的元素，使其隶属于当前资源。</td>
        <td><b>删除</b> 指定的元素。</td>
    </tr>
</table>

### 2.1.3 CRUD

　　CRUD 是指在做计算处理时的增加(Create)、读取(Retrieve)（重新得到数据）、更新(Update)和删除(Delete)几个单词的首字母简写。主要被用在描述软件系统中数据库或者持久层的基本操作功能。
　　在 Rails 程序中，REST 意味着大多数的组件会被模型化（如 Product, User, Category 等 ），变成资源（resource），可以被创建（create）、读取（read）、更新（update）和删除（delete），这些操作会与关系型数据库中的 CRUD 操作和 HTTP 请求方法（POST，GET，PATCH 和 DELETE）对应起来。

## 2.2文献综述
