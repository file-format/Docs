---
date: 2019-10-11
keywords: rm, .rm, rm-filformat, .rm-filformat, .rm-tillägg, RealMedia-filformat
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om RM-filformat och API:er som kan skapa och öppna RM-filer." 
title: RM filformat
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Vad är en RM fil? ##

RealMedia är ett proprietärt multimediacontainerformat utvecklat av RealNetworks som använder tillägget .rm. Den används med kombinationen av [RealAudio (RA)](/sv/audio/ra/) och [RealVideo(RV)](/sv/video/rv/) för streaming över internet. Dessa strömmar har konstant bithastighet. För variabel bithastighet utvecklade RealNetworks formatet RealMedia Variable Bitrate (RMVB). RealMedia lämpar sig för att streama innehåll över internet och kan användas för att streama live-tv till exempel.

## Struktur för RealMedia-fil ##

En RealMedia-fil består av en serie bitar som var och en har följande struktur:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Följande är de typer av bitar som finns i RealMedia-filen:

- **RealMedia filhuvud (.RMF)**: Detta måste vara den första biten i RealMedia-filen. Endast en RMF-bit finns i en fil. Den innehåller information om antalet rubriker.
- **Rubrik för filegenskaper (PROP)**: Detta innehåller information om de allmänna egenskaperna för RealMedia-filen. Det finns bara en bit av denna typ i varje RealMedia-fil.
- **Medieegenskaper rubrik (MDPR)**: Denna del innehåller information om strömningsegenskaperna. Den innehåller information om vilken typ av stream och vilken codec som används. Det finns en MDPR-bit för varje stream i filen.
- **Innehållsbeskrivningshuvud (CONT)**: Den här biten innehåller textinformation som titeln eller författaren för innehållet i RealMedia-filen. Denna del är endast i informationssyfte.
- **Datahuvud (DATA)**: Den här biten innehåller en grupp datapaket.
- **Indexhuvud (INDX)**: Denna del kommer efter alla DATA-bitar och innehåller indexposter. En fil kan ha mer än en INDX-bit.

## Ljud- och videoformat som stöds ##

### Ljudformat ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- dnet: AC3
- sipr: Sipro
- kock: Kock
- atrc: ATRAC3
- ralf: RealAudio Lossless Format
- raac: LC-AAC
- racp: HE-AAC

### Videoformat ###

- CLV1: ClearVideo
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- RV30: H.264-prekursor
- RV40: H.264-prekursor, RV40
- RVTR: H.263+ (RV20)

## Referenser ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

