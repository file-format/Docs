{
  "date" : "2020-08-20",
  "keywords" :["eot 文件","eot 文件格式","什么是 eot 文件","文件","eot 示例","eot 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - TrueType 字体文件格式",
  "description":"了解 EOT 文件格式和用于创建和打开 EOT 文件的 API。",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## 什么是一 .eot 文件？

带有 .eot 扩展名的文件是嵌入在文档中的 OpenType 字体。这些主要用于 Web 文件，例如网页。它由 Microsoft 创建并受 Microsoft 产品支持，包括 PowerPoint 演示文稿 [.pps](/zh/presentation/pps) 文件。该文件不是主要用途，是主文档或网页的附带文档。与 OTF 字体类似，EOT 支持字形的 Postscript 和 TrueType 轮廓。 EOT 文件的大小较小，因为它们使用 LZ 压缩进行压缩。 EOT 使用 Microsoft 工具从现有的 TTF/OTF 字体创建字体。

## 历史简介

EOT 字体于 2007 年作为 CSS3 的一部分提交给 W3C，但由于其要求永久安装在远程系统上成为拒绝的原因。 2008年3月重新提交，但W3C最终选择了当时标准化的[Web Font Format](/zh/font/woff/) (WOFF)。

## EOT 文件格式

EOT 文件格式详细信息可以在 [W3 提交页面](https://www.w3.org/Submission/EOT/#FileFormat) 上找到，并详细说明了此字体格式使用的结构。 EOT 由一个 EMBEDDEDFONT 结构组成，该结构提供了有关 hte 字体名称和支持的字符的足够基本信息。如果机器上已经存在字体，则打包此信息使用户代理可以避免解压、解压缩或安装字体。

### EMBEDDEDFONT 结构
EMBEDDEDFONT 结构经历了三个修订，每个修订都在结构末尾添加了附加数据。 EMBEDDEDFONT 结构的最新版本如下所示。

|数据类型|条目名称|描述|
---|---|---|
|unsigned long|EOTSize|以字节为单位的结构总长度（包括字符串和字体数据）|
|unsigned long|FontDataSize|OpenType 字体 (FontData) 的长度（以字节为单位）|
|unsigned long|版本|此格式的版本号 - 0x00020002|
|unsigned long|标志|处理标志|
|byte[10]|FontPANOSE|此字体的 PANOSE 值 - 请参阅 http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|在 Windows 中，这是从 TEXTMETRIC.tmCharSet 派生的。此值指定字体的字符集。 DEFAULT_CHARSET (0x01) 表示没有偏好。 - 请参阅 https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|如果在 OS/2.fsSelection 中设置了 ITALIC 位，则值为 0x01 - 请参阅 http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|此字体的重量值 - 请参阅 http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|提供有关嵌入权限信息的类型标志 - 请参阅 http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|EOT 文件的幻数 - 0x504C。用于检查数据损坏。|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1（位 0-31） - 请参阅 http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2（位 32-63） - 请参阅 http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3（位 64-95） - 请参阅 http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bits 96-127) - 见 http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1（位 0-31） - 请参阅 http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2（位 32-63） - 请参阅 http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - 请参阅 https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserved1|保留 - 必须为 0|
|unsigned long|Reserved2|保留 - 必须为 0|
|unsigned long|Reserved3|保留 - 必须为 0|
|unsigned long|Reserved4|保留 - 必须为 0|
|unsigned short|Padding1|填充以保持长对齐。填充值必须始终设置为 0x0000。|
|unsigned short|FamilyNameSize|FamilyName 数组使用的字节数|
|byte|FamilyName[FamilyNameSize]|UTF-16 字符数组 FamilyNameSize 字节的长度。这是在字体名称表中找到的英文字体系列字符串（名称 ID = 1） - 请参阅 https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|填充值必须始终设置为 0x0000。|
|unsigned short|StyleNameSize|StyleName 使用的字节数|
|byte|StyleName[StyleNameSize]|UTF-16 字符数组 StyleNameSize 字节的长度。这是在字体名称表中找到的英文字体子族字符串（名称 ID = 2） - 请参阅 https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|填充值必须始终设置为 0x0000。|
|unsigned short|VersionNameSize|VersionName 使用的字节数|
|bytes|VersionName[VersionNameSize]|UTF-16 字符数组，VersionNameSize 字节的长度。这是在字体名称表中找到的英文版本字符串（名称 ID = 5） - 请参阅 https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|填充值必须始终设置为 0x0000。|
|unsigned short|FullNameSize|FullName 使用的字节数|
|byte|FullName[FullNameSize]|UTF-16 字符数组 FullNameSize 字节的长度。这是在字体名称表中找到的英文全名字符串（名称 ID = 4） - 请参阅 https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|填充值必须始终设置为 0x0000。|
|unsigned short|RootStringSize|RootString 数组使用的字节数|
|byte|RootString[RootStringSize]|UTF-16 字符数组，RootStringSize 字节的长度。|
|unsigned long|RootStringCheckSum|RootString CheckSum 值。请参阅下面的算法来处理 RootStringChecksum。|
|unsigned long|EUDCCodePage|EUDC 字体支持所需的代码页值。|
|unsigned short|Padding6|填充值必须始终设置为 0x0000。|
|unsigned short|SignatureSize|签名数组使用的字节数。当前保留，应设置为 0x0000。|
|byte|Signature[SignatureSize]|当前保留。如果 SignatureSize 为 0x0000，则此数组没有长度。|
|unsigned long|EUDCFlags|处理 EUDC 字体的标志。典型值可能是 TTEMBED_XORENCRYPTDATA 和 TTEMBED_TTCOMPRESSED。|
|unsigned long|EUDCFontSize|签名数组使用的字节数。|
|byte|EUDCFontData[EUDCFontSize]|用于 EUDC 字体数据的字节数。如果 EUDCFontSize 为 0x00000000，则此数组没有长度。|
|byte|FontData[FontDataSize]|这个 EOT 文件的字体数据。如处理标志所示，数据可能被压缩或 XOR 加密。

## 参考

* [EOT 文件格式](https://www.w3.org/Submission/EOT/)
* [嵌入式 OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [字体嵌入](https://en.wikipedia.org/wiki/Font_embedding)

