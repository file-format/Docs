{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - iCalendar 文件格式",
  "description":"了解 ICS 文件格式和可以创建和打开 ICS 文件的 API。",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .ICS 文件？

Internet 日历和调度核心对象规范 (iCalendar) 是用于交换和部署日历事件和调度的 Internet 标准 (RFC 2445)。 iCalendar 格式是可互操作的，从而确保在具有不同电子邮件应用程序的用户之间交换日历信息。 iCalendar 将输入数据格式化为多用途 Internet 邮件扩展 (MIME)，并促进通过不同传输协议交换对象。这些传输协议可以是 SMTP、HTTP、点对点异步通信和基于物理媒体的网络传输。

iCalendar 允许用户通过电子邮件将事件、日期/时间相关任务和忙/闲信息分享给可以回复的其他用户。 iCalendar 文件存储使用后缀“.ics"、“.iCalendar"或“.ifb"，MIME 类型为“text/calendar"。 iCalendar 保持独立，没有任何传输协议依赖。 Web 服务器（使用 HTTP 协议）可以传输 iCalendar 信息，并且网页可以使用 iCalendar 以嵌入形式包含 iCalendar 数据。

## ICS 文件格式简史

1998 年，互联网工程任务组 (IETF) 将 iCalendar 定义为标准 (RFC 2445)。该标准由 Frank Dawson（Lotus Notes Corporation）和 Derik Stenerson（Microsoft）记录。 2009 年，Bernard Desruisseaux (Oracle) 再次将该标准改进为 RFC 5545。这次添加了一些新特性，弃用了一些过时的特性。 2016 年，RFC 7986 发布并扩充到原始 iCalendar RFC。 RFC 7986 为主要 VCALENDAR 对象添加了新特性，并且还为会议系统引入了新的支持特性。

## ICS 文件格式##

iCalendar 的数据使用的 MIME 类型是“文本/日历"。 iCalendar 的默认字符集是 UTF-8，但是通过在 MIME 中提供参数，可以使用不同的字符集。一个 iCalendar 文件包含部分，在这些部分中，“VCALENDAR"是封装所有其他部分的全局部分。 VEVENT 部分定义事件，VTODO 列出所有待办事项，VJOURNAL 包含日记条目，VTIMEZONE 指定时区信息。允许多个类似类别的部分。对于许多事件，iCalendar 文件中可以存在多个 VEVENT 部分。

### 内容行###

iCalendar 对象排列成不同的文本行“内容行"。在这种文件格式中，CRLF 序列终止一行，而行的长度限制为 75 个八位字节，不包括换行符。一个长数据项可以跨越多行。

### 列表和字段分隔符###

属性和参数指定由逗号字符分隔的值列表。带引号的字符串用于基于 URI 的参数值。参数列表可以由属性值构造。此列表中的每个属性参数必须用分号分隔。

在值列表中，分号分隔属性参数，逗号分隔属性值。示例如下：

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### 多个值

一些属性可以有多个值。简单地用属性名称生成一个新的内容行是多值属性的基本规则。但是，对于具有多种语言变体的单个值，不得使用多值属性。

### 二进制内容

在 iCalendar 对象中，属性值可以使用 URI 引用放置在外部 MIME 实体中的二进制内容数据。内联二进制内容可用于带有“ENCODING"参数的特殊情况，其中应用程序需要将 iCalendar 对象表示为唯一实体。以下示例解释了带有 URI 引用的“ATTACH"属性：

附件：https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

＃＃＃ 字符集

虽然 iCalendar 的默认字符集方案是 UTF-8，但没有指定属性参数来定义属性值的字符集。在 MIME 传输中，“charset"参数必须用于现有的字符集。

## 参考

* [互联网日历和调度核心对象规范](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

