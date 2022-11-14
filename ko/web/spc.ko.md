---
date: 2021-07-05
keywords: spc, .spc, spc 파일 형식, spc 파일을 여는 방법, 소프트웨어 게시자 인증서 파일
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - 소프트웨어 게시자 인증서 파일
linktitle: SPC
description: "SPC 파일 형식과 SPC 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## .SPC 파일이란?

확장자가 .spc인 파일은 PKCS # 7 형식으로 생성된 디지털 보안 인증서 파일입니다. 여러 응용 프로그램에서 정보의 안전한 교환을 위해 이러한 인증서 파일을 만듭니다. Microsoft의 .NET Framework에 포함된 OpenSSL 및 Signcode.exe 응용 프로그램을 포함하는 이러한 응용 프로그램은 거의 없습니다. [.cer](/ko/web/cer/), [.p7c](/ko/web/p7c/) 및 [.ssp](/ko/web/ssp/)와 같은 다른 인증서 파일과 마찬가지로 SPC 파일에는 공개 키가 포함되어 있습니다. 개인 키로 암호화된 정보입니다. 이 공개 키는 개인 키가 기밀로 유지되는 동안 사용자와 공개적으로 공유될 수 있습니다.

## SPC 파일 형식 - 추가 정보

SPC 파일은 모든 텍스트 편집기에서 열 수 있지만 사람이 읽을 수 없는 바이너리 파일로 디스크에 저장됩니다. 이는 [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315)에서 사용할 수 있는 최신 버전의 PKCS # 7을 기반으로 합니다.

## 참고문헌

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [SSP 레퍼런스](https://scalate.github.io/scalate/documentation/ssp-reference.html)

