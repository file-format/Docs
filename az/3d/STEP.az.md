---
date: 2019-10-11
keywords: step, .step, step file format, how to open step files, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP fayl formasıat
linktitle: STEP
description: LSTEP faylı yarada və aça bilən STEP fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## STEP faylı nədir?

STEP faylı Kompüter dəstəkli dizayn (CAD) üçün geniş istifadə olunan məlumat mübadiləsi formatıdır. 1994-cü ildə ISO komitəsi tərəfindən ISO 10303-21 adı ilə standartlaşdırılıb. ISO 10303-21 EXPRESS məlumat modelləşdirmə dilində məlumatların təqdim edilməsi üçün kodlaşdırma mexanizmini müəyyən edir. STEP faylı p21-fayl və STEP fiziki faylı kimi də tanınır. STEP faylı üçün istifadə olunan fayl uzantıları .stp və .stepdir.

## Əsas tarix

In 1994, the original Part 21 specification was issued. It has some bugs which were corrected by the technical corrigendum issued in 1996. İkinci nəşr 2002-ci ildə nəşr olundu və bir neçə məlumat bölməsi üçün korrigendum və genişləndirmələr daxil edildi. Üçüncü nəşr 2016-cı ildə nəşr olundu ki, bu da obyektlərin və dəyərlərin xarici fayllarda saxlanmasına imkan verən lövbər və istinad bölmələri əlavə etdi. UTF-8 dəstəyi sətirlərdən əlavə edildi. Faylın məzmununu yoxlamaq və etimadnamələri təsdiqləmək üçün rəqəmsal imzalar əlavə edilib. ZIP istifadə edərək mübadilə strukturunun sıxılması və saxlanması dəstəyi də əlavə edildi.

## STEP fayl formatı

The plain text format for a STEP-file consists of a sequence of records. The character set is defined as code points of ISO 10646. ISO-10303-21; ilk qeydin ilk simvollarıdır. Şərhlər /* və */ simvolları ilə əhatə olunub. Son qeyddə END-ISO-10303-21; STEP faylı 2002 versiyasına uyğundursa. 2016-cı il versiyasına uyğundursa, END-ISO-10303-21;dən sonra bir və ya daha çox rəqəmsal imza ola bilər. terminator. Sətir fasilələri \N\ və səhifə fasilələri \F\ ilə işarələnir.

STEP faylı bölmələrə bölünür və onların adları qorunan şərtlərdir. Bütün bölmələr ENDSEC qeydi ilə bitir və aşağıda göstərilən ardıcıllıqla olmalıdır.

- ** HEADER**: Bu məcburi və təkrar olunmayan bölmədir. O, aşağıdakı qurumlardan ibarətdir:
  - file_description (mandatory)
  - "fayl_adı (məcburi)"
  - "fayl_şeması (məcburi)"
  - "schema_population (isteğe bağlı)"
  - "fayl_populyasiyası (isteğe bağlı)"
  - "bölmə_dil (isteğe bağlı)"
  - "bölmə_kontekst (isteğe bağlı)"
- **ANCHOR**: Bu, 2016-cı il versiyasında təqdim edilmiş isteğe bağlı təkrar olunmayan bölmədir. Nümunələr üçün xarici adları müəyyən edir ki, onlara istinad olunsun.
- **İSTİNAD**: Bu, 2016-cı il versiyasında da təqdim edilmiş isteğe bağlı təkrar olunmayan bölmədir. Bu bölmədəki hər bir giriş giriş/dəyər nümunəsinin adını xarici fayldakı nümunə/dəyərlə əlaqələndirir.
- **MƏLUMAT**: Bu, model nümunəsinin əsas məzmununu ehtiva edən isteğe bağlı təkrarlanan bölmədir.
- **SIGNATURE**: It is an optional repeatable section that was introduced in the 2016 version. It holds the digital signature to verify the file's content or to validate credentials.

## İstinadlar

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

