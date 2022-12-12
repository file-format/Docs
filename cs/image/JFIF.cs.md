---
date: 2020-08-12
keywords: jfif, .jfif, formát souboru jfif, jak otevřít soubory jfif, přípona .jfif, přípona jfif
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Soubor JFIF – Co je soubor .jfif?
linktitle: JFIF
description: "Přečtěte si o formátu souborů JFIF a rozhraních API, která mohou vytvářet a otevírat soubory JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Co je soubor JFIF?

JFIF (JPEG File Interchange Format (JFIF)) je soubor ve formátu obrázku, který používá příponu .jfif. JFIF staví přes JIF (JPEG Interchange Format) tím, že snižuje složitost a řeší jeho omezení.

## Stručná historie JFIF

Vývoj dokumentů JFIF vedl Eric Hamilton a dohoda o první verzi byla uzavřena koncem roku 1991. Verze 1.02 byla zveřejněna 7. září 1992. RFC 2046 specifikovalo, že formát JFIF se používá k přenosu obrázků JPEG přes internet. JFIF byl publikován ECMA v roce 2009 a byl standardizován ITU-T v roce 2011 jako jeho doporučení T.871 a ISO/IEC v roce 2013 jako ISO/IEC 10918-5

## Formát souboru JFIF ##

Soubor JFIF se skládá ze sekvence značek definovaných v části 1 standardu JPEG. Každá značka se skládá ze dvou bajtů (FF následovaný bajtem, který určuje typ značky). Značky mohou být buď samostatné, nebo mohou indikovat začátek segmentu značky.

JFIF umožňuje více komponentům jako Y, Cb, Cr mít různá rozlišení, ale jejich zarovnání není definováno. Na rozdíl od JPEG může JFIF poskytovat informace o rozlišení a poměru stran. JFIF také definuje barevný model, který se má použít.

### Struktura souboru ##

|Segment|Kód|Popis|
|---|---|---|
|SOI|FF D8|Začátek obrázku|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|další segmenty značek|
|SOS|FF DA|Začátek skenování|
||komprimovaná obrazová data||
|EOI|FF D9|Konec obrázku|

Standard JFIF definuje následující segmenty:

### segment značky JFIF APP0 ###

Je to povinný segment obsahující parametry obrázku. Může také obsahovat vložený nekomprimovaný náhled.

|Pole|Velikost (bajty)|Popis|
|---|---|---|
|Značka APP0|2|FF E0|
|Délka|2|Délka segmentu bez značky APP0|
|Identifikátor|5|JFIF (4A 46 49 46 00) v ASCII ukončený prázdným bajtem|
|Verze JFIF|2|Verze JFIF|
|Jednotky hustoty|1|Jednotky pro následující pole hustoty pixelů</br> 00 : Žádné jednotky; Poměr stran pixelů šířka:výška se rovná Ydensity:Xdensity</br> 01 : Pixely na palec</br> 02 : Pixely na centimetr|
|Xdensity|2|Horizontální hustota pixelů větší než nula|
|Ydensity|2|Vertikální hustota pixelů větší než nula|
|Xthumbnail|1|Horizontální počet pixelů vložené miniatury RGB. Může být nula|
|Ythumbnail|1|Vertikální počet pixelů vložené miniatury RGB. Může být nula|
|Data miniatur|3 × n|Nekomprimovaná data miniatur rastru 24 bitů RGB|

### Segment značky APP0 rozšíření JFIF ###

Toto je volitelná sekce, která, pokud je definována, musí bezprostředně následovat segment značky JFIF APP0. Tato část je podporována JFIF verze 1.02 a vyšší a umožňuje vkládání miniatur ve třech různých formátech.

|Pole|Velikost (bajty)|Popis|
|---|---|---|
|Značka APP0|2|FF E0|
|Délka|2|Délka segmentu bez značky APP0|
|Identifikátor|5|JFXX (4A 46 58 58 00) v ASCII ukončený prázdným bajtem|
|Formát miniatury|1|Uvádí, jaký formát dat se použije pro následující vloženou miniaturu:</br> 10: Formát JPEG</br> Paletizovaný formát 11 : 1 bajt na pixel</br> 13 : 3 bajty na pixel Formát RGB|
|Data miniatur|proměnná||

## Převod JFIF na jiné formáty obrazových souborů

JFIF lze převést na oblíbené formáty souborů obrázků, jako je [PNG](/cs/image/png/), [JPG](/cs/image/jpg/) a [PDF](/cs/pdf/).

## Reference ##

– [JFIF – Wikipedie](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

