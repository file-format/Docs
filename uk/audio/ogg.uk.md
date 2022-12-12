---
date: 2019-12-13
keywords: ogg, формат файлу ogg, розширення .ogg, аудіоформат ogg
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Дізнайтеся про формат файлу OGG та API, які можуть створювати та відкривати файли OGG."
title: Файл OGG - аудіофайл Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Що таке файл OGG?

OGG — це стиснутий аудіофайл Ogg Vorbis, який зберігається з розширенням .ogg. Файли OGG використовуються для зберігання аудіоданих і можуть містити інформацію про виконавця та композицію, а також метадані. OGG — це вільний і відкритий контейнерний формат, який підтримує Xiph.Org Foundation.

## Коротка історія формату файлів OGG

Проект Ogg розпочався як частина більшого проекту в 1993 році та отримав назву Squish, але через існуючу торгову марку його було перейменовано на OggSquish. Це було описано як спроба створити гнучкий формат стисненого аудіо для сучасних аудіододатків. Посилання OGG було відокремлено від Vorbis 2 вересня 2000 року.

OGM було створено в 2002 році через відсутність офіційної підтримки відео в OGG. Це дозволило вбудовувати відео з інфраструктури Microsoft DirectShow в оболонку на основі OGG. До 2006 року OGG підтримувався багатьма движками відеоігор і широко використовувався для кодування безкоштовного вмісту. Фонд вільного програмного забезпечення розпочав кампанію 15 травня 2007 року, щоб збільшити використання Vorbis як кращої альтернативи MP3. До 30 червня 2009 року OGG був єдиним форматом контейнера, який підтримувався версією HTML5 у Firefox 3.5.

## Формат файлу OGG

Формат OGG складається з фрагментів даних. Кожна частина називається сторінкою Ogg. Кожна сторінка починається з "OggS", щоб визначити формат Ogg. Верхній колонтитул містить порядковий номер і номер сторінки, які ідентифікують кожну сторінку як частину серії. Сторінка складається з наступних компонентів.

- **Заголовок сторінки**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Біт | Значення | Опис |
| --- | --- | --- |
| 0 | 0x01 | Вказує, що перший пакет сторінки є продовженням попереднього пакету в логічному бітовому потоці. |
| 1 | 0x02 | Вказує, що ця сторінка є першою в логічному бітовому потоці. |
| 2 | 0x04 | Вказує, що ця сторінка є останньою в логічному бітовому потоці. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Метадані**: VorbisComment є найбільш широко підтримуваним механізмом для зберігання метаданих. Серед інших механізмів:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Посилання ##

– [OGG – Вікіпедія](https://en.wikipedia.org/wiki/Ogg)

