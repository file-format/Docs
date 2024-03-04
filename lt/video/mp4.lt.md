---
date: 2019-10-11
keywords: MP4, file, extension, format, video format, MPEG-4
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Luždirbti apie MP4 failo formatą ir API, kurios gali sukurti ir atidaryti MP4 failąs.
title: MP4 failo formaat
linktitle: MP4
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## Kas yra MP4 failas? ##

MP4(short for MPEG-4 Part 14) is a file format based on ISO/IEC 14496-12:2004 that is based on QuickTime File Format but formally specifies support for Initial Object Descriptors (IOD) and other MPEG features. It is mostly used to store video and audio but can also be used to store subtitles and still images. MP4 files are stored with the .mp4 extension. MP4 is an international audio-visual coding standard. Similar to most modern container formats, MP4 supports streaming over the internet. Due to the high compression used in MP4, the resultant files are smaller in size with almost all the original quality retained.

## Trumpa istorija ##

MP4 specification was developed by Moving Picture Experts Group (MPEG) and was based on the QuickTime format [MOV](/video/mov/) that was published in 2001. Pirmoji MP4 versija (ISO/IEC 14496-1:2001) buvo MPEG-4 1 dalies: sistemų specifikacijos, paskelbtos 1999 m., peržiūra. MP4 failo formatas buvo apibendrintas iki ISO bazinio laikmenos failo formato ISO/IEC 14496-12. :2004, kuris apibrėžė bendrą laiko laikmenų failų struktūrą. Dėl to jis naudojamas kaip kitų failų formatų pagrindas.

## MP4 failų struktūra ##

MP4 yra išplečiamas talpyklos failas, o tai reiškia, kad jis neapibrėžia griežtos struktūros ir leidžia kiekvienam medijos tipui pasirinkti tinkintą struktūrą ir hierarchiją. Duomenys MP4 faile yra suskirstyti į dvi dalis: pirmajame yra su medija susiję duomenys, o antrajame – metaduomenys. Medijos duomenyse yra garso arba vaizdo įrašų, o metaduomenys nurodo atsitiktinės prieigos vėliavėles, laiko žymes ir kt.
MP4 struktūros paprastai vadinamos atomais arba dėžėmis. Mažiausias atomo dydis yra 8 baitai (pirmieji 4 baitai nurodo dydį, o kiti 4 baitai nurodo tipą). Čia yra MP failuose esančių šakninio lygio atomų sąrašas:

- **ftyp**: Contains the file type, description, and the common data structures used.
- **pdin**: yra progresyvios vaizdo įrašų įkėlimo / atsisiuntimo informacijos.
- **moov**: visų filmų metaduomenų talpykla.
- **moof**: konteineris su vaizdo įrašo fragmentais.
- **mfra**: konteineris su atsitiktine prieiga prie vaizdo įrašo fragmento
- **mdat**: laikmenos duomenų talpykla.
- **stts**: imties ir laiko lentelė.
- **stsc**: lentelė nuo mėginio iki gabalo.
- **stsz**: pavyzdžių dydžiai (įrėminti)
- **meta**: konteineris su metaduomenų informacija.

Čia yra MP4 naudojamų antrojo lygio atomų sąrašas:

- **mvhd**: yra vaizdo įrašo antraštės informacija su visa vaizdo įrašo informacija.
- **trakas**: konteineris su atskiru takeliu.
- **udta**: konteineris su vartotojo ir takelio informacija.
- **iods**: MP4 failo aprašas

## Nuorodos Nr.

- [MP4 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

