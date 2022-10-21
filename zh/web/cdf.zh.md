{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - 频道定义格式",
  "description" :"了解什么是 CDF 文件以及可以创建和打开 CDF 文件的 API。",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## 什么是一 .cdf 文件？

扩展名为 .cdf 的文件是一种基于 XLM 的信息分发文件格式，用于将频繁更新发布为“通道"。信息从任何网络服务器发布，并自动传送到具有兼容接收程序（如网络浏览器）的计算机。用户订阅活动频道并将预定更新发送到他们的桌面。
CDF 文件早期与 Microsoft 的 Active Channel、Active Desktop 和 Smart Offline Favorites 技术结合使用。

## CDF 文件格式

CDF 文件保存为 XML 文件，这是一种用于信息交换的通用 Web 文件格式。 CDF 文件格式现在是一种旧格式，从未被广泛采用。与此相比，Netscape 的 RSS 更为著名和广泛使用。

### CDF 文件格式示例

以下是 CDF 文件格式的通用示例。

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://域名/文件夹/"
LASTMOD="1998-11-05T22:12"
前兆=“是"
水平=“0">
<TITLE>频道名称</TITLE>
<ABSTRACT>频道内容概要。</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    前兆=“是"
水平=“1">
<TITLE>第二页的标题</TITLE>
<ABSTRACT>第二页内容概要。</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## 参考

* [频道定义格式 - 由维基百科提供](https://en.wikipedia.org/wiki/Channel_Definition_Format)

