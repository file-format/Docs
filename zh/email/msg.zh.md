{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Microsoft Outlook 电子邮件格式",
  "description":"了解 MSG 文件格式和可以创建和打开 MSG 文件的 API。",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .msg 文件？

MSG 是 [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) 和 Exchange 用于存储电子邮件的一种文件格式、联系人、约会或其他任务。此类消息可能包含一个或多个电子邮件字段，包括发件人、收件人、主题、日期和消息正文，或联系信息、约会详情以及一个或多个任务规范。构成 Message 对象的属性，包括也是 MSG 文件的一部分。 MSG 文件具有作为纯 ASCII 文本的标题、主要消息正文和超链接。 MSG 文件也适用于需要 Microsoft 消息应用程序编程接口 (MAPI) 的程序。

## 味精文件结构

CFB_3 格式是 MSG 文件的基础。该范例基于存储和流概念，非常接近目录和文件。因此，前者的一个主要区别是整个层次结构，打包成一个不同的文件，称为复合文件。对象构成消息文件并由单个属性或其集合组成。这种能力有助于应用程序将复杂的结构化数据存储在单个文件中。这种格式还指定了多个存储，每个存储都将消息对象表示为一个主要组件。这些存储包含许多表示该组件属性的流。也可以嵌套存储。

## 马比地产

在 .msg 文件的顶层，存储包含在其中存储属性的流。属性可以分类如下：

* 固定长度属性
* 可变长度属性
* 多值属性

无论类别如何，属性要么是标记的，要么是命名的。但是，命名属性需要合适的映射信息，由它们的映射存储指定。

## 存储

存储构成 Message 对象的关键组件。 MSG 文件格式规定了以下存储：

## 顶层结构

Message 对象代表了整个 MSG 文件格式的顶层。根据类型、属性、收件人和附件对象的数量，消息对象可以在其相应的 .MSG 文件中具有不同的流存储。

### 与其他结构的关系

Msg 文件格式与其他结构有以下关系：

* .msg 的基础是复合文件二进制文件格式。
* 此格式使用消息和附件对象协议使用的属性。

## 避免 MSG 格式的场景

消息对象可以在使用 .msg 文件系统的客户端或消息存储之间共享。在少数情况下，不适合以 .msg 文件格式存储 Message 对象。例如：

* 在维护大型独立存档的情况下，最好使用可以更精确地呈现视图的全功能格式。
* 如果接收方未知，则可能是接收方不支持该格式，可能会传递私有或无关的格式。

## 味精文件示例

要了解 MSG 文件的外观，您可以下载 [示例 MSG 文件](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) 并在您的电脑查看其内容。

## 参考

* [[MS-OXMSG]: Outlook MSG 文件格式](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

