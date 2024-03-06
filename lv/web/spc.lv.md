---
date: 2021-07-05
keywords: spc, .spc, spc file format, how to open spc files, Software Publisher Certificate File
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC — programmatūras izdevēja sertifikāts File
linktitle: SPC
description: Lnopelniet par SPC faila formātu un API, kas var izveidot un atvērt SPC failus.
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Kas ir SPC fails?

Fails ar paplašinājumu .spc ir digitālās drošības sertifikāta fails, kas izveidots PKCS #7 formātā. Vairākas lietojumprogrammas, izveidojiet šos sertifikātu failus drošai informācijas apmaiņai. Dažas šādas lietojumprogrammas ietver OpenSSL un Signcode.exe lietojumprogrammu, kas iekļauta Microsoft .NET Framework. Tāpat kā citi sertifikātu faili, piemēram, [.cer](/web/cer/), [.p7c](/web/p7c/) un [.ssp](/web/ssp/), SPC faili satur publiskās atslēgas informāciju, kas ir šifrēta ar privāto atslēgu. Šo publisko atslēgu var publiski koplietot ar lietotājiem, kamēr privātā atslēga tiek saglabāta konfidenciāla.

## SPC faila formāts — vairāk informācijas

SPC faili tiek saglabāti diskā kā bināri faili, kurus var atvērt jebkurā teksta redaktorā, taču tie nav lasāmi cilvēkiem. Tie ir balstīti uz jaunāko PKCS 7. versiju, kas ir pieejama [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Atsauces

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)

* [SSP atsauce](https://scalate.github.io/scalate/documentation/ssp-reference.html)


