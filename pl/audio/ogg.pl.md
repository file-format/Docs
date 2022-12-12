---
date: 2019-12-13
keywords: ogg, format pliku ogg, rozszerzenie .ogg, format audio ogg
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Dowiedz się więcej o formacie plików OGG i interfejsach API, które mogą tworzyć i otwierać pliki OGG."
title: Plik OGG — plik audio Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Czym jest plik OGG?

OGG to skompresowany plik audio Ogg Vorbis zapisany z rozszerzeniem .ogg. Pliki OGG służą do przechowywania danych audio i mogą zawierać informacje o wykonawcy i utworze oraz metadane. OGG to darmowy i otwarty format kontenera utrzymywany przez Fundację Xiph.Org.

## Krótka historia formatu pliku OGG

Projekt Ogg powstał jako część większego projektu w 1993 roku i nosił nazwę Squish, ale ze względu na istniejący znak towarowy został przemianowany na OggSquish. Zostało to opisane jako próba stworzenia elastycznego skompresowanego formatu audio dla nowoczesnych aplikacji audio. Odniesienie OGG zostało oddzielone od Vorbis 2 września 2000 r.

OGM powstał w 2002 roku z powodu braku formalnej obsługi wideo w OGG. Umożliwiło to osadzenie wideo z platformy Microsoft DirectShow w opakowaniu opartym na OGG. Do 2006 roku OGG był obsługiwany przez wiele silników gier wideo i był powszechnie używany do kodowania bezpłatnych treści. Fundacja Wolnego Oprogramowania rozpoczęła 15 maja 2007 r. kampanię mającą na celu zwiększenie wykorzystania Vorbis jako lepszej alternatywy dla MP3. Do 30 czerwca 2009 OGG był jedynym formatem kontenera obsługiwanym przez implementację HTML5 przeglądarki Firefox 3.5.

## Format pliku OGG

Format OGG składa się z porcji danych. Każdy fragment nazywany jest stroną Ogg. Każda strona zaczyna się od „OggS”, aby zidentyfikować format Ogg. Nagłówek zawiera numer seryjny i numer strony, który identyfikuje każdą stronę jako część serii. Strona składa się z następujących elementów.

- **Nagłówek**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Kawałek | Wartość | Opis |
| --- | --- | --- |
| 0 | 0x01 | Wskazuje, że pierwszy pakiet strony jest kontynuacją poprzedniego pakietu w logicznym strumieniu bitów. |
| 1 | 0x02 | Wskazuje, że ta strona jest pierwszą w logicznym strumieniu bitów. |
| 2 | 0x04 | Wskazuje, że ta strona jest ostatnią w logicznym strumieniu bitów. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Metadane**: VorbisComment to najczęściej obsługiwany mechanizm przechowywania metadanych. Inne mechanizmy obejmują:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Bibliografia ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

