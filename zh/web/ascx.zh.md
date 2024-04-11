{
  "date" : "2019-10-11",
  "keywords" :["ascx","ascx 文件","ascx 文件格式","ascx 文件类型","文件","类型","什么是 ascx 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASCX 文件格式",
  "description" :"了解什么是 ASCX 文件以及可以创建和打开 ASCX 文件的 API。",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## 什么是一 .asx 文件？

扩展名为 .ascx 的文件是一种用户控件，在网页中用作可重用组件。它在任何 ASP 网站中通过将其从控制框拖动到页面来引用。 ASCX 用户控件作为中央源添加到项目中，导致用户控件的任何更改都会反映在整个网站上。与定义通过 Internet 在 2 个对象内进行通信的机制的 ASMX 文件不同，ASCX 文件是用于嵌入页面或网站的用户控件。

## ASCX 文件格式

ASCX 文件以纯文本格式编写，并且可以使用代码隐藏功能，例如以 .ascx.cs 结尾的网页。用户控件的标记代码以@Control 指令开头，如下例所示。

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

此 Web 用户控件可以在许多页面上重复使用，例如页脚、页眉或某种网站导航。 Web 用户控件与任何其他控件一样具有属性、方法和事件，这使得它们在设置其视觉行为时很有用。

### 在 web.config 中注册用户控件的示例

为了在多个页面上使用单个用户控件，可以在 web.config 中注册 Web 控件。这允许使用对所有网站的控制，而不是单独在每个页面上注册。下面的示例代码定义了如何在 web.config 中注册一个 Web 控件以在整个网站上显示为页脚。

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## 参考

* [ASCX 用户控制](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

