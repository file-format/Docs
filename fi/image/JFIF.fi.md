---
date: 2020-08-12
keywords: jfif, .jfif, jfif file format, how to open jfif files, .jfif extension, jfif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF-tiedosto - Mikä on .jfif-tiedostoe?
linktitle: JFIF
description: Lansaitse JFIF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JFIF-tiedostons.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Mikä on JFIF-tiedosto?

JFIF (JPEG File Interchange Format (JFIF)) on kuvamuotoinen tiedosto, joka käyttää .jfif-tunnistetta. JFIF rakentaa JIF:n (JPEG Interchange Format) päälle vähentämällä monimutkaisuutta ja ratkaisemalla sen rajoituksia.

## JFIF:n lyhyt historia

JFIF document development was led by Eric Hamilton and an agreement on the first version was established in late 1991. Versio 1.02 julkaistiin 7. syyskuuta 1992. RFC 2046 määritti, että JFIF-muotoa käytetään JPEG-kuvien lähettämiseen Internetin kautta. ECMA julkaisi JFIF:n vuonna 2009, ja ITU-T standardoi sen vuonna 2011 suosituksensa T.871 ja ISO/IEC vuonna 2013 ISO/IEC 10918-5.

## JFIF-tiedostomuoto ##

JFIF-tiedosto koostuu JPEG-standardin osassa 1 määritellystä merkkijonosta. Jokainen merkki koostuu kahdesta tavusta (FF, jota seuraa tavu, joka määrittää merkin tyypin). Merkit voivat olla joko itsenäisiä tai osoittavat merkkisegmentin alkua.

JFIF sallii useiden komponenttien, kuten Y, Cb, Cr, eri resoluution, mutta niiden kohdistusta ei ole määritelty. Toisin kuin JPEG, JFIF voi tarjota tarkkuus- ja kuvasuhdetietoja. JFIF määrittelee myös käytettävän värimallin.

### Tiedostorakenne ##

|Segmentti|Koodi|Kuvaus|
|---|---|---|
|SOI|FF D8|Kuvan alku|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|muut merkkisegmentit|
|SOS|FF DA|Skannauksen aloitus|
||pakatut kuvatiedot||
|EOI|FF D9|Kuvan loppu|

JFIF-standardi määrittelee seuraavat segmentit:

### JFIF APP0 -merkkisegmentti ###

Se on pakollinen segmentti, joka sisältää kuvaparametreja. Se voi sisältää myös upotetun pakkaamattoman pikkukuvan.

|Kenttä|Koko (tavuja)|Kuvaus|
|---|---|---|
|APP0-merkki|2|FF E0|
|Pituus|2|Segmentin pituus ilman APP0-merkkiä|
|Identifier|5|JFIF (4A 46 49 46 00) ASCII:ssa, joka päättyy nollatavulla|
|JFIF-versio|2|JFIF-versio|
|Tiheysyksiköt|1|Yksikkö seuraaville pikselitiheyskentille</br> 00 : Ei yksiköitä; leveys:korkeus pikselin kuvasuhde on yhtä suuri kuin Ydensity:Xdensity</br> 01 : pikseliä tuumaa kohti</br> 02 : pikseliä senttimetrissä|
|Xdensity|2|Vaakasuuntainen pikselitiheys suurempi kuin nolla|
|Ydensity|2|Pysty pikselitiheys suurempi kuin nolla|
|Xthumbnail|1|Upotetun RGB-pikkukuvan vaakasuuntainen pikselimäärä. Saattaa olla nolla|
|Ythumbnail|1|Upotetun RGB-pikkukuvan pystysuuntainen pikselimäärä. Saattaa olla nolla|
|Pikkukuvatiedot|3 × n|Pakkaamaton 24-bittinen RGB-rasteripikkukuvadata|

### JFIF-laajennuksen APP0 merkkisegmentti ###

Tämä on valinnainen osio, jonka on välittömästi seurattava JFIF APP0 -merkkisegmenttiä, jos se on määritetty. Tätä osiota tukevat JFIF-versio 1.02 ja uudemmat, ja se mahdollistaa pikkukuvien upottamisen kolmessa eri muodossa.

|Kenttä|Koko (tavuja)|Kuvaus|
|---|---|---|
|APP0-merkki|2|FF E0|
|Pituus|2|Segmentin pituus ilman APP0-merkkiä|
|Identifier|5|JFXX (4A 46 58 58 00) ASCII:ssa, joka päättyy nollatavulla|
|Pikkukuvan muoto|1|Määrittää, mitä tietomuotoa käytetään seuraavassa upotetussa pikkukuvassa:</br> 10 : JPEG-muoto</br> 11 : 1 tavu pikseliä kohden paletoitu muoto</br> 13 : 3 tavua pikseliä kohden RGB-muoto|
|Pikkukuvatiedot|muuttuja||

## JFIF:n muuntaminen muihin kuvatiedostomuotoihin

JFIF voidaan muuntaa suosittuihin kuvatiedostomuotoihin, kuten [PNG](/image/png/), [JPG](/image/jpeg/) ja [PDF](/pdf/).

## Viitteet ##

- {{HYPERLINKKI1}}

