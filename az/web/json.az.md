---
date: 2019-10-11
keywords: json, .json, json file format, how to open json files, javascript object notation, json data format, .json file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON fayl formatı - JSON faylı nədire?
linktitle: JSON
description: LJSON faylı yarada və aça bilən JSON fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## JSON faylı nədir?

JSON (JavaScript Object Notation) verilənlərin saxlanması və ötürülməsi üçün insan tərəfindən oxuna bilən mətndən istifadə edən məlumat mübadiləsi üçün açıq standart fayl formatıdır. JSON faylları .json uzantısı ilə saxlanılır. JSON daha az formatlaşdırma tələb edir və [XML](/web/xml/) üçün yaxşı alternativdir. JSON JavaScript-dən əldə edilib, lakin dildən asılı olmayan məlumat formatıdır. JSON-un yaradılması və təhlili bir çox müasir proqramlaşdırma dilləri tərəfindən dəstəklənir. *application/json* JSON üçün istifadə olunan media növüdür.

## JSON Fayl Format - Qısa Tarix

There was a need for real-time server to client communication that lead to the creation of JSON. The JSON format was first specified by Douglas Crockford in March 2001. JSON JavaScript alt dəsti olan ECMA-262 3-cü Nəşr-Dekabr 1999-cu il əsasında hazırlanmışdır.

The first edition of JSON standard ECMA-404 was published in October 2013 by Ecma International. RFC 7159 became the main reference for JSON's Internet uses in 2014. 2017-ci ilin noyabr ayında ISO/IEC 21778:2017 beynəlxalq standart olaraq nəşr edilmişdir. RFC 8259 13 dekabr 2017-ci ildə İnternet Standartı STD 90-ın cari versiyası olan İnternet Mühəndisliyi İşçi Qrupu tərəfindən nəşr edilmişdir.

## JSON Fayl Strukturu

JSON məlumatları **açar/dəyər** cütlərində yazılır. Açar və dəyər ortada iki nöqtə (:) ilə ayrılır, açar solda və dəyər sağdadır. Müxtəlif açar/dəyər cütləri vergül(,) ilə ayrılır. Açar qoşa dırnaq işarələri ilə əhatə olunmuş sətirdir, məsələn, ad. Qiymətlər aşağıdakı növlərdə ola bilər.

- `Nömrə`
- `String`: Qoşa dırnaq işarələri ilə əhatə olunmuş Unicode simvollarının ardıcıllığı.
- `Boolean`: Doğru və ya Yanlış.
- `Array`: Məsələn, kvadrat mötərizələrlə əhatə olunmuş dəyərlərin siyahısı

```json
[ Alma, Banan, Portağal ]
```

- `Obyekt`: Buruq mötərizələrlə əhatə olunmuş açar/dəyər cütlərinin toplusu, məsələn

```json
{ad: Jack, yaş: 30, favoriteSport : Futbol}
```

JSON obyektləri həmçinin verilənlərin strukturunu təmsil etmək üçün yuvalana bilər. Aşağıda JSON obyektinin nümunəsi verilmişdir.

### JSON Format Nümunəsi

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## JSON faylının maksimum ölçüsü nədir?

JSON faylının maksimum ölçüsündə praktiki olaraq heç bir məhdudiyyət yoxdur. Bu, saxlanacaq məzmunun tələb etdiyi yer qədər ola bilər.

İnternet üzərindən məlumat ötürmək üçün JSON fayl formatından istifadə etməyə gəldikdə, kompüterin mövcud resurslarına diqqət yetirmək lazımdır. Böyük JSON məlumatları ötürülürsə, müştəri brauzerinin yaddaşı məhduddursa, köçürmə təsirlənəcək.


Spesifikasiya ilə müəyyən edilmiş sərt məhdudiyyət yoxdur, lakin istifadəçilərinizin kompüterlərində resursları tükəndirməmək üçün diqqətli olmalısınız, çünki bu, onların istifadəçi təcrübəsini tez bir zamanda pisləşdirəcək və onlar proqramınızı tərk edəcəklər.

## JSON və XML

**XML** internet üzərindən məlumat mübadiləsi üçün başqa bir ümumi və geniş istifadə olunan fayl formatıdır. Proqramlar arasında məlumat mübadiləsinə gəldikdə, tərtibatçıların həm XML, həm də JSON fayl formatlarından istifadə etmək imkanı var. Bununla belə, JSON aşağıdakı səbəblərə görə internet üzərindən tətbiqlər arasında məlumat mübadiləsi üçün ən əlverişli üsul kimi qəbul edilir.

 1. JSON, XML fayl formatları ilə müqayisədə məlumatların aydın və oxunması asan görünüşünü verir
 1. JSON, XML ilə müqayisədə eyni məlumat dəstini müəyyən etmək üçün daha az simvol olduğu üçün internet üzərindən məlumat ötürülməsi xərclərini azaldır.
 1. Müasir proqramlaşdırma dilləri internet üzərindən JSON cavabını təhlil etmək üçün daxili təhlilçiləri təmin edir.

## Tez-tez verilən suallar

 * **JSON faylı nə üçün istifadə olunur?** JSON fayl formatı vebsaytda təqdim edilmiş forma kimi yaradılan məlumatların saxlanması üçün aralıq fayl formatı kimi istifadə edilə bilər. O, həmçinin hər hansı proqramlaşdırma dili üçün məlumat formatı faylı kimi istifadə olunur və müxtəlif növ verilənlər arasında qarşılıqlı əlaqəni təmin edir.
 * **JSON və XML faylı eynidir?** Həqiqətən deyil. JSON XML-dən onunla fərqlənir ki, JSON daha qısadır, oxuna bilər və tez oxuna bilər, massivlərdən istifadə edə bilər və son teqdən istifadə etmir.
 * **Can I convert JSON to CSV?** Yes, there are certain online converter apps such as **GroupDocs Conversion apps** that can [convert JSON to CSV](https://products.groupdocs.app/conversion/json-to-csv).
 * **JSON-u PDF-ə Necə Çevirmək olar?** Siz [JSON faylını PDF-ə çevirmək] üçün Asopse.app for Cells kimi onlayn proqramlardan istifadə edə bilərsiniz(https://products.aspose.app/cells/conversion/json-to- pdf).
 * **JSON faylını Word-də necə açmaq olar?** JSON faylını Word-ə çevirmək üçün Aspose.app for Words kimi onlayn proqramlardan istifadə edə bilərsiniz.

## bilirdinizmi?

You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about JSON or Web file formats, you can post your findings in [Web File Format News](https://news.fileformat.com/t/Web) section for people to learn more form these.

## İstinadlar

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [An Introduction to JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

