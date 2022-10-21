{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - 电子邮件邮箱文件",
  "description":"了解 MBOX 文件格式和可以创建和打开 MBOX 文件的 API。",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .mbox 文件？

MBox 文件格式是一个通用术语，表示用于收集电子邮件消息的容器。消息连同它们的附件一起存储在容器内。来自整个文件夹的消息保存在单个数据库文件中，新消息附加到文件末尾。许多应用程序和 API 提供对 MBox 文件格式的支持，例如 Apple Mail 和 Mozilla Thunderbird。

## MBOX 文件格式##

MBox 文件格式在很长一段时间内一直处于非标准化状态，直到 2005 年应用程序/mbox 被标准化为 [RFC 4155](https://tools.ietf.org/rfc/rfc4155.txt) 消息，采用 RFC 2822 格式, 在 MBox 文件格式中一个接一个地串联起来。每条消息都以用于标识消息发送者的分隔线开头，并且还标识最终接收者（传输路径中的最后一跳系统或充当接收者的系统）接收消息的日期和时间。邮箱）。每条消息通常以空行结束。数据库的结尾通常通过缺少任何附加数据或存在显式文件结束标记来识别。

## 从 MBox 文件中读取消息##

阅读器扫描 mbox 文件以查找 From_ 行。任何 From_ 行都标志着消息的开始。读者不应试图利用每个 From_ 行（文件开头之后）都是空白行这一事实。一旦阅读器找到一条消息，它就会从 From_ 行中提取（可能已损坏的）信封发件人和投递日期。然后读取直到下一个 From_ 行或文件末尾，以先到者为准。它剥离最后的空白行并删除 >From_ 行和 >>From_ 行等的引用。结果是一条 RFC 822 消息。

## 编码注意事项##

当收到的电子邮件包含 Mbox 文件作为附件并保存在另一个 Mbox 文件中时，MBox 文件的内容可能会变得不可逆转。为了避免这种情况，无论何时通过消息传递协议传输此类对象，消息传递系统都必须使用非透明传输编码（例如 BASE64 或 Quoted-Printable）对 mbox 数据库进行编码。如果收到不合规的数据，实施者还应准备好在本地对 mbox 数据进行编码。

## 参考 ＃＃

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - 维基百科](https://en.wikipedia.org/wiki/Mbox)

