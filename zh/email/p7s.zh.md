{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7S 文件 - 数字签名的电子邮件",
  "description":"了解 P7S 文件格式和可以创建和打开 P7S 文件的 API。",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## 什么是一 .p7s 文件？

P7S 文件是通过数字签名电子邮件接收的数字签名。此文件作为电子邮件的附件存在，可验证该电子邮件是从真实来源发送的。这可确保发件人在其计算机上安装了电子邮件签名证书。当从用户的计算机发送此类签名的电子邮件时，会附上包含发件人姓名的 P7S 文件。支持签名电子邮件的电子邮件客户端可以看到发件人的信息。

## P7S 文件格式 - 更多信息

S/MIME（安全/多用途 Internet 邮件扩展）P7S 文件包含人类可读的纯文本格式的信息。 Microsoft Outlook、Apple Mail 和 Mozilla Thunderbird 等电子邮件客户端支持从 S/MIME 电子邮件中读取数字签名信息。签署电子邮件验证发件人的身份，并告诉接收者该消息是真实的。从电子邮件客户端（作为 [EML](/zh/email/eml/) 或 [MSG](/zh/email/msg/)）下载电子邮件时，会发现这些 P7S 文件附在这些电子邮件中。

P7S 文件包含以下信息：

* 电子邮件的来源
* 发送日期和时间，
* 传输过程中是否被修改

此信息是使用公钥加密标准#7 (PKCS7) 技术嵌入的，用于将加密签名以数字方式附加到电子邮件中。

## 参考 ＃＃

* [微软签名工具](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

