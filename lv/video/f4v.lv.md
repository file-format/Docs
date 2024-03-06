---
date: 2019-10-11
keywords: f4v, .f4v, f4v file format, .f4v file format, .f4v extension, f4v extension, f4v video format, how to open f4v files, what are f4v files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lnopelniet par F4V faila formātu un API, kas var izveidot un atvērt F4V failues
title: F4V faila formaat
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Kas ir F4V fails? ##

F4V (Flash MP4 video fails) ir video fails, kas saglabāts ar paplašinājumu .f4v. Tas ir balstīts uz ISO bāzes multivides faila formātu (MPEG-4 12. daļa). Tas ir ļoti līdzīgs [MP4](/video/mp4/), tāpēc to neoficiāli dēvē arī par Flash MP4. [FLV](/video/flv/) bija ierobežojumi H.264/ACC satura straumēšanai, kā rezultātā Adobe Systems izveidoja jauno F4V formātu. Flash Player var atskaņot F4V failus kopš Flash Player 9 atjauninājuma 3 izlaišanas.

## F4V failu struktūra ##

F4V faila formāts ir balstīts uz ISO bāzes multivides faila formātu (MPEG-4 12. daļa) un ir ļoti līdzīgs MP4 formātam. Lai iegūtu sīkāku informāciju par struktūru, lūdzu, skatiet [MP4](/video/mp4/) lapu. Galvenā atšķirība starp F4V un MP4 ir metadatu formāti, ko F4V var saglabāt. Tālāk ir sniegts F4V formāta atbalstīto metadatu formātu saraksts.

- **Tag box**: Additional four optional tag boxes (auth, title, dscp, cprt) within the Movie (moov) box.
- **XMP metadatu lodziņš**: šis lodziņš atrodas tieši aiz lodziņa Filma (moov). Tādējādi fails var nosūtīt XMP metadatus SWF filmai, izmantojot ActionScript.
- **ilst box**: šis lodziņš atrodas meta (meta) lodziņā un var saturēt vairākus metadatu tagus. Atbalstītie datu veidi ir norādīti tālāk.
  - "**0**: pielāgoti dati."
  - "**1**: teksta dati."
  - "**12, 14**: binārie dati"
  - "**21**: vispārīgi dati."
- **Teksta celiņa metadatu lodziņš**: teksta paraugi (teksts vai tx3g) multivides datu lodziņā (mdat). Tajā var būt šādi metadatu lodziņi.
  - "**Stila lodziņš**: teksta stila specifikācijas."
  - "**Izcelšanas lodziņš**: norāda izceļamā teksta diapazonu."
  - "**Highlight Color box**: Specifies the highlight color for the text."
  - "**Karaoke kaste**: norādīti karaoke metadati."
  - "**Ritināšanas aizkaves lodziņš**: norāda ritināšanas aizkavi."
  - "**Nokrītošās ēnas nobīdes lodziņš**: norāda teksta nolaižamās ēnas nobīdes koordinātas."
  - "**Nolaižamās ēnas alfa lodziņš**: norāda teksta nolaižamās ēnas alfa vērtību."
  - "**Hiperteksta lodziņš**: norāda hiperteksta tekstu ar alternatīvo tekstu teksta diapazonā."
  - "**Tekstlodziņa lodziņš**: definē tekstlodziņa koordinātas."
  - "**Mirgojošs lodziņš**: norāda teksta diapazona mirgošanu."
  - "**Teksta aplaušanas lodziņš**: iestata teksta aplaušanas karogu."
  - "**Teksta aplaušanas lodziņš**: iestata teksta aplaušanas karogu."

## Atsauces Nr.

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

