---
date: 2019-10-11
keywords: flv, .flv, flv file format, .flv file format, .flv extension, flv extension, flv video format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Luždirbti apie FLV failo formatą ir API, kurios gali sukurti ir atidaryti FLV failąs.
title: FLV failo formaat
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Kas yra FLV failas? ##

FLV (Flash Video) is a container file format with the .flv extension. FLV is used to deliver audio/video content over the internet by using the Adobe Flash Player or Adobe Air. The data in FLV files are encoded in the same way as SWF files. The direct support was added to Flash Player 7 in 2003. Adobe sistemos sukūrė F4V 2007 m. dėl FLV apribojimų.

### Kodavimas ###

FLV files contain video bitstreams of Sorenson Spark which are a proprietary variant of the H.263 video standard. It is the required compression format for Flash Player 6 and 7. 8 Flash Player palaikymo versija On2 TrueMotion VP6 vaizdo įrašų bitų srautams. Tai rekomenduojamas glaudinimo formatas Flash Player 8 ir naujesnėms versijoms. FLV palaiko garsą MP3 formatu, Nellymoser Asao Codec ir atvirojo kodo Speex kodeką. Jis taip pat palaiko nesuspaustą garsą arba ADPCM formato garsą. AAC (HE-AAC / AAC SBR, AAC pagrindinis profilis ir AAC-LC) palaiko naujausios Flash Player 9 versijos.

## Struktūra Nr.

FLV failus sudaro antraštė ir paketai. FLV failas prasideda antrašte. Antraštėje yra šie laukai.

- **Parašas**: jo reikšmė yra FLV
- **Version**: Its default value is 1. Galioja tik 0x01.
- **Vėliavos**: 0x04 naudojamas garsui, o 0x01 naudojamas vaizdo įrašams, taigi 0x05 naudojamas ir garsui, ir vaizdui.
- **Header Size**: The default value is 9. Jis naudojamas norint praleisti naujesnę išplėstinę antraštę.

Po antraštės ateina paketai. FLV failas yra padalintas į kelis paketus, vadinamus FLV žymomis, turinčiomis 15 baitų antraštes. Paketuose yra garso, vaizdo, scenarijų, šifravimo informacijos ir naudingos apkrovos metaduomenys. FLV paketai turi šiuos laukus.

- **Rezervuota**: rezervuota FMS ir turėtų būti 0.
- **Filtras**: nurodo, ar paketai filtruojami, ar ne.
  - "**0**: išankstinio apdorojimo nereikia. Tai naudojama nešifruotiems failams."
  - "**1**: reikalingas išankstinis apdorojimas. Tai naudojama užšifruotiems failams"
- **Paketo tipas**: apibrėžia paketo turinio tipą.
  - "**8**: garsas"
  - "**9**: vaizdo įrašas"
  - "**18**: scenarijaus duomenys"
- **Duomenų dydis**: nurodo pranešimo ilgį.
– **Laiko žyma žemesnė**: išsaugoma laiko žyma milisekundėmis, kai taikomi žymos duomenys. Pirmajam paketui jis nustatytas į NULL.
- **Timestamp Upper**: plėtinys, skirtas sukurti uint32_be reikšmę.
- **Srauto ID**: pirmam srautui nustatytas NULL.
- **Payload Data**: tai duomenys, pagrįsti paketo tipu.

## Nuorodos Nr.

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

