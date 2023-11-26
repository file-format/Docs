{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2 文件 - iOS SHSH Blob 文件格式",
  "description":"了解什么是 SHSH2 文件。",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## 什么是SHSH2文件？

SHSH2 文件也称为 SHSH blob 或 ECID SHSH，是 Apple 用于验证和验证 iPhone、iPad 和 iPod 等 iOS 设备的固件更新的数字签名。它包含设备的唯一标识符，称为 ECID（专用芯片 ID）。它还包含有关设备上安装的固件版本的信息。

## SHSH2 文件格式 - 更多信息

SHSH2 文件以二进制文件格式保存到光盘上，并且该文件格式的内部文件结构详细信息无法公开获得。

当 iPhone、iPad 或 Mac 等 Apple 设备上安装新版本的 iOS 时，会生成 SHSH2 文件。该 SHSH2 文件被发送到 Apple 服务器，该服务器读取并验证该数字签名文件。服务器根据此信息允许或阻止安装。

当请求更新时也会发生同样的情况。当用户通过 iTunes 或其他软件请求更新或恢复其设备时，Apple 的服务器将检查 SHSH2 文件是否与设备的 ECID 和固件版本匹配，然后才允许继续更新。

## 参考

* [SHSH Blob - 来自维基百科](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS 保存程序](https://tsssaver.1conan.com/v2/)

