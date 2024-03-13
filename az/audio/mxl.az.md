---
date: 2022-03-20
keywords: mxl, Musepack file format, .mxl extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: LMXL fayl formatı və MXL faylını yarada və aça bilən API-lər haqqında qazanıns.
title: MXL Fayl Format - Sıxılmış MusicXML File
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## MXL faylı nədir?

MXL faylı rəqəmsal notların mübadiləsi üçün açıq standart format olan MusicXML fayl formatının sıxılmış formasıdır. Düz mətn MusicXML fayllarının ölçüsü böyükdür və bu cür faylların vərəq paylama formatı kimi istifadəsi böyük fayl ölçüsündən təsirlənir. Bu problemlər [MusicXML](https://www.musicxml.com/) 2.0 ilə orijinal MIDI fayllarına bənzər fayl ölçüsünü azaltmaq üçün faylları kifayət qədər sıxan MXL fayl formatını təqdim etməklə həll edildi. MXL faylları üçün tövsiyə olunan media növü application/vnd.recordare.musicxml-dir.

## MXL fayl formatı

MXL faylları .mxl fayl uzantısı olan [ZIP](/compression/zip/) sıxılmış [XML](/web/xml/) fayl kimi saxlanılır. MXL faylları [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)-də göstərildiyi kimi DEFLATE alqoritmi ilə sıxılır.

### MXL Fayl Strukturu

Hər bir MXL faylı ZIP əsaslı XML formatına malikdir və bu formatda faylın MusicXML versiyasının başlanğıc nöqtəsini təsvir edən META-INF/container.xml faylı olmalıdır. MXL fayl formatı üçün müəyyən edilmiş müvafiq .xsd faylı yoxdur.

Sadə container.xml faylının məzmunu aşağıdakı kimidir. Bu nümunə MakeMusic veb saytında mövcud olan Dichterliebe01.mxl faylından götürülmüşdür.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Bu nümunədə,<container> element sənəd elementidir. The<rootfiles> element bir və ya daha çox ehtiva edə bilər<rootfile> elementləri, birincisi ilə<rootfile> MusicXML kökünü təsvir edən element. kimi istifadə olunan MusicXML faylı<rootfile> ola bilər<score-partwise> ,<score-timewise> , və ya<opus> onun sənəd elementi kimi.

## İstinadlar

* [Sıxılmış MXL Faylları](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)

* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)


