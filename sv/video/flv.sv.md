---
date: 2019-10-11
keywords: flv, .flv, flv-filformat, .flv-filformat, .flv-tillägg, flv-tillägg, flv-videoformat
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Lär dig om FLV-filformat och API:er som kan skapa och öppna FLV-filer." 
title: FLV-filformat
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Vad är en FLV fil? ##

FLV (Flash Video) är ett containerfilformat med filtillägget .flv. FLV används för att leverera ljud-/videoinnehåll över internet med hjälp av Adobe Flash Player eller Adobe Air. Data i FLV-filer kodas på samma sätt som SWF-filer. Det direkta stödet lades till i Flash Player 7 2003. Adobe-system skapade F4V 2007 på grund av begränsningarna i FLV.

### Kodning ###

FLV-filer innehåller videobitströmmar av Sorenson Spark som är en egenutvecklad variant av H.263-videostandarden. Det är det obligatoriska komprimeringsformatet för Flash Player 6 och 7. Version 8 av Flash Player-stöd för On2 TrueMotion VP6-videobitströmmar. Det är det rekommenderade komprimeringsformatet för Flash Player 8 och högre. FLV stöder ljud i MP3, Nellymoser Asao Codec och Speex-codec med öppen källkod. Den stöder också okomprimerat ljud eller ljud i ADPCM-format. AAC (HE-AAC/AAC SBR, AAC Main Profile och AAC-LC) stöds av de senaste versionerna av Flash Player 9.

## Struktur ##

FLV-filer består av Header och Packets. En FLV-fil börjar med rubriken. Rubriken har följande fält.

- **Signatur**: Dess värde är FLV
- **Version**: Dess standardvärde är 1. Endast 0x01 är giltigt.
- **Flaggor**: 0x04 används för ljud och 0x01 används för video så 0x05 används för både ljud och video.
- **Rubrikstorlek**: Standardvärdet är 9. Det används för att hoppa över en nyare utökad rubrik.

Efter rubriken kommer paketen. FLV-filen är uppdelad i flera paket som kallas FLV-taggar som har 15-byte rubriker. Paketen innehåller metadata för ljud, video, skript, krypteringsinformation och nyttolast. FLV-paketen har följande fält.

- **Reserverad**: Den är reserverad för FMS och ska vara 0.
- **Filter**: Indikerar om paketen är filtrerade eller inte.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Packet Type**: Detta definierar typen av innehåll i paketet.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Datastorlek**: Detta anger längden på meddelandet.
- **Timestamp Lower**: Detta lagrar tidsstämpeln i millisekunder vid vilken taggdata gäller. Den är inställd på NULL för det första paketet.
- **Timestamp Upper**: Tillägg för att skapa ett uint32_be-värde.
- **Stream ID**: Detta är inställt på NULL för den första streamen.
- **Nyttlastdata**: Detta är data baserad på pakettypen.

## Referenser ##

- [Flash-video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

