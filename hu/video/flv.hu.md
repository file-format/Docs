---
date: 2019-10-11
keywords: flv, .flv, flv fájlformátum, .flv fájlformátum, .flv kiterjesztése, flv kiterjesztése, flv videó formátum
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Ismerje meg az FLV fájlformátumot és az API-kat, amelyek FLV-fájlokat hozhatnak létre és nyithatnak meg."
title: FLV fájl formátum
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Mi az az FLV fájl? ##

Az FLV (Flash Video) egy tárolófájl formátum .flv kiterjesztéssel. Az FLV audio/video tartalom interneten keresztül történő továbbítására szolgál Adobe Flash Player vagy Adobe Air használatával. Az FLV-fájlok adatai ugyanúgy vannak kódolva, mint az SWF-fájlok. A közvetlen támogatást 2003-ban adták hozzá a Flash Player 7-hez. Az Adobe rendszerek 2007-ben hozták létre az F4V-t az FLV korlátozásai miatt.

### Kódolás ###

Az FLV fájlok a Sorenson Spark videó bitfolyamait tartalmazzák, amelyek a H.263 videószabvány szabadalmaztatott változatai. Ez a szükséges tömörítési formátum a Flash Player 6-hoz és 7-hez. A Flash Player 8-as verziója támogatja az On2 TrueMotion VP6 videó bitfolyamokat. Ez az ajánlott tömörítési formátum a Flash Player 8 és újabb verzióihoz. Az FLV támogatja az MP3-as hangot, a Nellymoser Asao Codec-et és a nyílt forráskódú Speex kodeket. Támogatja a tömörítetlen vagy ADPCM formátumú hangot is. Az AAC-t (HE-AAC/AAC SBR, AAC Main Profile és AAC-LC) támogatja a Flash Player 9 legújabb verziója.

## Szerkezet ##

Az FLV fájlok fejlécből és csomagokból állnak. Az FLV fájl a fejléccel kezdődik. A fejléc a következő mezőket tartalmazza.

- **Aláírás**: Értéke FLV
- **Verzió**: Az alapértelmezett értéke 1. Csak a 0x01 érvényes.
- **Flags**: A 0x04 hanghoz, a 0x01 a videóhoz, tehát a 0x05 hanghoz és videóhoz egyaránt használható.
- **Fejléc mérete**: Az alapértelmezett érték 9. Egy újabb kiterjesztett fejléc kihagyására szolgál.

A fejléc után jön a Packets. Az FLV-fájl több, 15 bájtos fejléccel rendelkező, FLV-címkéknek nevezett csomagra van felosztva. A csomagok a hang, a kép, a szkriptek, a titkosítási információk és a rakomány metaadatait tartalmazzák. Az FLV-csomagok a következő mezőkkel rendelkeznek.

- **Fenntartva**: FMS számára van fenntartva, és 0-nak kell lennie.
- **Szűrő**: Azt jelzi, hogy a csomagok szűrve vannak-e vagy sem.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Packet Type**: Ez határozza meg a csomagban lévő tartalom típusát.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Adatméret**: Az üzenet hosszát jelöli.
- **Időbélyeg alsó**: Ez az időbélyeget ezredmásodpercben tárolja, amikor a címkeadatok érvényesek. Az első csomag NULL-ra van állítva.
- **Időbélyeg Felső**: Kiterjesztés az uint32_be érték létrehozásához.
- **Stream ID**: Az első adatfolyamnál NULL értékre van állítva.
- **Payload Data**: Ezek a csomagtípuson alapuló adatok.

## Referenciák ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

