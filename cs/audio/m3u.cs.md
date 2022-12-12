---
date: 2019-12-13
keywords: m3u, formát souboru m3u, přípona .m3u, multimediální seznam stop m3u, formát seznamu stop m3u
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souboru M3U a rozhraních API, která mohou vytvářet a otevírat soubory M3U."
title: Formát souboru M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Co je soubor M3U? ##

M3U (MP3 URL) je soubor seznamu zvukových stop uložený s příponou .m3u. M3U není skutečný zvukový soubor, pouze ukazuje na zvukové a někdy i video soubory. M3U byl vyvinut pro použití se softwarem Winplay3 od Fraunhofer. Podporují jej také různé přehrávače médií a software.

## Formát souboru M3U

Pro formát souboru M3U neexistuje žádná oficiální specifikace, je to de-facto standard. M3U je prostý textový soubor, který používá příponu .m3u, pokud je text zakódován ve výchozím kódování místního systému bez Unicode, nebo s příponou .m3u8, pokud je text kódován UTF-8. Každá položka v souboru M3U může být jedna z následujících:

- Absolutní cesta k souboru
- Cesta k souboru vzhledem k souboru M3U.
- URL

### Rozšířené M3U ###

V rozšířeném M3U jsou zavedeny další direktivy, které začínají "#" a končí dvojtečkou(:), pokud mají parametry. Níže je uveden seznam direktiv pro rozšířené M3U.

- **#EXTM3U** - Je to hlavička souboru označující Extended M3U a musí být na prvním řádku souboru.
- **#EXTENC:** - Kódování textu. Musí to být 2. řádek souboru.
- **#EXTINF:** - Používá se pro informace o skladbě a další doplňkové vlastnosti.
- **#PLAYLIST:** - Název seznamu skladeb
- **#EXTGRP:** - Začněte seskupování jmen
- **#EXTALB:** - Informace o albu
- **#EXTART:** - Interpret alba
- **#EXTGENRE** - Žánr alba
- **#EXTM3A** - Seznam stop jednoho souboru pro stopy alba nebo kapitoly.
- **#EXTBYT:** - Velikost souboru v bajtech.
- **#EXTBIN:** - Následují binární data.
- **#EXTIMG:** - Logo, obálka nebo jiné obrázky.

### HLS M3U ###

HLS (HTTP Live Streaming) byl vytvořen společností Apple pro streamování zvuku a rádia do zařízení iOS. Je založen na rozšířeném M3U kódovaném UTF-8. To bylo standardizováno jako RFC 8216 v roce 2017 IETF. Značky pro seznam stop HLS začínají „#EXT-X-“. Níže je uveden seznam značek pro HLS

- **EXT-X-VERSION** - Označuje verzi kompatibility souboru na základě média a jeho serveru.
- **#EXT-X-START:** - Označuje preferovaný počáteční bod seznamu skladeb.
- **#EXT-X-PLAYLIST-TYPE:** - Poskytuje typ seznamu stop (EVENT nebo VOD).
- **#EXT-X-TARGETDURATION:** - Určuje maximální dobu trvání segmentu.
- **#EXT-X-MEDIA-SEQUENCE:** - Označuje pořadové číslo média.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Označuje, že všechny vzorky médií jsou nezávislé a lze je dekódovat bez dalších segmentů.
- **#EXT-X-MEDIA:** - Používá se ke spojení seznamů médií, které obsahují alternativní ztvárnění stejného obsahu.
- **#EXT-X-STREAM-INF:** - Určuje tok variant, který je součástí interpretací.
- **#EXT-X-BYTERANGE:** - Označuje, že mediální segment je podrozsahem zdroje identifikovaného pomocí jeho URI.
- **#EXT-X-DISCONTINUITY** - Označuje diskontinuitu mezi předchozími a následujícími segmenty média.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Umožňuje synchronizaci mezi různými ztvárněními stejného Variant Stream nebo různých Variant Stream.
- **#EXT-X-KEY:** - Určuje způsob dešifrování segmentů médií.
- **#EXT-X-MAP:** - Určuje, jak získat oddíl inicializace média. Je nutné analyzovat příslušné mediální segmenty.
- **#EXT-X-PROGRAM-DATE-TIME:** - Přiřazuje první vzorek mediálního segmentu k absolutnímu datu a/nebo času.
- **#EXT-X-DATERANGE:** - Přidružuje rozsah dat.
- **#EXT-XI-FRAMES-ONLY** - Označuje, že každý mediální segment v seznamu stop popisuje jeden I-snímek.
- **EXT-XI-FRAME-STREAM-INF** - Označuje, že soubor seznamu stop obsahuje I-snímky multimediální prezentace.
- **#EXT-X-SESSION-DATA:** - Umožňuje libovolná data relace
přenášeny v hlavním seznamu skladeb.
- **#EXT-X-SESSION-KEY:** - Umožňuje šifrovací klíče. Klient může tyto klíče předem načíst, aniž by nejprve četl seznam skladeb.
- **#EXT-X-ENDLIST** - Označuje, že do souboru nebudou přidány žádné další segmenty médií.

Níže je uveden seznam typů internetových médií používaných M3U:

- **application/vnd.apple.mpegurl**: Je to jediný registrovaný typ média (registrovaný v roce 2009) pro M3U, který se používá k odkazování na seznamy stop v aplikacích HLS.
- Aplikace jiné než HLS používají následující typy internetových médií.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Příklad M3U ##

Toto je příklad souboru M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Reference ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
– [HTTP živé vysílání](https://tools.ietf.org/html/rfc8216)

