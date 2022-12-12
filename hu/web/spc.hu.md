---
date: 2021-07-05
keywords: spc, .spc, spc fájlformátum, spc fájlok megnyitása, szoftvermegjelenítői tanúsítvány fájl
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC – Software Publisher Certificate File
linktitle: SPC
description: "Ismerje meg, mi az az SPC-fájlformátum és az API-k, amelyek SPC-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Mi az SPC fájl?

Az .spc kiterjesztésű fájl egy PKCS # 7 formátumban létrehozott digitális biztonsági tanúsítványfájl. Számos alkalmazás hozza létre ezeket a tanúsítványfájlokat a biztonságos információcsere érdekében. Kevés ilyen alkalmazás az OpenSSL és a Microsoft .NET-keretrendszerében található Signcode.exe alkalmazás. Más tanúsítványfájlokhoz hasonlóan, mint például a [.cer](/hu/web/cer/), [.p7c](/hu/web/p7c/) és [.ssp](/hu/web/ssp/), az SPC-fájlok is tartalmazzák a nyilvános kulcsot privát kulccsal titkosított információk. Ez a nyilvános kulcs nyilvánosan megosztható a felhasználókkal, miközben a titkos kulcsot bizalmasan kezelik.

## SPC fájlformátum – További információ

Az SPC fájlok bináris fájlokként kerülnek a lemezre, amelyek bármely szövegszerkesztőben megnyithatók, de ember által nem olvashatók. Ezek a PKCS # 7 legújabb verzióján alapulnak, amely elérhető [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Hivatkozások

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [SSP-referencia](https://scalate.github.io/scalate/documentation/ssp-reference.html)

