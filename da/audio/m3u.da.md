---
date: 2019-12-13
keywords: m3u, m3u file format, .m3u extension, m3u multimedia playlist, m3u playlist format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltjene om M3U filformat og API'er, der kan oprette og åbne M3U fils.
title: M3U filformularat
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Hvad er en M3U fil? ##

M3U (MP3 URL) er en lydafspilningslistefil, der er gemt med filtypenavnet .m3u. M3U er ikke en egentlig lydfil, den peger bare på lyd- og nogle gange videofiler. M3U blev udviklet til brug med Winplay3 software af Fraunhofer. Det understøttes også af forskellige medieafspillere og software.

## M3U filformat

Der er ingen officiel specifikation for M3U-filformatet, det er en de-facto standard. M3U er en almindelig tekstfil, der bruger filtypen .m3u, hvis teksten er kodet i det lokale systems standard ikke-Unicode-kodning eller med filtypenavnet .m3u8, hvis teksten er UTF-8-kodet. Hver post i M3U-filen kan være en af følgende:

- Absolut sti til filen
- Filsti i forhold til M3U-filen.
- URL

### Udvidet M3U ###

I den udvidede M3U introduceres yderligere direktiver, der begynder med # og slutter med et kolon(:), hvis de har parametre. Nedenstående er en liste over direktiver for udvidet M3U.

- **#EXTM3U** - Det er filoverskriften, der angiver Extended M3U og skal være første linje i filen.
- **#EXTENC:** - Tekstkodning. Det skal være 2. linje i filen.
- **#EXTINF:** - Bruges til sporoplysninger og andre yderligere egenskaber.
- **#PLAYLIST:** - The title of the playlist
- **#EXTGRP:** - Begynd navnegruppering
- **#EXTALB:** - Albumoplysninger
- **#EXTART:** - Albumkunstner
- **#EXTGENRE** - Albumgenre
- **#EXTM3A** - Enkeltfil afspilningsliste til albumnumre eller kapitler.
- **#EXTBYT:** - Filstørrelse i bytes.
- **#EXTBIN:** - Binære data følger.
- **#EXTIMG:** - Logo, cover eller andre billeder.

### HLS M3U ###

HLS (HTTP Live Streaming) blev skabt af Apple til at streame lyd og radio til iOS-enheder. Den er baseret på den UTF-8-kodede udvidede M3U. Det blev standardiseret som RFC 8216 i 2017 af IETF. Taggene til HLS-afspilningslisten begynder med #EXT-X-. Nedenfor er en liste over tags til HLS

- **EXT-X-VERSION** - Angiver kompatibilitetsversionen af filen baseret på mediet og dets server.
- **#EXT-X-START:** - Angiver det foretrukne startpunkt for afspilningslisten.
- **#EXT-X-PLAYLIST-TYPE:** - Giver typen af afspilningsliste (EVENT eller VOD).
- **#EXT-X-MÅLVARIGHED:** - Det angiver den maksimale segmentvarighed.
- **#EXT-X-MEDIA-SEQUENCE:** - Det angiver mediesekvensnummeret.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Det angiver, at alle medieeksempler er uafhængige og kan afkodes uden andre segmenter.
- **#EXT-X-MEDIA:** - Det bruges til at relatere medieafspilningslister, der indeholder alternative gengivelser af det samme indhold.
- **#EXT-X-STREAM-INF:** - Det specificerer en variantstrøm, der er en del af gengivelserne.
- **#EXT-X-BYTERANGE:** - Indikerer, at mediesegmentet er et underområde af ressourcen identificeret af dets URI.
- **#EXT-X-DISCONTINUITY** - Angiver diskontinuitet mellem de foregående og følgende mediesegmenter.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Det tillader synkronisering mellem forskellige gengivelser af den samme Variant Stream eller forskellige Variant Streams.
- **#EXT-X-KEY:** - Specificerer, hvordan mediesegmenter dekrypteres.
- **#EXT-X-MAP:** - Specificerer, hvordan man henter Media Initialization Section. Det er påkrævet at parse de relevante mediesegmenter.
- **#EXT-X-PROGRAM-DATE-TIME:** - It associates the first sample of the Media Segment with an absolute date and/or time.
- **#EXT-X-DATERANGE:** - Det forbinder et dataområde.
- **#EXT-XI-FRAMES-ONLY** - Angiver, at hvert mediesegment i afspilningslisten beskriver en enkelt I-frame.
- **EXT-XI-FRAME-STREAM-INF** - Det angiver, at afspilningslistefilen indeholder I-frames af multimediepræsentation.
- **#EXT-X-SESSION-DATA:** - Det tillader vilkårlige sessionsdata at blive
båret i en Master Playliste.
- **#EXT-X-SESSION-KEY:** - Det giver mulighed for krypteringsnøgler. Klienten kan forudindlæse disse nøgler uden først at læse afspilningslisten.
- **#EXT-X-ENDLIST** - Det angiver, at der ikke vil blive tilføjet flere mediesegmenter til filen.

Følgende er listen over internetmedietyper, der bruges af M3U:

- **application/vnd.apple.mpegurl**: Det er den eneste registrerede medietype (registreret i 2009) for M3U, der bruges til at henvise til afspilningslisterne i HLS-applikationer.
- Følgende internetmedietyper bruges af ikke-HLS-applikationer.
  - "**applikation/mpegurl**"
  - "**applikation/x-mpegurl**"
  - "**lyd/mpegurl**"
  - "**lyd/x-mpegurl**"

## M3U eksempel ##

Dette er et eksempel på M3U-filen.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Referencer ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP Live Streaming](https://tools.ietf.org/html/rfc8216)

