{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - 电子邮件消息",
  "description":"了解 EML 文件格式和可以创建和打开 EML 文件的 API。",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## 什么是一 .eml 文件？

EML 文件格式表示使用 Outlook 和其他相关应用程序保存的电子邮件。几乎所有的电子邮件客户端都支持这种文件格式，因为它符合 RFC-822 Internet 消息格式标准。 Microsoft Outlook 是打开 EML 邮件类型的默认软件。 EML 文件可用于保存到光盘以及使用通信协议发送给收件人。

## EML 简史

EML 文件格式规范按照 [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) 标准格式提供。在 RFC-822 之前，RFC-733 管理网络消息交换的规则，直到 1982 年，前者是通过建立 ARPA 标准作为对横向的改进而创建的。同时，微软为开发自己的电子邮件客户端（即 Outlook Express）创建了自己的 COM 模块。当 Microsoft 偏离开放标准并创建 [PST](/zh/email/pst/) 文件格式，其中电子邮件以高度结构化的数据库格式保存时，RFC-822 走上了被确立为专有格式的道路。当从 Microsoft Outlook 转发电子邮件时，这会导致非 Microsoft 电子邮件客户端的用户出现问题。

2001 年，822 标准被增强为 2822 - Internet 消息格式，目前用于创建、读取和发送 MIME RFC-822 格式的 EML 消息。

## EML 文件格式规范

EML 文件由两个不同的部分组成：

* Headers - 包含有关消息头的信息
* 消息正文 - 包含一系列信息，可以包括消息内容、嵌入的图像和附件

### 标题信息###

EML 文件由标头信息和可选的消息正文组成。 EML 中的每个标题行都有两个部分，由冒号“:"分隔。第一个称为标题名称，冒号后面的称为标题正文。例如，此类标头包括：

* 发件人电子邮件地址
* 收件人电子邮件地址
* 邮件主题
*消息的时间和日期戳

**示例标题**

从：<John@bmw.eml.light.com>

至：<Andy@fileformat.com>

日期：2018 年 3 月 8 日星期四 10:43:37 +0100

主题：bmw eml light

＃＃＃ 邮件正文 ＃＃＃

EML 消息正文以文本、超链接和附件的形式包含电子邮件的主要信息。电子邮件正文可以包含纯可读文本，但不是必需的。在这种情况下，消息正文可以为空或包含编码的附件数据。

消息体的内容由其 Content-Type 描述，使阅读应用程序能够读取相应格式的信息。它实际上代表了文档的性质和格式。 MIME 类型或内容类型的结构非常简单；它由一个类型和一个子类型，两个字符串组成，用'/'分隔。不允许有空间。 `type` 表示类别，可以是离散类型或多部分类型。 `subtype` 特定于每种类型。属于 Content-Type 类别的类型列表很长，但一些重要的内容类型如下：


|**类型**|**描述**|**子类型示例**
---|---|---|
|text|表示人类可读的格式|text/plain, text/html, text/css, text/javascript
|image|表示除视频之外的任何类型的图像|image/bmp, image/png, image/jpg, image/gif
|audio|代表任何音频文件格式|audio/mdi, audio/wav
|application|表示任何类型的二进制数据|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### EML 正文中的附件表示 ###

EML 正文包含它所包含的每个内容类型的边界。消息正文中的附件由其 Content-Type 和 Content-Disposition 标识，如下例所示：

内容类型：文本/纯文本；字符集#"windows-1252";名称#“苹果应用商店.txt"
内容处置：附件；文件名#"苹果应用商店.txt"
内容传输编码：base64
X 附件 ID：f_jkhztmd02

可以看出，Content-Disposition 设置为附件使阅读应用程序能够获取附件信息，例如附件文件名和传输编码。附件头信息后面是要读取的编码附件内容。

#### 作为附件的电子表格示例####

内容类型：application/vnd.openxmlformats-officedocument.spreadsheetml.sheet；名称#"english_spodr.xlsx"
内容处置：附件；文件名#"english_spodr.xlsx"
内容传输编码：base64
X 附件 ID：f_jkhztmd43

## 参考

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

