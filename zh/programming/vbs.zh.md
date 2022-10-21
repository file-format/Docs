{
  "date" : "2021-08-24", 
  "keywords" :["vbs","文件","扩展名","文件格式","Visual Basic 脚本","编程指南","vbs 示例","Microsoft Visual Basic","VBScript"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Visual Basic 脚本文件",
  "description":"了解 VBS 文件格式和可以创建和打开 VBS 文件的 API。",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## 什么是一 .vbs 文件？

VBS 或 VBScript 与 Microsoft Visual Basic 的脚本版本相连。在计算环境中，允许用户访问和控制它的许多方面。允许 VBScript 使用名为 **Component Object Model** 的模型来利用环境的元素和工具。此环境是为工作和运行 VBScript 指定的。

在 Web 开发领域被客户端访问时，它的作用类似于 Javascript。服务器也使用它来处理网页。它可以在一些其他类型的脚本文件中考虑，例如 [HTML](/zh/web/html/) 的应用程序。


## 历史简介 ＃＃

它于 1996 年首次推出，作为 Microsoft 指定用于 Windows 脚本的技术的一部分。它最初是为了帮助 Web 开发人员而专门开发的。同年，Microsoft Windows 的资源管理器 Internet Explorer 与 Visual Basic Script 的功能一起发布。

随着技术和 Web 开发的进步，许多版本的 VBScript 以及许多高级功能被推出。此外，在来年，这种脚本语言将成为 Microsoft Windows 的一部分，并具有新功能。

## 技术规格##

对于服务器端的网页，**Active Server Pages** 等工具与 VBScript 一起使用。这种脚本语言也可以用在 Windows 的脚本组件中。这种语言的文件在 Windows 中以 .vbs 扩展名存储。

该语言的代码中使用了许多控制结构，例如循环。它还包括命令行参数，可以命名或未命名。这种语言的文件可以简单地存储在文件夹中或 Windows 操作系统的桌面上。尽管没有像 Microsoft Script Editor 这样的 VBScript 程序的特定集成开发环境提供了开发这种语言的便利。

当 VBScript 由 Windows 的脚本宿主托管时，它提供了各种脚本语言非常常见但在 Visual Basic 6.0 中不可用的功能。涉及简单或直接访问的功能包括网络打印机、未命名和命名的命令行参数、标准输出和标准输入、网络共享、Windows 管理规范、网络的用户信息（如组成员身份）等等。

## VBS 文件格式示例 ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## 参考 ＃＃

* [VBS - 维基百科](https://en.wikipedia.org/wiki/VBScript)



