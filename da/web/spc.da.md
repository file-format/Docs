---
date: 2021-07-05
keywords: spc, .spc, spc file format, how to open spc files, Software Publisher Certificate File
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Software Publisher Certificate File
linktitle: SPC
description: Ltjene om, hvad der er et SPC-filformat og API'er, der kan oprette og åbne SPC-fils.
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Hvad er en SPC fil?

En fil med filtypenavnet .spc er en digital sikkerhedscertifikatfil, der er oprettet i formatet PKCS #7. Flere applikationer opretter disse certifikatfiler for sikker udveksling af information. Få sådanne applikationer inkluderer OpenSSL og Signcode.exe-applikationen, der følger med Microsofts .NET Framework. Ligesom andre certifikatfiler såsom [.cer](/web/cer/), [.p7c](/web/p7c/) og [.ssp](/web/ssp/), indeholder SPC-filerne den offentlige nøgleinformation, der er krypteret med en privat nøgle. Denne offentlige nøgle kan deles med brugere offentligt, mens den private nøgle holdes fortrolig.

## SPC-filformat - flere oplysninger

SPC-filerne gemmes på disken som binære filer, der kan åbnes i enhver teksteditor, men som ikke kan læses af mennesker. Disse er baseret på den seneste version af PKCS # 7, som er tilgængelig [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Referencer

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)

* [SSP-reference](https://scalate.github.io/scalate/documentation/ssp-reference.html)


