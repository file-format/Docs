---
date: 2019-10-11
keywords: flv, .flv, formát souboru flv, formát souboru .flv, přípona .flv, přípona flv, formát videa flv
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souboru FLV a rozhraních API, která mohou vytvářet a otevírat soubory FLV."
title: Formát souboru FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Co je soubor FLV? ##

FLV (Flash Video) je kontejnerový formát souboru s příponou .flv. FLV se používá k doručování audio/video obsahu přes internet pomocí Adobe Flash Player nebo Adobe Air. Data v souborech FLV jsou kódována stejným způsobem jako soubory SWF. Přímá podpora byla přidána do Flash Player 7 v roce 2003. Systémy Adobe vytvořily F4V v roce 2007 kvůli omezením FLV.

### Kódování ###

Soubory FLV obsahují bitové toky videa Sorenson Spark, které jsou proprietární variantou standardu videa H.263. Je to požadovaný kompresní formát pro Flash Player 6 a 7. Verze 8 Flash Player podporuje video bitové toky On2 TrueMotion VP6. Je to doporučený kompresní formát pro Flash Player 8 a vyšší. FLV podporuje zvuk ve formátu MP3, kodek Nellymoser Asao a open source kodek Speex. Podporuje také nekomprimovaný zvuk nebo zvuk ve formátu ADPCM. AAC (HE-AAC/AAC SBR, AAC Main Profile a AAC-LC) jsou podporovány v nejnovějších verzích Flash Player 9.

## Struktura ##

Soubory FLV se skládají ze záhlaví a paketů. Soubor FLV začíná záhlavím. Záhlaví obsahuje následující pole.

- **Podpis**: Jeho hodnota je FLV
- **Verze**: Jeho výchozí hodnota je 1. Platí pouze 0x01.
- **Flags**: 0x04 se používá pro zvuk a 0x01 se používá pro video, takže 0x05 se používá pro zvuk i video.
- **Velikost záhlaví**: Výchozí hodnota je 9. Používá se k přeskočení novějšího rozšířeného záhlaví.

Po záhlaví následují pakety. Soubor FLV je rozdělen do několika paketů nazývaných značky FLV, které mají 15bajtová záhlaví. Pakety obsahují metadata pro zvuk, video, skripty, informace o šifrování a užitečné zatížení. Pakety FLV mají následující pole.

- **Vyhrazeno**: Je rezervováno pro FMS a mělo by být 0.
- **Filter**: Označuje, zda jsou pakety filtrovány nebo ne.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Typ paketu**: Definuje typ obsahu v paketu.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Velikost dat**: Označuje délku zprávy.
- **Timestamp Lower**: Toto ukládá časové razítko v milisekundách, kdy se data tagu použijí. Pro první paket je nastavena na NULL.
- **Timestamp Upper**: Rozšíření pro vytvoření hodnoty uint32_be.
- **ID streamu**: Toto je nastaveno na hodnotu NULL pro první stream.
- **Payload Data**: Jedná se o data založená na typu paketu.

## Reference ##

- [Flash Video - Wikipedie](https://en.wikipedia.org/wiki/Flash_Video)

