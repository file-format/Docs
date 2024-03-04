---
date: 2019-12-13
keywords: m3u, m3u file format, .m3u extension, m3u multimedia playlist, m3u playlist format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Luždirbti apie M3U failo formatą ir API, kurios gali sukurti ir atidaryti M3U failąs.
title: M3U failo formaat
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Kas yra M3U failas? ##

M3U (MP3 URL) yra garso grojaraščio failas, saugomas su plėtiniu .m3u. M3U nėra tikras garso failas, jis tiesiog nurodo garso ir kartais vaizdo failus. M3U sukūrė Fraunhofer, kad būtų galima naudoti su Winplay3 programine įranga. Jį taip pat palaiko įvairūs medijos leistuvai ir programinė įranga.

## M3U failo formatas

Nėra oficialios M3U failo formato specifikacijos, tai yra de facto standartas. M3U yra paprasto teksto failas, kuriame naudojamas plėtinys .m3u, jei tekstas užkoduotas vietinės sistemos numatytuoju ne Unikodo kodu, arba plėtiniu .m3u8, jei tekstas yra užkoduotas UTF-8. Kiekvienas M3U failo įrašas gali būti vienas iš šių:

- Absoliutus kelias į failą
- Failo kelias, palyginti su M3U failu.
– URL

### Išplėstinis M3U ###

Išplėstiniame M3U įvedamos papildomos direktyvos, kurios prasideda # ir baigiasi dvitaškiu (:), jei turi parametrų. Toliau pateikiamas išplėstinio M3U direktyvų sąrašas.

– **#EXTM3U** – tai failo antraštė, nurodanti išplėstinį M3U ir turi būti pirmoji failo eilutė.
– **#EXTENC:** – Teksto kodavimas. Tai turi būti 2-oji failo eilutė.
- **#EXTINF:** - Naudojamas takelio informacijai ir kitoms papildomoms ypatybėms.
- **#PLAYLIST:** - The title of the playlist
– **#EXTGRP:** – Pradėti vardų grupavimą
- **#EXTALB:** - Albumo informacija
– **#EXTART:** – Albumo atlikėjas
– **#EXTGENRE** – albumo žanras
– **#EXTM3A** – vieno failo grojaraštis, skirtas albumo takeliams arba skyriams.
– **#EXTBYT:** – Failo dydis baitais.
- **#EXTBIN:** - Toliau pateikiami dvejetainiai duomenys.
– **#EXTIMG:** – logotipas, viršelis ar kiti vaizdai.

### HLS M3U ###

HLS (HTTP Live Streaming) sukūrė Apple, kad transliuotų garsą ir radiją į iOS įrenginius. Jis pagrįstas UTF-8 koduotu išplėstiniu M3U. IETF jį standartizavo kaip RFC 8216 2017 m. HLS grojaraščio žymos prasideda #EXT-X-. Toliau pateikiamas HLS žymų sąrašas

– **EXT-X-VERSION** – nurodo failo suderinamumo versiją, pagrįstą laikmena ir jos serveriu.
– **#EXT-X-START:** – nurodo pageidaujamą grojaraščio pradžios tašką.
– **#EXT-X-PLAYLIST-TYPE:** – pateikia grojaraščio tipą (EVENT arba VOD).
– **#EXT-X-TARGETDURATION:** – nurodo maksimalią Segmento trukmę.
- **#EXT-X-MEDIA-SEQUENCE:** - nurodo laikmenos sekos numerį.
– **#EXT-X-INDEPENDENT-SEGMENTS** – tai rodo, kad visi medijos pavyzdžiai yra nepriklausomi ir gali būti iškoduoti be kitų segmentų.
– **#EXT-X-MEDIA:** – naudojama medijos grojaraščiams, kuriuose yra alternatyvių to paties turinio pateikimų, susieti.
– **#EXT-X-STREAM-INF:** – nurodo srauto variantą, kuris yra perteikimų dalis.
– **#EXT-X-BYTERANGE:** – Nurodo, kad medijos segmentas yra URI identifikuoto šaltinio pogrupis.
– **#EXT-X-DISCONTINUITY** – nurodo ankstesnių ir paskesnių medijos segmentų nutrūkimą.
– **#EXT-X-DISCONTINUITY-SEQUENCE:** – leidžia sinchronizuoti skirtingus to paties varianto srauto arba skirtingų variantų srautų perteikimus.
– **#EXT-X-KEY:** – nurodo, kaip iššifruoti medijos segmentus.
– **#EXT-X-MAP:** – nurodo, kaip gauti laikmenos inicijavimo skyrių. Būtina išanalizuoti taikomus medijos segmentus.
- **#EXT-X-PROGRAM-DATE-TIME:** - It associates the first sample of the Media Segment with an absolute date and/or time.
– **#EXT-X-DATERANGE:** – susieja duomenų diapazoną.
– **#EXT-XI-FRAMES-ONLY** – nurodo, kad kiekvienas grojaraščio medijos segmentas apibūdina vieną I kadrą.
- **EXT-XI-FRAME-STREAM-INF** - Tai rodo, kad grojaraščio faile yra daugialypės terpės pristatymo I-kadrai.
– **#EXT-X-SESSION-DATA:** – leidžia būti savavališkais seanso duomenimis
įtraukta į pagrindinį grojaraštį.
– **#EXT-X-SESSION-KEY:** – leidžia naudoti šifravimo raktus. Klientas gali iš anksto įkelti šiuos klavišus neperskaitęs grojaraščio.
– **#EXT-X-ENDLIST** – tai rodo, kad daugiau medijos segmentų nebus įtraukta į failą.

Toliau pateikiamas M3U naudojamų interneto medijos tipų sąrašas:

- **application/vnd.apple.mpegurl**: tai vienintelis registruotas medijos tipas (registruotas 2009 m.), skirtas M3U, naudojamas HLS programų grojaraščiams nurodyti.
– Ne HLS programose naudojamos toliau nurodytos interneto medijos rūšys.
  - "**application/mpegurl**"
  - "**application/x-mpegurl**"
  - "**garsas/mpegurl**"
  - "**garsas/x-mpegurl**"

## M3U pavyzdys Nr.

Tai yra M3U failo pavyzdys.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Nuorodos Nr.

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [HTTP Live Streaming](https://tools.ietf.org/html/rfc8216)

