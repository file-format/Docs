---
date: 2019-12-13
keywords: ogg, формат файла ogg, расширение .ogg, аудиоформат ogg
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Узнайте о формате файла OGG и API-интерфейсах, которые могут создавать и открывать файлы OGG."
title: Файл OGG - Аудиофайл Ogg Vorbis
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## .OGG вариант №

OGG — это сжатый аудиофайл Ogg Vorbis, который сохраняется с расширением .ogg. Файлы OGG используются для хранения аудиоданных и могут также включать информацию об исполнителе и треке, а также метаданные. OGG — это бесплатный и открытый формат контейнера, поддерживаемый Xiph.Org Foundation.

## Краткая история формата файла OGG

Проект Ogg начался как часть более крупного проекта в 1993 году и был назван Squish, но из-за существующей торговой марки он был переименован в OggSquish. Он был описан как попытка создать гибкий сжатый аудиоформат для современных аудиоприложений. Ссылка OGG была отделена от Vorbis 2 сентября 2000 г.

OGM был создан в 2002 году из-за отсутствия официальной поддержки видео в OGG. Это позволило встроить видео из фреймворка Microsoft DirectShow в оболочку на основе OGG. К 2006 году OGG поддерживался многими движками видеоигр и широко использовался для кодирования бесплатного контента. 15 мая 2007 г. Фонд свободного программного обеспечения начал кампанию по расширению использования Vorbis в качестве превосходной альтернативы MP3. К 30 июня 2009 года OGG был единственным форматом контейнера, поддерживаемым реализацией HTML5 Firefox 3.5.

## Формат файла OGG

Формат OGG состоит из фрагментов данных. Каждый фрагмент называется Ogg-страницей. Каждая страница начинается с «OggS», чтобы определить формат Ogg. Заголовок содержит порядковый номер и номер страницы, которые идентифицируют каждую страницу как часть серии. Страница состоит из следующих компонентов.

- **Заголовок страницы**
  - **Capture Pattern(32 bits)**: This is used for synchronization when parsing OGG files.
  - **Version(8 bits)**: It indicates the version of the Ogg bitstream.
  - **Header Type(8 bits)**: It indicates the type of page.

| Бит | Значение | Описание |
| --- | --- | --- |
| 0 | 0x01 | Указывает, что первый пакет страницы является продолжением предыдущего пакета в логическом битовом потоке. |
| 1 | 0x02 | Указывает, что эта страница является первой в логическом битовом потоке. |
| 2 | 0x04 | Указывает, что эта страница является последней в логическом битовом потоке. |

  - **Granule position(64 bits)**: It is the time marker whose meaning is determined by the codec.
  - **Bitstream serial number(32 bits)**: It is the serial number that identifies the page belonging to a particular logical bitstream.
  - **Page sequence number(32 bits)**: It indicates the sequence of the page with the first page starting at 0.
  - **Checksum(32 bits)**: Provides the CRC32 checksum of the entire page data.
  - **Page segments(8 bits)**: Indicates the number of segments on the page.
  - **Segment table**: It is an array of 8-bit values indicating the length of each segment in the page body.
- **Метаданные**: VorbisComment — наиболее широко поддерживаемый механизм хранения метаданных. Другие механизмы включают следующее:
  - FLAC metadata blocks
  - Ogg Skeleton
  - Continuous Media Markup Language

## Использованная литература ##

- [ОГГ - Википедия](https://en.wikipedia.org/wiki/Ogg)

