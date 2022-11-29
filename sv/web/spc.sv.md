---
date: 2021-07-05
keywords: spc, .spc, spc-filformat, hur man öppnar spc-filer, Software Publisher Certificate File
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Software Publisher Certificate File
linktitle: SPC
description: "Lär dig mer om vad som är ett SPC-filformat och API:er som kan skapa och öppna SPC-filer." 
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Vad är en SPC fil?

En fil med filtillägget .spc är en digital säkerhetscertifikatfil skapad i formatet PKCS #7. Flera applikationer skapar dessa certifikatfiler för säkert utbyte av information. Få sådana applikationer inkluderar OpenSSL och Signcode.exe-applikationen som ingår i Microsofts .NET Framework. Liksom andra certifikatfiler som [.cer](/sv/web/cer/), [.p7c](/sv/web/p7c/) och [.ssp](/sv/web/ssp/), innehåller SPC-filerna den publika nyckeln information som är krypterad med en privat nyckel. Denna offentliga nyckel kan delas med användare offentligt medan den privata nyckeln hålls konfidentiell.

## SPC-filformat - Mer information

SPC-filerna sparas på skiva som binära filer som kan öppnas i vilken textredigerare som helst men som inte är läsbara för människor. Dessa är baserade på den senaste versionen av PKCS # 7 som är tillgänglig [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Referenser

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [SSP-referens](https://scalate.github.io/scalate/documentation/ssp-reference.html)

