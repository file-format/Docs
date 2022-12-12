---
date: 2022-03-20
keywords: mxl, формат файлу Musepack, розширення .mxl
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Дізнайтеся про формат файлу MXL та API, які можуть створювати та відкривати файли MXL."
title: Формат файлу MXL – стиснутий файл MusicXML
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Що таке файл MXL?

Файл MXL — це стиснена форма файлу MusicXML, який є відкритим стандартним форматом для обміну цифровими нотами. Звичайні текстові файли MusicXML мають великий розмір, тому великий розмір файлу вплинув на використання таких файлів як формату розповсюдження аркушів. Цю проблему було вирішено за допомогою [MusicXML](https://www.musicxml.com/) 2.0 шляхом запровадження формату файлу MXL, який достатньо стискає файли, щоб зменшити розмір файлу, схожий на розмір оригінальних файлів MIDI. Рекомендований тип носія для файлів MXL – application/vnd.recordare.musicxml.

## Формат файлу MXL

Файли MXL зберігаються як [ZIP](/uk/compression/zip/) стиснені [XML](/uk/web/xml/) файли з розширенням .mxl. Файли MXL стискаються за допомогою алгоритму DEFLATE, як зазначено в [RFC 1951] (https://www.ietf.org/rfc/rfc1951.txt).

### Структура файлу MXL

Кожен файл MXL має формат XML на основі ZIP, який повинен містити файл META-INF/container.xml, який описує початкову точку версії файлу MusicXML. Для формату файлу MXL не визначено відповідного файлу .xsd.

Простий файл container.xml має наступний вміст. Цей приклад взято з файлу Dichterliebe01.mxl, доступного на веб-сайті MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
У цьому прикладі<container> element — це елемент документа. The<rootfiles> елемент може містити один або декілька<rootfile> елементів, з перш<rootfile> елемент, що описує корінь MusicXML. Файл MusicXML, який використовується як a<rootfile> може мати<score-partwise> ,<score-timewise> , або<opus> як його елемент документа.

## Список літератури

* [Стиснуті файли MXL](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

