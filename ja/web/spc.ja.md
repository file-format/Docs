---
date: 2021-07-05
keywords: spc, .spc, spc ファイル形式, spc ファイルの開き方, Software Publisher Certificate File
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - ソフトウェア発行者証明書ファイル
linktitle: SPC
description: "SPC ファイル形式とは何か,および SPC ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## .SPC オプション番号

拡張子が .spc のファイルは、PKCS # 7 形式で作成されたデジタル セキュリティ証明書ファイルです。いくつかのアプリケーションは、情報を安全に交換するためにこれらの証明書ファイルを作成します。このようなアプリケーションには、Microsoft の .NET Framework に含まれる OpenSSL や Signcode.exe アプリケーションなどはほとんどありません。 [.cer](/web/cer/)、[.p7c](/web/p7c/)、[.ssp](/web/ssp/) などの他の証明書ファイルと同様に、SPC ファイルには公開鍵が含まれています。秘密鍵で暗号化された情報。この公開鍵はユーザーと公に共有できますが、秘密鍵は機密に保たれます。

## SPC ファイル形式 - 詳細情報

SPC ファイルは、任意のテキスト エディターで開くことができるバイナリ ファイルとしてディスクに保存されますが、人間が判読することはできません。これらは、[RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315) で利用可能な PKCS # 7 の最新バージョンに基づいています。

## 参考文献

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [SSP リファレンス](https://scalate.github.io/scalate/documentation/ssp-reference.html)

