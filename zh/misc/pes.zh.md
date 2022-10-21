{
  "date" : "2021-07-29",
  "keywords" :["pes 文件","pes 文件格式","什么是 pes 文件","文件","pes 示例","pes 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PES文件格式-兄弟PE绣花格式",
  "description":"了解 PES 文件格式和可以创建和打开 PES 文件的 API。",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## 什么是 PES 刺绣文件？

PES 刺绣文件是一个设计文件，其中包含刺绣/缝纫机的说明。它是由 Brother Industries 为他们的刺绣机开发的，但后来被正式化为通用文件格式。缝纫机使用 PES 文件来阅读在织物上缝合图案的说明。这些文件有两个目的；首先提供 Brother Industries 开发的 PE-Design 应用程序的设计信息，其次提供设计名称、颜色和绣花机代码，例如“stop"、“jump"和“trim"。

## PES 文件格式 - 更多信息

PES 文件以二进制文件格式保存到光盘中。它包含多个部分，这些部分使用预定义的方法存储了缝纫信息。 PES 文件格式如下。

* 版本数据 - 提供版本信息，可以是任何值 `#PES0001`、`#PES0020`、`#PES0030`、`#PES0040`、`#PES0050`、`#PES0055`、`#PES0060`
* PEC 搜索值 - 紧跟版本数据的 4 字节小端整数，表示包含设计细节信息的 PEC 部分的搜索值
* PSE 部分 - 包含与 Brother PE-Design 相关的设计信息，可能是其他缝纫应用程序
* PCE 部分 - 可以在 PSE 文件中的任何位置，但由 PEC 搜索值引用。

## 使用 PES 文件的缝纫机类型

PES 文件主要由 Brother 缝纫机使用的 PE-Design 软件创建。其他一些可能支持 PES 文件的机器包括 Babylock 和 Bernina 家用刺绣机。

## 如何转换 PSE 文件？

PE-Design软件应用程序可以[转换PSE文件](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+file) 转换为其他格式，例如 .pes、.dst、.exp、.pcs、.hus、.vip、.shv、.jef、.sew、.csd 或 .xxx。可以使用 PE-Design 应用程序通过打开文件并选择转换格式来完成。

## 参考

* [PE 设计 - 指导手册](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

