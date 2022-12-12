---
date: 2022-03-20
keywords: mxl, файлов формат Musepack, разширение .mxl
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Научете за файловия формат MXL и API, които могат да създават и отварят MXL файлове."
title: MXL файлов формат - Компресиран MusicXML файл
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Какво е MXL файл?

MXL файлът е компресираната форма на файловия формат MusicXML, който е отворен стандартен формат за обмен на цифрови ноти. MusicXML файловете с обикновен текст са големи по размер и използването на такива файлове като формат за разпространение на листа беше засегнато от големия размер на файла. Този проблем беше третиран с [MusicXML](https://www.musicxml.com/) 2.0 чрез въвеждане на файлов формат MXL, който компресира файловете достатъчно, за да намали размера на файла, подобен на този на оригиналните MIDI файлове. Препоръчителният тип медия за MXL файлове е application/vnd.recordare.musicxml.

## MXL файлов формат

MXL файловете се съхраняват като [ZIP](/bg/compression/zip/) компресирани [XML](/bg/web/xml/) файлове с файлово разширение .mxl. MXL файловете се компресират с алгоритъма DEFLATE, както е посочено в [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### MXL файлова структура

Всеки MXL файл има базиран на ZIP XML формат, който трябва да има META-INF/container.xml файл, който описва началната точка на MusicXML версията на файла. Няма съответен .xsd файл, дефиниран за файловия формат MXL.

Прост файл container.xml има следното съдържание. Този пример е взет от файла Dichterliebe01.mxl, достъпен на уеб сайта на MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
В този пример,<container> елемент е елементът документ. The<rootfiles> елемент може да съдържа един или повече<rootfile> елементи, с първ<rootfile> елемент, описващ корена на MusicXML. MusicXML файл, използван като a<rootfile> Може да се наложи<score-partwise> ,<score-timewise> , или<opus> като негов документен елемент.

## Препратки

* [Компресирани MXL файлове](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

