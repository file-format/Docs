---
date: 2019-12-13
keywords: m3u, m3u file format, .m3u extension, m3u multimedia playlist, m3u playlist format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lnopelniet par M3U faila formātu un API, kas var izveidot un atvērt M3U failus.
title: M3U faila veidlapaat
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Kas ir M3U fails? ##

M3U (MP3 URL) ir audio atskaņošanas saraksta fails, kas tiek saglabāts ar paplašinājumu .m3u. M3U nav īsts audio fails, tas tikai norāda uz audio un dažreiz arī video failiem. Fraunhofer M3U izstrādāja lietošanai kopā ar programmatūru Winplay3. To atbalsta arī dažādi multivides atskaņotāji un programmatūra.

## M3U faila formāts

M3U faila formātam nav oficiālas specifikācijas, tas ir de facto standarts. M3U ir vienkārša teksta fails, kurā tiek izmantots paplašinājums .m3u, ja teksts ir kodēts vietējās sistēmas noklusējuma kodējumā, kas nav Unikoda kods, vai ar paplašinājumu .m3u8, ja teksts ir UTF-8 kodēts. Katrs ieraksts M3U failā var būt viens no šiem:

- Absolūtais ceļš uz failu
- Faila ceļš attiecībā pret M3U failu.
- URL

### Pagarināts M3U ###

Paplašinātajā M3U tiek ieviestas papildu direktīvas, kas sākas ar # un beidzas ar kolu (:), ja tām ir parametri. Tālāk ir sniegts paplašinātā M3U direktīvu saraksts.

- **#EXTM3U** - tā ir faila galvene, kas norāda Extended M3U, un tai ir jābūt faila pirmajai rindai.
- **#EXTENC:** - teksta kodējums. Tai ir jābūt faila 2. rindiņai.
- **#EXTINF:** - izmanto ierakstu informācijai un citiem papildu rekvizītiem.
- **#PLAYLIST:** - The title of the playlist
- **#EXTGRP:** - Sāciet nosaukumu grupēšanu
- **#EXTALB:** - informācija par albumu
- **#EXTART:** - albuma izpildītājs
- **#EXTGENRE** - albuma žanrs
- **#EXTM3A** - viena faila atskaņošanas saraksts albuma ierakstiem vai nodaļām.
- **#EXTBYT:** - Faila lielums baitos.
- **#EXTBIN:** - seko binārie dati.
- **#EXTIMG:** - logotips, vāks vai citi attēli.

### HLS M3U ###

Apple izveidoja HLS (HTTP Live Streaming), lai straumētu audio un radio uz iOS ierīcēm. Tas ir balstīts uz UTF-8 kodēto paplašināto M3U. IETF 2017. gadā to standartizēja kā RFC 8216. HLS atskaņošanas saraksta atzīmes sākas ar #EXT-X-. Tālāk ir sniegts HLS tagu saraksts

- **EXT-X-VERSION** - norāda faila saderības versiju, pamatojoties uz datu nesēju un tā serveri.
- **#EXT-X-START:** - norāda atskaņošanas saraksta vēlamo sākuma punktu.
- **#EXT-X-PLAYLIST-TYPE:** - Norāda atskaņošanas saraksta veidu (EVENT vai VOD).
- **#EXT-X-TARGETDURATION:** - tas norāda maksimālo segmenta ilgumu.
- **#EXT-X-MEDIA-SEQUENCE:** - tas norāda datu nesēja kārtas numuru.
- **#EXT-X-INDEPENDENT-SEGMENTS** — tas norāda, ka visi multivides paraugi ir neatkarīgi un tos var atšifrēt bez citiem segmentiem.
- **#EXT-X-MEDIA:** - to izmanto, lai saistītu multivides atskaņošanas sarakstus, kas satur alternatīvus tā paša satura atveidojumus.
- **#EXT-X-STREAM-INF:** - tas norāda straumes variantu, kas ir daļa no pārveidošanas.
- **#EXT-X-BYTERANGE:** - norāda, ka multivides segments ir tā URI identificētā resursa apakšdiapazons.
- **#EXT-X-DISCONTINUITY** - norāda uz pārtraukumu starp iepriekšējo un nākamo multivides segmentu.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Tas ļauj sinhronizēt dažādus vienas un tās pašas straumes variantu vai dažādu variantu straumes atveidojumus.
- **#EXT-X-KEY:** - norāda, kā atšifrēt multivides segmentus.
- **#EXT-X-MAP:** - norāda, kā iegūt multivides inicializācijas sadaļu. Ir nepieciešams parsēt piemērojamos multivides segmentus.
- **#EXT-X-PROGRAM-DATE-TIME:** - It associates the first sample of the Media Segment with an absolute date and/or time.
- **#EXT-X-DATERANGE:** - tas saista datu diapazonu.
- **#EXT-XI-FRAMES-ONLY** — norāda, ka katrs atskaņošanas saraksta multivides segments apraksta vienu I-kadru.
- **EXT-XI-FRAME-STREAM-INF** — norāda, ka atskaņošanas saraksta failā ir multivides prezentācijas I-kadri.
- **#EXT-X-SESSION-DATA:** - ļauj iegūt patvaļīgus sesijas datus
pārnests galvenajā atskaņošanas sarakstā.
- **#EXT-X-SESSION-KEY:** - ļauj izmantot šifrēšanas atslēgas. Klients var iepriekš ielādēt šos taustiņus, vispirms neizlasot atskaņošanas sarakstu.
- **#EXT-X-ENDLIST** — tas norāda, ka failam netiks pievienoti vairāk multivides segmenti.

Šis ir M3U izmantoto interneta multivides veidu saraksts:

- **application/vnd.apple.mpegurl**: tas ir vienīgais reģistrētais multivides veids (reģistrēts 2009. gadā) M3U, ko izmanto, lai atsauktos uz atskaņošanas sarakstiem HLS lietojumprogrammās.
- Tālāk norādītos interneta multivides veidus izmanto lietojumprogrammas, kas nav HLS.
  - "**pieteikums/mpegurl**"
  - "**aplikācija/x-mpegurl**"
  - "**audio/mpegurl**"
  - "**audio/x-mpegurl**"

## M3U piemērs ##

Šis ir M3U faila piemērs.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Atsauces Nr.

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP Live Streaming](https://tools.ietf.org/html/rfc8216)

