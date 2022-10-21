{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple 邮件文件格式",
  "description":"了解 EMLX 文件格式和可以创建和打开 EMLX 文件的 API。",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .EMLX 文件？

EMLX 文件格式由 Apple 实施和开发。 Apple Mail 应用程序使用 EMLX 文件格式导出电子邮件。还有其他应用程序可以打开 EMLX 文件并将其转换为其他文件格式。

## EMLX 文件格式简史

Mac OS X 操作系统采用了现有的电子邮件程序 NeXTMail，它是由 NeXT 创建的，作为 NeXTSTEP 操作系统的一部分。 Apple 在收购 NeXT 后提升了其功能，并成为现在的 Apple Mail 电子邮件应用程序，用作默认邮件客户端。通过 Apple Mail 导出的电子邮件直接保存为 EMLX 文件。此外，当有人在 Mac OS 上双击打开这些文件时，它是 EMLX 文件的默认邮件客户端。

## EMLX 文件格式

EMLx 文件是简单的基于文本的文件，可以在任何文本编辑器（如记事本）中打开。 EMLX 文件结构由三部分组成：

* 消息的字节数 - 消息本身的长度，以 ASCII 十进制形式写入，以 0x0a 结尾
* 消息本身
* XML plist 形式的消息元数据

借助从 Apple Mail 提取为 EMLX 并在文本编辑器中打开的以下示例电子邮件，可以更好地解释这些。

### EMLX 示例

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1] (******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

在本例中，875 显示消息的总长度。消息元数据包含在<plist>标签和标志如下所述：

|字段|描述|值
---|---|---|
|0|读取|1 << 0
|1|已删除|1 << 1
|2|已回答|1 << 2
|3|加密|1 << 3
|4|标记|1 << 4
|5|最近|1 << 5
|6|草稿|1 << 6
|7|初始（不再使用）|1 << 7
|8|转发|1 << 8
|9|重定向|1 << 9
|10-15|附件计数|3F << 10（6 位）
|16-22|优先级|7F << 16（7位）
|23|签名|1 << 23
|24|是垃圾|1 << 24
|25|不是垃圾|1 << 25
|26-28|字体大小增量|7 << 26（3 位）
|29|记录的垃圾邮件级别|1 << 29
|30|突出显示目录中的文本|1 << 30
|31|(未使用)|

## 也可以看看 ＃＃

* [EML](/zh/email/eml/)
* [味精](/zh/email/msg/)

