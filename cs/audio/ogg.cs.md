---
date: 2019-12-13
keywords: ogg, formát souboru ogg, přípona .ogg, formát zvuku ogg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Přečtěte si o formátu souboru OGG a rozhraních API, která mohou vytvářet a otevírat soubory OGG."
title: Soubor OGG – zvukový soubor Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Co je soubor OGG?

OGG je komprimovaný zvukový soubor Ogg Vorbis, který je uložen s příponou .ogg. Soubory OGG se používají k ukládání zvukových dat a mohou obsahovat také informace o interpretovi a skladbě a metadata. OGG je bezplatný a otevřený formát kontejneru, který spravuje nadace Xiph.Org Foundation.

## Stručná historie formátu souborů OGG

Projekt Ogg začal jako součást většího projektu v roce 1993 a byl pojmenován Squish, ale kvůli existující ochranné známce byl přejmenován na OggSquish. Byl popsán jako pokus o vytvoření flexibilního komprimovaného zvukového formátu pro moderní zvukové aplikace. OGG reference byla oddělena od Vorbis 2. září 2000.

OGM byl vytvořen v roce 2002 kvůli nedostatku formální podpory videa v OGG. To umožnilo vkládání videa z rozhraní Microsoft DirectShow do obalu založeného na OGG. V roce 2006 byl OGG podporován mnoha videoherními motory a byl běžně používán ke kódování bezplatného obsahu. Free Software Foundation zahájila 15. května 2007 kampaň s cílem zvýšit používání Vorbisu jako lepší alternativy k MP3. Do 30. června 2009 byl OGG jediným formátem kontejneru podporovaným implementací HTML5 Firefoxu 3.5.

## Formát souboru OGG

Formát OGG se skládá z bloků dat. Každý blok se nazývá stránka Ogg. Každá stránka začíná "OggS" pro identifikaci formátu Ogg. Záhlaví obsahuje sériové číslo a číslo stránky, které identifikuje každou stránku jako součást série. Stránka se skládá z následujících komponent.

- **Záhlaví stránky**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Bit | Hodnota | Popis |
| --- | --- | --- |
| 0 | 0x01 | Označuje, že první paket stránky je pokračováním předchozího paketu v logickém bitovém toku. |
| 1 | 0x02 | Označuje, že tato stránka je první v logickém bitovém proudu. |
| 2 | 0x04 | Označuje, že tato stránka je poslední v logickém bitovém proudu. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadata**: VorbisComment je nejrozšířenější mechanismus pro ukládání metadat. Mezi další mechanismy patří následující:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Reference ##

- [OGG - Wikipedie](https://en.wikipedia.org/wiki/Ogg)

