---
date: 2019-12-13
keywords: m3u, m3u filformat, .m3u tillägg, m3u multimedia spellista, m3u spellista format
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om M3U-filformat och API:er som kan skapa och öppna M3U-filer."
title: M3U filformat
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Vad är en M3U fil? ##

M3U (MP3 URL) är en ljudspellistfil som lagras med tillägget .m3u. M3U är inte en verklig ljudfil, den pekar bara på ljud- och ibland videofiler. M3U utvecklades för att användas med programvaran Winplay3 av Fraunhofer. Det stöds också av olika mediaspelare och mjukvara.

## M3U filformat

Det finns ingen officiell specifikation för M3U-filformatet, det är en de facto-standard. M3U är en vanlig textfil som använder tillägget .m3u om texten är kodad i det lokala systemets standardkodning utan Unicode eller med tillägget .m3u8 om texten är UTF-8-kodad. Varje post i M3U-filen kan vara en av följande:

- Absolut sökväg till filen
- Filsökväg i förhållande till M3U-filen.
- URL

### Extended M3U ###

I den utökade M3U införs ytterligare direktiv som börjar med "#" och slutar med ett kolon(:) om de har parametrar. Nedan finns en lista över direktiv för utökad M3U.

- **#EXTM3U** - Det är filhuvudet som indikerar Extended M3U och måste vara första raden i filen.
- **#EXTENC:** - Textkodning. Det måste vara den andra raden i filen.
- **#EXTINF:** - Används för spårinformation och andra ytterligare egenskaper.
- **#PLAYLIST:** - Spellistans titel
- **#EXTGRP:** - Börja namngruppering
- **#EXTALB:** - Albuminformation
- **#EXTART:** - Albumartist
- **#EXTGENRE** - Albumgenre
- **#EXTM3A** - Spellista för enstaka filer för albumspår eller kapitel.
- **#EXTBYT:** - Filstorlek i byte.
- **#EXTBIN:** - Binära data följer.
- **#EXTIMG:** - Logotyp, omslag eller andra bilder.

### HLS M3U ###

HLS (HTTP Live Streaming) skapades av Apple för att strömma ljud och radio till iOS-enheter. Den är baserad på den UTF-8-kodade utökade M3U. Det standardiserades som RFC 8216 2017 av IETF. Taggarna för HLS-spellistan börjar med "#EXT-X-". Nedan finns en lista med taggar för HLS

- **EXT-X-VERSION** - Indikerar kompatibilitetsversionen av filen baserat på media och dess server.
- **#EXT-X-START:** - Indikerar den föredragna startpunkten för spellistan.
- **#EXT-X-PLAYLIST-TYPE:** - Tillhandahåller typen av spellista (EVENT eller VOD).
- **#EXT-X-TARGETDURATION:** - Den anger den maximala segmentets varaktighet.
- **#EXT-X-MEDIA-SEQUENCE:** - Det indikerar mediasekvensnumret.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Det indikerar att alla mediaprover är oberoende och kan avkodas utan andra segment.
- **#EXT-X-MEDIA:** - Det används för att relatera mediaspellistor som innehåller alternativa återgivningar av samma innehåll.
- **#EXT-X-STREAM-INF:** - Den specificerar en variantström som är en del av återgivningarna.
- **#EXT-X-BYTERANGE:** - Indikerar att mediesegmentet är ett underområde av resursen som identifieras av dess URI.
- **#EXT-X-DISCONTINUITY** - Indikerar diskontinuitet mellan föregående och efterföljande mediasegment.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Det tillåter synkronisering mellan olika versioner av samma variantström eller olika variantströmmar.
- **#EXT-X-KEY:** - Anger hur mediasegment ska dekrypteras.
- **#EXT-X-MAP:** - Anger hur man skaffar Media Initialization Section. Det krävs att de tillämpliga mediesegmenten analyseras.
- **#EXT-X-PROGRAM-DATE-TIME:** - Det associerar det första urvalet av mediesegmentet med ett absolut datum och/eller tid.
- **#EXT-X-DATERANGE:** - Den associerar ett dataområde.
- **#EXT-XI-FRAMES-ONLY** - Indikerar att varje mediesegment i spellistan beskriver en enda I-frame.
- **EXT-XI-FRAME-STREAM-INF** - Det indikerar att spellistfilen innehåller I-frames av multimediapresentation.
- **#EXT-X-SESSION-DATA:** - Det tillåter godtyckliga sessionsdata
bärs i en Master Playlist.
- **#EXT-X-SESSION-KEY:** - Den tillåter krypteringsnycklar. Klienten kan ladda dessa nycklar i förväg utan att först läsa spellistan.
- **#EXT-X-ENDLIST** - Det indikerar att inga fler mediesegment kommer att läggas till filen.

Följande är listan över internetmedietyper som används av M3U:

- **application/vnd.apple.mpegurl**: Det är den enda registrerade mediatypen (registrerad 2009) för M3U som används för att referera till spellistorna i HLS-applikationer.
- Följande internetmedietyper används av icke-HLS-applikationer.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## M3U Exempel ##

Detta är ett exempel på M3U-filen.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Referenser ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP Live Streaming](https://tools.ietf.org/html/rfc8216)

