---
date: 2021-07-05
keywords: "spc, .spc, spc 文件格式, 如何打开 spc 文件, Software Publisher Certificate File"
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "SPC - 软件发布者证书文件"
linktitle: "SPC"
description: "了解什么是 SPC 文件格式以及可以创建和打开 SPC 文件的 API。"
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## 什么是一 .spc 文件？

扩展名为 .spc 的文件是以 PKCS #7 格式创建的数字安全证书文件。多个应用程序创建这些证书文件以进行安全的信息交换。很少有这样的应用程序包括 OpenSSL 和 Microsoft .NET Framework 中包含的 Signcode.exe 应用程序。与 [.cer](/zh/web/cer/)、[.p7c](/zh/web/p7c/) 和 [.ssp](/zh/web/ssp/) 等其他证书文件一样，SPC 文件包含公钥用私钥加密的信息。这个公钥可以与用户公开共享，而私钥是保密的。

## SPC 文件格式 - 更多信息

SPC 文件以二进制文件的形式保存到光盘中，可以在任何文本编辑器中打开，但不是人类可读的。这些基于可用的 [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315) 的最新版本 PKCS #7。

## 参考

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [SSP 参考](https://scalate.github.io/scalate/documentation/ssp-reference.html)

