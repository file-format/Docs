---
date: 2020-08-12
keywords: jxr, .jxr, jxr file format, how to open jxr files, .jxr extension, jxr extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JXR failo formaat
linktitle: JXR
description: Luždirbti apie JXR failo formatą ir API, kurios gali sukurti ir atidaryti JXR failąs.
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Kas yra JXR failas? ##

JPEG XR (JPEG išplėstinis diapazonas) yra nepertraukiamo atspalvio fotografinių vaizdų failo formatas. Tai nejudančių vaizdų glaudinimo standartas, pagrįstas Microsoft sukurta HD nuotrauka. Jis palaiko ir nuostolingą, ir be nuostolių suspaudimą.

## Trumpa istorija ##

Windows Media Photo was first announced by Microsoft at WinHEC 2006. 2006 m. lapkričio mėn. jis buvo pervadintas į HD Photo. JPEG XR kaip tarptautinis standartas ISO/IEC 29199-2 patvirtintas 2009 m. birželio 19 d. ITU-T ir ISO/IEC paskelbė judėjimo formato specifikaciją (ITU-T T.833 | ISO/ IEC 29199-3), atitikties bandymo rinkinį (ITU-T T.834 | ISO/IEC 29199-4) ir pamatinę programinę įrangą (ITU-T T.835 | ISO/IEC 29199-5), skirtą JPEG XR užbaigus vaizdų kodavimo specifikacijos 2010 m. Techninė ataskaita, kurioje aprašoma JPEG XR darbo eigos architektūra, buvo paskelbta 2011 m.

## JPEG XR dizainas ##

Palyginti su JPEG, JPEG XR siūlo keletą patobulinimų, įskaitant:

- **Geresnis suspaudimas**: JPEG XR siūlo didesnį suspaudimo laipsnį.
- **Nuostolingas glaudinimas**: JPEG XR palaiko glaudinimą be nuostolių.
- **Plytelių struktūra**: JPEG XR vaizdą galima suskirstyti į plytelių sritis, kur kiekvieną regioną galima iššifruoti atskirai.
- **Daugesnis spalvų tikslumas**: JPEG XR apima vidinį konvertavimą į YCoCg spalvų erdvę, kad būtų palaikomi vaizdai naudojant RGB spalvų erdvę. JPEG XR taip pat palaiko 16 bitų vienam komponentui (64 bitų vienam pikseliui) sveikojo skaičiaus CMYK spalvų modelį. JPEG XR palaiko HDR vaizdų RGBE bendro eksponento slankiojo kablelio spalvų formatą. JPEG XR taip pat palaiko pilkos spalvos ir kelių kanalų spalvų kodavimą.
- **Skaidrumo žemėlapis**: JPEG XR palaiko alfa kanalą skaidrumui užtikrinti.
- **Suspausto domeno vaizdo modifikavimas**: JPEG XR vaizdus galima konvertuoti į nuostolingą kodavimą, sumažinti skiriamąją gebą, apkarpyti, apversti, pasukti, o plytelių struktūrą galima pakeisti visiškai neiššifruojant failo.
– **Metaduomenų palaikymas**: JPEG XR vaizdo faile gali būti ICC spalvų profilis, kad spalvos būtų vienodai atvaizduojamos keliuose įrenginiuose. Formatas taip pat palaiko Exif ir XMP metaduomenų formatus.

## Sudėtinio rodinio formatas ##

JPEG XR vaizdo duomenys gali būti saugomi TIFF tipo konteinerio formatu, naudojant vaizdų failų katalogo (IFT) žymų lentelę. JXR faile IFD žymose yra:

- Vaizdo duomenys: tai gretimi savarankiški vaizdo duomenys.
- Pasirenkami alfa kanalo duomenys: jei jie yra, vaizdo duomenis galima suspausti atskirai, kad būtų galima palaikyti programas, kurios nepalaiko skaidrumo.
- Metaduomenys
- Pasirenkami XMP metaduomenys
- Neprivalomi Exif metaduomenys

Kadangi jis pagrįstas TIFF formatu, jis paveldi visus TIFF formato apribojimus, pvz., 4 GB failo dydžio apribojimą.

## Nuorodos Nr.

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

