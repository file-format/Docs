---
date: 2019-10-11
keywords: f4v, .f4v, файлов формат f4v, файлов формат .f4v, разширение .f4v, разширение f4v, видео формат f4v, как да отваряте файлове f4v, какво представляват файловете f4v
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Научете за файловия формат F4V и API, които могат да създават и отварят F4V файлове"
title: F4V файлов формат
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Какво е F4V файл? ##

F4V (Flash MP4 Video File) е видео файл, записан с разширение .f4v. Базиран е на ISO базовия медиен файлов формат (MPEG-4 част 12). Той е много подобен на [MP4](/bg/video/mp4/), поради което неофициално се нарича също Flash MP4. [FLV](/bg/video/flv/) имаше ограничения при поточно предаване на H.264/ACC съдържание, което доведе до създаването на новия формат F4V от Adobe Systems. Flash Player може да възпроизвежда F4V файлове след пускането на Flash Player 9 Update 3.

## Структура на F4V файлове ##

Файловият формат F4V се основава на основния формат на мултимедиен файл ISO (MPEG-4 част 12) и е много подобен на формата MP4. За подробности относно структурата, моля, вижте страницата [MP4](/bg/video/mp4/). Основната разлика между F4V и MP4 са форматите на метаданни, които F4V може да съхранява. По-долу е даден списък на форматите на метаданни, поддържани от формата F4V.

- **Кутия за етикети**: Допълнителни четири незадължителни полета за етикети (auth, title, dscp, cprt) в полето Movie (moov).
- **Кутия с метаданни XMP**: Това поле идва веднага след полето Филм (moov). С това файлът може да комуникира XMP метаданни към SWF филм чрез ActionScript.
- **ilst box**: Това поле се намира в полето Meta (мета) и може да съдържа редица маркери за метаданни. Поддържаните типове данни са дадени по-долу.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Кутия с метаданни за текстова песен**: Примерите на текст (текст или tx3g) в кутията с медийни данни (mdat). Може да съдържа следните полета с метаданни.
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

## Препратки ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

