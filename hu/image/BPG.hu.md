---
date: 2020-08-12
keywords: bpg, .bpg, bpg fájlformátum, bpg fájlok megnyitása, .bpg kiterjesztése, bpg kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: BPG fájl formátum
linktitle: BPG
description: "Ismerje meg a BPG fájlformátumot és az API-kat, amelyek BPG fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "image"
lastmod: 2021-20-01
---

## Mi az a BPG fájl? ##

A BPG (Better Portable Graphics) egy fájlformátum, amelyet Fabrice Bellard hozott létre 2014-ben digitális képekhez. A BPG-t javasolta a JPEG helyett, mivel a BPG tömörítési vagy mérethatékonyabb volt. A BPG a HEVC (High-Efficiency Video Coding) videótömörítési szabvány kereten belüli kódolását használja.

A BPG-t hordozható memória-hatékony formátumnak tervezték, amely kézi és IoT-eszközökön használható. Jelenleg a webböngészők nem támogatják a BPG formátumot, de a webhelyek továbbra is képesek BPG képeket megjeleníteni a Bellard által írt JavaScript-könyvtár használatával. A BPG a HEVC fő 4:4:4 16 állókép profilját használja mintánként legfeljebb 14 bites méretig.

## Műszaki adatok ##

A BPG-tároló formátum egy általános képformátum, nem pedig a HEVC-ben használt nyers bitfolyam. A BPG támogatja a 4:4:4, 4:2:2 és 4:2:0 színformátumokat. Az alfa-csatornát egy külön kódolt extra csatorna vagy a CMYK kép negyedik csatornája is támogatja. A BPG metaadat-támogatást biztosít az Exif, az ICC profilok és az XMP számára. A BPG támogatja az YCbCr (ITU-R BT.601, BT.709 és BT.2020 (nem állandó fénysűrűség)), YCgCo, RGB, CMYK és szürkeárnyalatos színteret. A BGP támogatja az animációt és a veszteséges és veszteségmentes HEVC adattömörítést is.

## Referenciák ##

- [Jobb hordozható grafika – Wikipédia](https://en.wikipedia.org/wiki/Better_Portable_Graphics)

