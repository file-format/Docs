---
date: 2019-10-11
keywords: f4v, .f4v, формат файла f4v, формат файла .f4v, расширение .f4v, расширение f4v, формат видео f4v, как открыть файлы f4v, что такое файлы f4v
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Узнайте о формате файлов F4V и API, которые могут создавать и открывать файлы F4V."
title: Формат файла F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## .F4V вариант № ##

F4V (видеофайл Flash MP4) — это видеофайл, сохраняемый с расширением .f4v. Он основан на базовом формате медиафайлов ISO (MPEG-4, часть 12). Он очень похож на [MP4](/ru/video/mp4/), поэтому его также неофициально называют Flash MP4. [FLV](/ru/video/flv/) имел ограничения при потоковой передаче содержимого H.264/ACC, в результате чего Adobe Systems создала новый формат F4V. Flash Player может воспроизводить файлы F4V с момента выпуска Flash Player 9 Update 3.

## Структура файлов F4V ##

Формат файла F4V основан на базовом формате медиафайлов ISO (MPEG-4, часть 12) и очень похож на формат MP4. Подробнее о структуре см. на странице [MP4](/ru/video/mp4/). Основное различие между F4V и MP4 заключается в форматах метаданных, которые может хранить F4V. Ниже приведен список форматов метаданных, поддерживаемых форматом F4V.

- **Поле тегов**: дополнительные четыре необязательных поля тегов (auth, title, dscp, cprt) в поле «Фильм» (moov).
- **Поле метаданных XMP**: это поле идет сразу после поля Movie (moov). При этом файл может передавать метаданные XMP в SWF-фильм через ActionScript.
- **ilst box**: это поле находится внутри поля Meta (мета) и может содержать несколько тегов метаданных. Поддерживаемые типы данных приведены ниже.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- ** Поле метаданных текстовой дорожки **: Образцы текста (текст или tx3g) внутри поля данных мультимедиа (mdat). Он может содержать следующие поля метаданных.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Использованная литература ##

- [Флэш-видео - Википедия] (https://en.wikipedia.org/wiki/Flash_Video)

