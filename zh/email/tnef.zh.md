{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"了解 TNEF 文件格式和可以创建和打开 TNEF 文件的 API。",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .TNEF 文件？

传输中性封装格式 (TNEF) 是 Microsoft 专有的，用于封装基于消息应用程序编程接口 (**MAPI**) 的电子邮件附件。 Microsoft Outlook 和 Microsoft Exchange Server 完全支持 TNEF，稍后将 TNEF 解码为 MAPI 并显示格式化的邮件。带有 TNEF 编码的电子邮件附件的 MIME 类型为 MS-TNEF，并存储为 winmail/win.dat。 winmail .dat 中的附件封装了以下信息：


|消息|OLE 对象|Outlook 功能
---|---|---|
|<ul><li>原始邮件附件</li><li>原始格式化版本</li><li>字体、文本大小和文本颜色</li></ul>|<ul><li>嵌入图片</li><li>嵌入式 Office 文档</li></ul>|<ul><li>自定义表格</li><li>投票按钮</li><li>会议要求</li></ul>


其他不支持 TNEF 的电子邮件服务会为 TNEF 格式的邮件提供纯文本。 Outlook 在 TNEF 文件 (OLE) 或特定 Outlook 功能（表单、轮询按钮和会议请求）中嵌入了丰富格式的邮件。在 Outlook 电子邮件客户端中批准显式 TNEF 编码是不可能的，但是，选择用于发送电子邮件的 RTF 格式隐式地促进了 TNEF 编码。

## TNEF 文件格式

TNEF 数据算法从丰富的分层消息属性中建立了扁平结构。然后，这些扁平结构用于表示由特定属性组成的串行数据流。

在某些情况下，属性以组形式出现或具有多个值，流可能包括计数和填充以强制执行特定的数据对齐。在不支持的消息传递环境中，使用该算法是有利的一个独特情况。在这种环境中，丰富的消息属性由 TNEF 写入器编码为串行数据流。此外，不属于底层TNEF的属性可以在传输过程中进行封装。然后通过 TNEF 进行解码，使这些封装的属性可用，以确保原始消息的所有属性对客户端应用程序的可用性。

在 TNEF 中，所有数字数据类型都是 little-endian，并且它们的大小大于一个字节。在非小端平台上处理这些数值需要完成适当的转换以获得正确的值。根据 [RFC5234] 规范，字符串值以增强巴科斯-瑙尔格式 (ABNF) 格式表示。当字符串以空字符结尾时，它也被包含在内；例如，“worker@specimen.com"%x00。

{{< figure src="../TNEF.png" alt="TNEF 文件格式" >}}

## TNEF 属性和处理规则##

TNEF 中的数据流以旧版本号、签名、原始键值和表示代码页的属性开始。此代码页是在编码器记录 ANSI 属性和属性时生成的。之后，流变成了一系列属性，其中首先排列的是消息属性，然后是附件属性。不同的消息和附件特征包含在 attMsgProps、attAttachment 和 attRecipTable 等特殊属性中。出现在 TNEF 流中的属性包含结构、消息属性和将它们与消息属性结合所必需的转换。每个属性由属性的ID、大小和数据、校验和和根据其应用的级别组成。

## 与协议和其他算法的关系##

显示丰富消息格式的机制较差的系统本身需要TNEF数据算法进行传输。使用媒体类型 ms-TNEF，算法的输出由附件文件 (winmail.dat) 和 [RFC2045] 中指定的 MIME 正文部分组成。纯文本消息体根据 [MSDN-UAF] 规范使用 UUENCODE 传输，并且在接收端解码此消息体或等效方法。此外，TNEF 可以使用不同的 Internet 协议传输消息数据，如 SMTP、POP3、IMAP4，以及根据 RFC2045 标准集成 MIME 的协议。

## 适用性声明##

除了简单的消息传输之外，TNEF 的原始应用程序将被创建为使用消息类并支持传输协议中没有原始支持的附加功能。该应用程序被进一步改进，用于传输现代消息传递客户端现在使用的丰富消息属性和命名属性。为了与原始实现保持一致，保留原始属性语法，并且一个特殊属性单独保存新消息属性。

## 参考

* [传输中性封装格式](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Exchange Server 中的电子邮件地址和通讯簿](https://docs.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]：传输中性封装格式 (TNEF) 数据算法](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

