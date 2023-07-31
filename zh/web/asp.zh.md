{
  "date" : "2019-10-11",
  "keywords" :["asp","asp文件","asp文件格式","asp文件类型","文件","类型","什么是asp文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Active Server Pages 文件格式",
  "description" :"了解什么是 ASP 文件以及可以创建和打开它们的 API。",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .asp 文件？

ASP 代表 Active Server Pages，它是一种用于创建网页的开发框架。它使计算机代码能够由内部服务器执行以服务 Web 请求。当 Web 浏览器对 ASP 文件产生请求时，服务器会读取该文件并执行其中的任何代码/脚本以生成 **[HTML](/zh/web/html/)** 结果返回给浏览器进行显示。

与由服务器提供的静态页面的 HTML 页面不同，ASP 文件在运行时生成动态内容，其中可能涉及对来自数据库的数据的请求。 ASP 页面通常使用 .asp 扩展名而不是 .html。由于 ASP 文件中的代码/脚本在服务器端执行，请求浏览器无法看到用于构建服务页面的代码。所有现代浏览器都能够显示作为结果生成的页面。基于 Microsoft 技术构建的使用 ASP 构建的页面托管在 Microsoft Internet 信息服务 (IIS) 服务器上。

## ASP 文件格式简史
ASP 只经历了几次修订，它被 ASP.NET 取代，这是一种更现代、更有效的开发和管理服务器端页面的方式。默认情况下包括对 ASP 的支持以及 Internet 信息服务 (IIS)。 ASP 以三个不同的版本发布，每个版本都有改进。

* ASP 1.0 于 1996 年 12 月作为 IIS 3.0 的一部分发布
* ASP 2.0 于 1997 年 9 月作为 IIS 4.0 的一部分发布
* ASP 3.0 于 2000 年 11 月作为 IIS 5.0 的一部分发布

## ASP 功能对象

ASP 文件使用服务器端对象来处理用户请求并生成提供给用户的输出页面。每个对象都有一组用于处理请求和响应的集合、属性和方法。这些对象包括：

### 请求对象

当浏览器向服务器请求页面时，称为请求。 Request 对象用于从访问者那里获取信息。

### 响应对象

ASP Response 对象用于从服务器向用户发送输出。

### 服务器对象

ASP Server 对象用于访问服务器上的属性和方法。它允许连接到数据库 (ADO)、文件系统和使用安装在服务器上的组件。

### 会话对象

会话对象就像用户浏览器向服务器请求页面和服务器本身之间的链接。这是通过 ASP 创建并发送到用户计算机的 cookie 来实现的。 Session 对象存储有关用户会话的信息或更改设置。信息存储在 Session 对象中，在应用程序的所有页面之间共享。存储在会话变量中的常见信息是名称、id 和首选项。服务器为每个新用户创建一个新的 Session 对象，并在会话到期时销毁该 Session 对象。

### 应用程序对象

Application 对象包含将被应用程序中的许多页面使用的信息（如数据库连接信息）。可以从任何页面访问该信息。信息也可以在一处更改，更改将自动反映在所有页面上。 Application 对象用于存储和访问来自任何页面的变量，就像 Session 对象一样。

### ASPError 对象

ASPError 对象在 ASP 3.0 中实现，在 IIS5 及更高版本中可用。ASPError 对象用于显示 ASP 页面中脚本中发生的任何错误的详细信息。

**注意：** ASPError 对象是在调用Server.GetLastError 时创建的，因此只能通过Server.GetLastError 方法访问错误信息。

## 参考

* [ASP - W3C](https://www.w3schools.com/asp/default.asp)
* [创建简单的 ASP 页面](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

