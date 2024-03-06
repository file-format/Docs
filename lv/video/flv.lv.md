---
date: 2019-10-11
keywords: flv, .flv, flv file format, .flv file format, .flv extension, flv extension, flv video format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lnopelniet par FLV faila formātu un API, kas var izveidot un atvērt FLV failus.
title: FLV faila formaat
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Kas ir FLV fails? ##

FLV (Flash Video) is a container file format with the .flv extension. FLV is used to deliver audio/video content over the internet by using the Adobe Flash Player or Adobe Air. The data in FLV files are encoded in the same way as SWF files. The direct support was added to Flash Player 7 in 2003. Adobe sistēmas F4V izveidoja 2007. gadā FLV ierobežojumu dēļ.

### Kodējums ###

FLV files contain video bitstreams of Sorenson Spark which are a proprietary variant of the H.263 video standard. It is the required compression format for Flash Player 6 and 7. Flash Player atbalsta 8. versija On2 TrueMotion VP6 video bitu straumēm. Tas ir ieteicamais saspiešanas formāts Flash Player 8 un jaunākām versijām. FLV atbalsta audio MP3 formātā, Nellymoser Asao Codec un atvērtā pirmkoda Speex kodeku. Tā atbalsta arī nesaspiestu audio vai ADPCM formāta audio. AAC (HE-AAC/AAC SBR, AAC galvenais profils un AAC-LC) atbalsta jaunākās Flash Player 9 versijas.

## Struktūra ##

FLV faili sastāv no galvenes un paketēm. FLV fails sākas ar galveni. Galvenē ir šādi lauki.

- **Paraksts**: tā vērtība ir FLV
- **Version**: Its default value is 1. Tikai 0x01 ir derīgs.
- **Karodi**: 0x04 tiek izmantots audio un 0x01 tiek izmantots video, tāpēc 0x05 tiek izmantots gan audio, gan video.
- **Header Size**: The default value is 9. To izmanto, lai izlaistu jaunāku izvērsto galveni.

Pēc galvenes nāk paketes. FLV fails ir sadalīts vairākās paketēs, ko sauc par FLV tagiem un kurām ir 15 baitu galvenes. Paketēs ir ietverti audio, video, skriptu, šifrēšanas informācijas un slodzes metadati. FLV paketēm ir šādi lauki.

- **Rezervēts**: tas ir rezervēts FMS, un tam jābūt 0.
- **Filtrs**: norāda, vai paketes ir vai nav filtrētas.
  - "**0**: iepriekšēja apstrāde nav nepieciešama. To izmanto nešifrētiem failiem."
  - "**1**: nepieciešama iepriekšēja apstrāde. To izmanto šifrētiem failiem"
- **Paketes veids**: tas nosaka paketes satura veidu.
  - "**8**: audio"
  - "**9**: video"
  - "**18**: skripta dati"
- **Datu lielums**: tas norāda ziņojuma garumu.
- **Laikspiedols zemāks**: tiek saglabāts laikspiedols milisekundēs, kad tiek lietoti taga dati. Pirmajai paketei tas ir iestatīts uz NULL.
- **Timestamp Upper**: paplašinājums, lai izveidotu uint32_be vērtību.
- **Straumes ID**: pirmajai straumei tas ir iestatīts uz NULL.
- **Payload Data**: šie ir dati, kuru pamatā ir pakešu veids.

## Atsauces Nr.

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

