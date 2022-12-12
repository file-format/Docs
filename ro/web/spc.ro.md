---
date: 2021-07-05
keywords: spc, .spc, format de fișier spc, cum se deschide fișiere spc, fișierul de certificat de editor de software
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Fișier de certificat de editor de software
linktitle: SPC
description: "Aflați despre ce este un format de fișier SPC și API-urile care pot crea și deschide fișiere SPC."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Ce este un fișier SPC?

Un fișier cu extensia .spc este un fișier de certificat de securitate digital creat în formatul PKCS # 7. Mai multe aplicații, creează aceste fișiere de certificat pentru schimbul securizat de informații. Puține astfel de aplicații includ OpenSSL și aplicația Signcode.exe inclusă cu .NET Framework de la Microsoft. Ca și alte fișiere de certificat, cum ar fi [.cer](/ro/web/cer/), [.p7c](/ro/web/p7c/) și [.ssp](/ro/web/ssp/), fișierele SPC conțin cheia publică informații care sunt criptate cu o cheie privată. Această cheie publică poate fi partajată public cu utilizatorii, în timp ce cheia privată este păstrată confidențială.

## Format de fișier SPC - Mai multe informații

Fișierele SPC sunt salvate pe disc ca fișiere binare care pot fi deschise în orice editor de text, dar nu pot fi citite de om. Acestea se bazează pe cea mai recentă versiune a PKCS # 7, care este disponibilă [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Referințe

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [Referință SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

