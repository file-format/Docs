---
date: 2019-12-13
keywords: ogg, файлов формат ogg, разширение .ogg, аудио формат ogg
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Научете за OGG файловия формат и API, които могат да създават и отварят OGG файлове."
title: OGG файл - Ogg Vorbis аудио файл
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Какво е OGG файл?

OGG е компресиран аудио файл на Ogg Vorbis, който се запазва с разширението .ogg. OGG файловете се използват за съхраняване на аудио данни и могат да включват информация за изпълнител и запис, както и метаданни. OGG е безплатен и отворен контейнерен формат, който се поддържа от Xiph.Org Foundation.

## Кратка история на файловия формат OGG

Проектът Ogg стартира като част от по-голям проект през 1993 г. и беше наречен Squish, но поради съществуваща търговска марка беше преименуван на OggSquish. Той беше описан като опит за създаване на гъвкав компресиран аудио формат за модерни аудио приложения. Справката OGG беше отделена от Vorbis на 2 септември 2000 г.

OGM е създаден през 2002 г. поради липсата на официална видео поддръжка в OGG. Това позволи вграждане на видео от рамката на Microsoft DirectShow в обвивка, базирана на OGG. До 2006 г. OGG се поддържа от много машини за видеоигри и обикновено се използва за кодиране на безплатно съдържание. Фондацията за свободен софтуер започна кампания на 15 май 2007 г. за увеличаване на използването на Vorbis като по-добра алтернатива на MP3. До 30 юни 2009 г. OGG беше единственият контейнерен формат, поддържан от внедряването на HTML5 на Firefox 3.5.

## OGG файлов формат

Форматът OGG се състои от части от данни. Всяка част се нарича Ogg страница. Всяка страница започва с "OggS", за да идентифицира Ogg формат. Заглавката съдържа серийния номер и номера на страницата, които идентифицират всяка страница като част от поредица. Страницата се състои от следните компоненти.

- **Заглавен колонтитул на страница**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Бит | Стойност | Описание |
| --- | --- | --- |
| 0 | 0x01 | Показва, че първият пакет от страницата е продължение на предишния пакет в логическия битов поток. |
| 1 | 0x02 | Показва, че тази страница е първата в логическия битов поток. |
| 2 | 0x04 | Показва, че тази страница е последната в логическия битов поток. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Метаданни**: VorbisComment е най-широко поддържаният механизъм за съхранение на метаданни. Други механизми включват следното:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Препратки ##

- [OGG - Уикипедия](https://en.wikipedia.org/wiki/Ogg)

