---
date: 2022-03-20
keywords: mxl, формат файла Musepack, расширение .mxl
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Узнайте о формате файлов MXL и API, которые могут создавать и открывать файлы MXL."
title: Формат файла MXL — сжатый файл MusicXML
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## .MXL вариант №

Файл MXL представляет собой сжатую форму формата файла MusicXML, который является открытым стандартным форматом для обмена цифровыми нотами. Файлы MusicXML с обычным текстом имеют большой размер, и на использование таких файлов в качестве формата распространения листов повлиял большой размер файла. Эта проблема устранена в [MusicXML](https://www.musicxml.com/) 2.0 путем введения формата файлов MXL, который сжимает файлы достаточно, чтобы уменьшить размер файла, как у исходных файлов MIDI. Рекомендуемый тип носителя для файлов MXL: application/vnd.recordare.musicxml.

## Формат файла MXL

Файлы MXL хранятся в виде [ZIP](/ru/compression/zip/) сжатых файлов [XML](/ru/web/xml/) с расширением .mxl. Файлы MXL сжимаются с помощью алгоритма DEFLATE, как указано в [RFC 1951] (https://www.ietf.org/rfc/rfc1951.txt).

### Структура файла MXL

Каждый файл MXL имеет формат XML на основе ZIP, который должен иметь файл META-INF/container.xml, описывающий начальную точку версии файла MusicXML. Для формата файла MXL не существует соответствующего файла .xsd.

Простой файл container.xml имеет следующее содержимое. Этот пример взят из файла Dichterliebe01.mxl, доступного на веб-сайте MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
В этом примере<container> element — это элемент документа.<rootfiles> элемент может содержать один или несколько<rootfile> элементы, с первым<rootfile> элемент, описывающий корень MusicXML. Файл MusicXML, используемый в качестве<rootfile> можно иметь<score-partwise> ,<score-timewise> , или же<opus> как его элемент документа.

## использованная литература

* [Сжатые файлы MXL] (https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951] (https://www.ietf.org/rfc/rfc1951.txt)

