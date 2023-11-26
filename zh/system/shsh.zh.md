{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH 文件 - iPhone/iPod Touch SHSH Blob 文件格式",
  "description":"了解什么是 SHSH 文件。",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## 什么是 .shsh 文件？

SHSH 文件也称为 Signature HaSH，是 Apple 用于验证和验证 iPhone、iPad 和 iPod 等 iOS 设备的固件更新的数字签名。

## SHSH 和 SHSH2 文件格式之间的区别

与 SHSH2 文件一样，SHSH 文件包含设备的唯一标识符，称为“ECID”（专用芯片 ID），以及有关设备上安装的固件版本的信息。但是，SHSH 文件在较旧版本的 iOS（iOS 10 之前）中使用，此后已被 SHSH2 文件取代。

## SHSH 文件格式 - 更多信息

SHSH 文件以二进制文件格式保存到光盘上。此文件格式的内部文件结构详细信息不公开。

SHSH 文件对于想要将设备固件降级到 Apple 不再签名的先前版本的用户非常重要。通过在 Apple 仍在签名时保存特定固件版本的 SHSH 文件，用户稍后可以使用它们绕过 Apple 的签名验证并在其设备上安装该固件版本。此过程也称为“越狱”。

## 参考

* [SHSH Blob - 来自维基百科](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS 保存程序](https://tsssaver.1conan.com/v2/)

