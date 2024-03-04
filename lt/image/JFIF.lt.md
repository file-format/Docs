---
date: 2020-08-12
keywords: jfif, .jfif, jfif file format, how to open jfif files, .jfif extension, jfif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF failas – kas yra .jfif failase?
linktitle: JFIF
description: Luždirbti apie JFIF failo formatą ir API, kurios gali sukurti ir atidaryti JFIF failąs.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Kas yra JFIF failas?

JFIF (JPEG failų mainų formatas (JFIF)) yra vaizdo formato failas, kuriame naudojamas .jfif plėtinys. JFIF sukuria per JIF (JPEG mainų formatą), sumažindamas sudėtingumą ir pašalindamas jo apribojimus.

## Trumpa JFIF istorija

JFIF document development was led by Eric Hamilton and an agreement on the first version was established in late 1991. 1.02 versija buvo paskelbta 1992 m. rugsėjo 7 d. RFC 2046 nurodė, kad JFIF formatas naudojamas JPEG vaizdams perduoti internetu. JFIF paskelbė ECMA 2009 m., o ITU-T 2011 m. standartizavo kaip savo rekomendaciją T.871, o ISO/IEC 2013 m. kaip ISO/IEC 10918-5

## JFIF failo formatas ##

JFIF failą sudaro žymeklių seka, kaip apibrėžta JPEG standarto 1 dalyje. Kiekvienas žymeklis susideda iš dviejų baitų (FF, po kurio seka baitas, nurodantis žymeklio tipą). Žymekliai gali būti atskiri arba nurodyti žymeklio segmento pradžią.

JFIF leidžia keliems komponentams, pvz., Y, Cb, Cr, turėti skirtingą skiriamąją gebą, tačiau jų lygiavimas nėra apibrėžtas. Skirtingai nei JPEG, JFIF gali pateikti informaciją apie skiriamąją gebą ir formato santykį. JFIF taip pat apibrėžia naudotiną spalvų modelį.

### Failo struktūra ##

|Segmentas|Kodas|Aprašymas|
|---|---|---|
|SOI|FF D8|Vaizdo pradžia|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|papildomi žymeklio segmentai|
|SOS|FF DA|Nuskaitymo pradžia|
||suspausti vaizdo duomenys||
|EOI|FF D9|Vaizdo pabaiga|

JFIF standartas apibrėžia šiuos segmentus:

### JFIF APP0 žymeklio segmentas ###

Tai privalomas segmentas, kuriame yra vaizdo parametrų. Jame taip pat gali būti įterpta nesuspausta miniatiūra.

|Laukas|Dydis (baitai)|Aprašymas|
|---|---|---|
|APP0 žymeklis|2|FF E0|
|Ilgis|2|Segmento ilgis be APP0 žymeklio|
|Identifier|5|JFIF (4A 46 49 46 00) ASCII baigiamas nuliniu baitu|
|JFIF versija|2|JFIF versija|
|Tankio vienetai|1|Šių pikselių tankio laukų vienetas</br> 00 : Nėra vienetų; plotis:aukštis pikselių formato santykis yra lygus Ydensity:Xdensity</br> 01: pikselių colyje</br> 02 : pikseliai centimetre|
|Xdensity|2|Horizontalus pikselių tankis didesnis už nulį|
|Density|2|Vertikalusis pikselių tankis didesnis už nulį|
|Xthumbnail|1|Horizontalus įterptosios RGB miniatiūros pikselių skaičius. Gali buti nulis|
|Ythumbnail|1|Vertikalus įterptosios RGB miniatiūros pikselių skaičius. Gali buti nulis|
|Miniatūros duomenys|3 × n|Nesuspausti 24 bitų RGB rastriniai miniatiūros duomenys|

### JFIF plėtinio APP0 žymeklio segmentas ###

Tai yra pasirenkama sekcija, kuri, jei ji apibrėžta, turi iš karto po JFIF APP0 žymeklio segmento. Šią skiltį palaiko JFIF 1.02 ir naujesnė versija ir leidžia įterpti trijų skirtingų formatų miniatiūras.

|Laukas|Dydis (baitai)|Aprašymas|
|---|---|---|
|APP0 žymeklis|2|FF E0|
|Ilgis|2|Segmento ilgis be APP0 žymeklio|
|Identifier|5|JFXX (4A 46 58 58 00) ASCII baigiamas nuliniu baitu|
|Miniatūros formatas|1|Nurodo, koks duomenų formatas naudojamas šiai įterptajai miniatiūrai:</br> 10 : JPEG formatas</br> 11 : 1 baitas vienam pikseliui paletintas formatas</br> 13 : 3 baitai pikseliui RGB formatas|
|Miniatūros duomenys|kintamasis||

## JFIF konvertavimas į kitus vaizdo failų formatus

JFIF galima konvertuoti į populiarius vaizdo failų formatus, tokius kaip [PNG](/image/png/), [JPG](/image/jpeg/) ir [PDF](/pdf/).

## Nuorodos Nr.

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

