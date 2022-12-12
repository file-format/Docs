---
date: 2020-08-12
keywords: Formát souboru jxr, .jxr, jxr, jak otevřít soubory jxr, přípona .jxr, přípona jxr
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru JXR
linktitle: JXR
description: "Přečtěte si o formátu souborů JXR a rozhraních API, která mohou vytvářet a otevírat soubory JXR."
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Co je soubor JXR? ##

JPEG XR (JPEG rozšířený rozsah) je souborový formát pro fotografické obrázky se spojitými tóny. Jedná se o standard komprese statických obrázků, který je založen na HD Photo vyvinutém společností Microsoft. Podporuje ztrátovou i bezeztrátovou kompresi.

## Stručná historie ##

Windows Media Photo byl poprvé oznámen společností Microsoft na WinHEC 2006. V listopadu 2006 byl přejmenován na HD Photo. JPEG XR byl schválen jako mezinárodní standard ISO/IEC 29199-2 dne 19. června 2009. ITU-T a ISO/IEC zveřejnily návrh specifikace formátu (ITU-T T.833 | ISO/IEC 29199-3), sada testů shody (ITU-T T.834 | ISO/IEC 29199-4) a referenční software (ITU-T T.835 | ISO /IEC 29199-5) pro JPEG XR po dokončení specifikace kódování obrázků v roce 2010. Technická zpráva popisující architekturu pracovního postupu pro JPEG XR byla zveřejněna v roce 2011.

## JPEG XR Design ##

Ve srovnání s JPEG nabízí JPEG XR několik vylepšení, včetně:

- **Lepší komprese**: JPEG XR nabízí vyšší kompresní poměry.
- **Bezztrátová komprese**: JPEG XR podporuje bezeztrátovou kompresi.
- **Struktura dlaždic**: Obrázek JPEG XR lze segmentovat do oblastí dlaždic, kde lze každou oblast dekódovat samostatně.
- **Větší přesnost barev**: JPEG XR obsahuje interní převod do barevného prostoru YCoCg pro podporu obrázků využívajících barevný prostor RGB. JPEG XR také podporuje celočíselný barevný model CMYK s 16 bity na komponentu (64 bitů na pixel). JPEG XR podporuje formát barev s pohyblivou řádovou čárkou se sdíleným exponentem RGBE pro obrázky HDR. JPEG XR podporuje také kódování ve stupních šedi a vícekanálové barevné kódování.
- **Mapa průhlednosti**: JPEG XR podporuje alfa kanál pro průhlednost.
- **Úprava obrazu v komprimované doméně**: Obrázky JPEG XR lze převést do ztrátového kódování, snížit rozlišení, oříznout, převrátit, otočit a strukturu dlaždic lze změnit, to vše bez úplného dekódování souboru.
- **Podpora metadat**: Soubor obrázku JPEG XR může obsahovat barevný profil ICC pro konzistentní reprezentaci barev na více zařízeních. Formát také podporuje formáty metadat Exif a XMP.

## Formát kontejneru ##

Obrazová data JPEG XR lze uložit ve formátu kontejneru podobného TIFF pomocí tabulky značek Image File Directory (IFT). Soubor JXR obsahuje ve značkách IFD následující položky:

- Obrazová data: Jedná se o souvislá samostatná obrazová data.
- Volitelná data alfa kanálu: Pokud jsou k dispozici, lze obrazová data komprimovat samostatně, což umožňuje podporu aplikací, které nepodporují průhlednost.
- Metadata
- Volitelná metadata XMP
- Volitelná metadata Exif

Protože je založen na formátu TIFF, zdědí všechna omezení formátu TIFF, jako je limit velikosti souboru 4 GB.

## Reference ##

– [JPEG XR – Wikipedie](https://en.wikipedia.org/wiki/JPEG_XR)

