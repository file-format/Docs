---
date: 2019-10-11
keywords: f4v, .f4v, формат файлу f4v, формат файлу .f4v, розширення .f4v, розширення f4v, формат відео f4v, як відкрити файли f4v, що таке файли f4v
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Дізнайтеся про формат файлу F4V та API, які можуть створювати та відкривати файли F4V"
title: Формат файлу F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Що таке файл F4V? ##

F4V (Flash MP4 Video File) — це відеофайл, збережений із розширенням .f4v. Він заснований на базовому форматі мультимедійних файлів ISO (MPEG-4, частина 12). Він дуже схожий на [MP4](/uk/video/mp4/), тому його також неофіційно називають Flash MP4. [FLV](/uk/video/flv/) мав обмеження під час потокової передачі вмісту H.264/ACC, у результаті чого Adobe Systems створила новий формат F4V. Flash Player може відтворювати файли F4V після випуску Flash Player 9 Update 3.

## Структура файлів F4V ##

Формат файлу F4V базується на базовому форматі мультимедійних файлів ISO (MPEG-4, частина 12) і дуже схожий на формат MP4. Докладніше про структуру дивіться на сторінці [MP4](/uk/video/mp4/). Основною відмінністю між F4V і MP4 є формати метаданих, які F4V може зберігати. Нижче наведено список форматів метаданих, які підтримує формат F4V.

- **Поле тегів**: чотири додаткові поля тегів (auth, title, dscp, cprt) у полі Movie (moov).
- **Поле метаданих XMP**: це поле розташовано одразу після вікна Movie (moov). Завдяки цьому файл може передавати метадані XMP у SWF-фільм через ActionScript.
- **ilst box**: це поле знаходиться всередині поля Meta (мета) і може містити кілька тегів метаданих. Нижче наведено підтримувані типи даних.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Поле метаданих текстової доріжки**: зразки тексту (text або tx3g) у полі даних Media (mdat). Він може містити такі поля метаданих.
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

## Посилання ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

