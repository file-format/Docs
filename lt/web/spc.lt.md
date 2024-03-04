---
date: 2021-07-05
keywords: spc, .spc, spc file format, how to open spc files, Software Publisher Certificate File
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC – programinės įrangos leidėjo sertifikatas File
linktitle: SPC
description: Luždirbti apie tai, kas yra SPC failo formatas ir API, kurios gali sukurti ir atidaryti SPC failąs.
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Kas yra SPC failas?

Failas su plėtiniu .spc yra skaitmeninio saugos sertifikato failas, sukurtas PKCS # 7 formatu. Keletas programų, sukurkite šiuos sertifikatų failus saugiam informacijos mainams. Nedaug tokių programų yra OpenSSL ir Signcode.exe programa, įtraukta į Microsoft .NET Framework. Kaip ir kituose sertifikatų failuose, pvz., [.cer](/web/cer/), [.p7c](/web/p7c/) ir [.ssp](/web/ssp/), SPC failuose yra viešojo rakto informacija, užšifruota privačiu raktu. Šiuo viešuoju raktu galima viešai dalytis su vartotojais, kol privatus raktas yra konfidencialus.

## SPC failo formatas – daugiau informacijos

SPC failai išsaugomi diske kaip dvejetainiai failai, kuriuos galima atidaryti bet kuriame teksto rengyklėje, tačiau jie nėra įskaitomi žmonėms. Jie yra pagrįsti naujausia PKCS Nr. 7 versija, kuri pasiekiama [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Nuorodos

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)

* [SSP nuoroda](https://scalate.github.io/scalate/documentation/ssp-reference.html)


