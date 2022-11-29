---
date: 2021-03-21
keywords: mpc, Musepack-filformat, .mpc-tillägg
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Lär dig om MPC-filformat och API:er som kan skapa och öppna MPC-filer."
title: MPC - Musepack Audio Compression File Format
linktitle: MPC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-28
---

## Vad är en MPC fil?

En fil med filtillägget .mpc är ett [Musepack](https://musepack.net/) ljudfilformat som använder ljudkomprimering med stark betoning på hög kvalitet. Detta gör det möjligt för dig att inte ens märka ljudkvalitetsskillnaderna mellan original [WAV](/sv/audio/wav/)-fil och den komprimerade MPC-filen. Den använder MPEG-1 Layer-2-algoritmer för att uppnå mycket optimerad komprimering. Musepack MPC-filformatet är öppen källkod med BSD/GNU LGPL-licens. [SVN-förrådet](http://svn.musepack.net/) av Musepack gör det möjligt att hämta den senaste uppdaterade koden för codec. Applikationer som kan öppna MPC-filer inkluderar VLC Media Player, JetAudio och Winamp förutom flera andra.

## MPC filformat

MPC-filen använder MPEG-1 Layer-2-algoritmerna för att komprimera ljudfilerna. Det är ett containeroberoende format och tillåter även råströmskodning. Formatet använder ingen intern klippning och kan streamas med provexakt skärning. Dess paketerade ström tillåter multiplexering till ljud- och videobehållare som [MKV](/sv/video/mkv/).

## Referenser

* [Musepack MPC - Wikipedia](https://en.wikipedia.org/wiki/Musepack)
* [Musepack MPC](https://musepack.net/)

