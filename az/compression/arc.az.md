---
date: 2019-12-09
keywords: arc, .arc, arc file format, how to open arc files, .arc extension, arc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC fayl formasıat
linktitle: ARC
description: LARC fayl formatı və ARC faylı yarada və aça bilən API-lər haqqında qazanıns.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## ARC faylı nədir?

ARC, System Enhancement Associates (SEA) tərəfindən hazırlanmış itkisiz məlumat sıxılma və arxiv formatıdır. Fayl formatı və onu yaradan proqram ARC adlanır. ARC dial-up BBS-nin ilk günlərində çox populyar idi, çünki o, sıxılma və eyni faylda birdən çox faylın arxivləşdirilməsi xüsusiyyətlərini birləşdirdi. ARC daha sonra daha yaxşı sıxılma nisbətləri təklif edən [ZIP](/compression/zip/) ilə əvəz olundu.

.arc fayl uzantısı bir neçə digər əlaqəli olmayan arxiv fayl növləri tərəfindən istifadə olunur, məsələn, İnternet Arxivi tərəfindən çoxsaylı veb-resursları saxlamaq üçün istifadə olunan ARC formatı, FreeArc arxivatoru tərəfindən istifadə edilən fərqli ARC formatı, Nintendo tərəfindən resurslar üçün istifadə olunan fərqli format və s. .

## ARC Fayl Formatının Qısa Tarixi

The ARC program was written by Thom Henderson of System Enhancement Associates in 1985. Bu proqram faylları bir arxiv faylında qruplaşdırdı və həmçinin onları sıxışdırdı. ARC proqramı tərəfindən yaradılan fayllar .arc uzantısından istifadə edirdi. SEA 1986-cı ildə ARC üçün mənbə kodunu buraxdı və ARC 1987-ci ildə Howard Chu tərəfindən Unix və Atari ST-yə köçürüldü.

Phil Katz faylların arxivləşdirilməsi və çıxarılması üçün PKARC və PKXARC-ni inkişaf etdirdi. Fayllar ARC fayl formatı ilə işləyirdi və əhəmiyyətli dərəcədə sürətli idi. ARC-dən fərqli olaraq, Katz sıxılma və arxivləşdirmə funksiyalarını iki müxtəlif fayl arasında böldü ki, bu da onların işləməsi üçün yaddaş tələbini azaltdı.

SEA və Katz arasındakı məhkəmə çəkişməsindən sonra SEA paylaşılan proqram bazarından çıxdı və tam ekran istifadəçi interfeysi ilə ARC+Plus inkişaf etdirdi. ARC formatı artıq PC-də ümumi deyil.

## ARC fayl formasıat

ARC faylı aşağıda göstərildiyi kimi fayl başlığı və fayl ardıcıllığından və sonra arxivin sonu markerindən ibarətdir.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### ARC Fayl Başlığı ###

|Offset|Etiket|Növ|Dəyər|Təsvir|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metod|
|02|ARCFNT|DS|12|fayl adı|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Sıxılmış ölçü|
|13|ARCDAT|DW|0000|Fayl tarixi (MSDOS)|
|15|ARCTIM|DW|0000|Fayl vaxtı (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Sıxılmamış ölçü|
|1D|ARCFIL|DS|ARCNSZ| |

### Sıxılma Metodları ###

Sıxılma üsulu baytı istifadə olunan sıxılma üsulunu göstərir. Aşağıda ARC faylı üçün istifadə olunan sıxılma üsulları verilmişdir.

|Metod|Ad|Təsvir|
|---|---|---|
|0|Saxlanılır|Sıxılma istifadə olunmur|
|1|Paketli|Təkrarlanan iş uzunluğu kodlaması (RLE)|
|2|Sıxılmış|Huffman kodlaması|
|3|Crunched|4K buferli LZW, 12 bit kodlar|
|4|Crunched|İlk qablaşdırma, sonra 12 bitli LZW 4K bufer|
|5|Crunched|Qablaşdırma, LZW, 4K bufer, dəyişən uzunluq (9-12 bit)|
|6|Əzilmiş|LZW, 8K bufer, dəyişən uzunluq (9-13 bit)|
|7|Əzilmiş|Qablaşdırma, sonra LZW 8K bufer, 2-13 bit (PAK 1.0)|
|8|Distill|8K buferli Dinamik Huffman (PAK 2.0)|

## İstinadlar

- [ARC (file format) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

