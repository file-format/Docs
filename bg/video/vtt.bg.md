---
date: 2022-01-06
keywords: vtt, .vtt, файлов формат vtt, файлов формат .vtt, разширение .vtt, разширение vtt
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Научете за .vtt файла и API, които могат да създават и отварят VTT файлове."
title: VTT файлов формат - файл с текстови записи в уеб видео
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Какво е VTT файл?

VTT файлът е текстов файл, който съдържа информация за показване на времеви текстови записи (като субтитри или надписи) с помощта на формата Web Video Text Tracks (WebVTT). Времевите текстови записи включват информация като субтитри или надписи. Целта на VTT файла е да добави текстови наслагвания към a<video> . Форматът е донякъде подобен на SRT файловете. Базираните на WebVTT текстови файлове са кодирани с UTF-8. VTT файлът съдържа информация като субтитри, описания, надписи, описания, глави и метаданни. Тъй като са обикновени текстови файлове, VTT файловете могат да се отварят с помощта на текстови редактори като Microsoft Notepad, Apple TextEdit и Notepad++.

## VTT файлов формат - Повече информация

VTT файловете използват файловия формат WebVTT за запазване на информация за последователни текстови записи. Всяка синхронизирана текстова песен се състои от един ред или няколко реда, известни също като „подсказка“, както е показано в следващия пример.

### Пример за VTT файл

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### VTT файлова структура

Следват структурните изисквания на VTT файл.

* Незадължителна маркировка за ред на байтове (BOM).
* Низът "WEBVTT".
* Незадължително текстово заглавие вдясно от WEBVTT.
* Празен ред, който е еквивалентен на два последователни нови реда.
* Нула или повече реплики или коментари.
* Нула или повече празни редове.

## Препратки

* [VTT - W3 училища](https://www.w3.org/TR/webvtt1/)
* [WebVTT - Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)
