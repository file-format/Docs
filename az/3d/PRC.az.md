---
date: 2019-10-11
keywords: prc, .prc, prc file format, how to open prc files, .prc extension, prc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC fayl formasıat
linktitle: PRC
description: LPRC faylı yarada və aça bilən PRC fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## PRC fayl formatları
.prc uzantıları Product Representation Compact 3D fayl formatı və MobiPocket tərəfindən e-kitab fayl formatı üçün istifadə olunur.

## Product Representation Compact (PRC) faylı nədir?

PRC (Product Representation Compact) xüsusilə CAD (Kompüter Dəstəkli Dizayn) sistemlərindən gələn 3D məlumatlarını saxlamaq, yükləmək və göstərmək üçün optimallaşdırılmış 3D fayl formatıdır. Bu portativ şəkildə yazılmış ardıcıl ikili fayldır. PRC 3D məlumatı PDF faylına yerləşdirmək üçün istifadə edilə bilər. PRC CAD-in əsas konstruksiyalarının əksəriyyətini dəstəkləyir, məsələn, montajlar və hissələr, 3D obyektlərin ağacları, dəqiq həndəsə təsviri, üçbucaqlı təsvir və işarələmə. PRC .prc uzantısından istifadə edir və istifadə edilən internet media növü *model/prc*-dir.

PRC çoxməqsədli fayl formatıdır və onun istifadəsinə əsasən CAD məlumatlarını birbaşa təmsil etmək üçün müntəzəm sıxılma ilə saxlanıla bilər və ya fayl ölçüsünü azaltmaq üçün yüksək sıxılma ilə saxlanıla bilər. PRC formatından istifadə edərək PDF-də saxlanılan 3D məlumat CAM və CAE proqramları ilə qarşılıqlı fəaliyyət göstərir.

### Product Representation Compact (PRC) File Format spesifikasiyası

PRC faylında bir əsas başlıq bölməsi, sonra bir və ya daha çox fayl strukturu və sonunda bir model faylı var. Fayl strukturunda bir başlıqdan sonra aşağıdakı məlumat bölmələri var:

- **Qloballar**: O, istinad edilən fayl strukturlarını və rənglərini, xətt üslublarını və fayl strukturunun hər bir ağac obyekti üçün koordinat sistemlərini ehtiva edir.
- **Tree**: It contains a description of the tree of items like product occurrences, part definitions, representation items, and markup.
- **Tessellation**: O, ağacın yarpaq elementlərindəki bütün mozaikalı (üçbucaqlı) məlumatları ehtiva edir (təmsil elementləri və işarələmələr).
- **Həndəsə**: O, ağacın yarpaq obyektlərinin (təmsil elementləri) bütün dəqiq həndəsə və topologiya məlumatlarını ehtiva edir.
- **Əlavə həndəsə**: Bu, həndəsənin xülasə məlumatlarını ehtiva edir. Bu, bütün həndəsəni yükləmədən faylı qismən yükləməyə imkan verir.

Aşağıda tipik PRC faylının quruluşu verilmişdir.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## PRC uzantılı MobiPocket e-kitab faylı nədir
**Mobipocket** adlı fransız şirkəti tərəfindən təqdim edilən e-kitab fayl formatı da .prc uzantısından istifadə edir. Əvvəlcə Mobipocket planşetlər, PDA və smartfonlar kimi bir çox ağıllı cihazlar üçün pulsuz proqram təqdim etdi. .prc uzantısı əslində .mobi ilə eynidir, lakin xüsusilə yalnız **.prc** və ya **.pdb** genişləndirmələrini dəstəkləyən PDA-lar üçün istifadə olunur.

### Mobipocket PRC fayl formatının spesifikasiyası
MobiPocket PRC fayl formatı XHTML istifadə edərək Open eBook standartına əsaslanır və həmçinin JavaScript və çərçivələri ehtiva edə bilər. Daxili verilənlər bazaları ilə istifadə ediləcək yerli SQL sorğuları üçün dəstək də mövcuddur.

Mobipocket Reader-ın ana səhifə kitabxanası var. Oxucular kitabın istənilən hissəsinə boş səhifələr daxil edə və dəyişən təsvirlər əlavə edə bilərlər. Annotasiyalar, əlfəcinlər, düzəlişlər, qeydlər və çertyojlar kimi obyektləri bir yerdən idarə etmək olar. Şəkillər GIF formatına çevrilir və kiçik ekranlı mobil telefonlar üçün kifayət edən maksimum 64K ölçüsünə malikdir. Mobipocket Reader elektron əlfəcinlərə və daxili lüğətə malikdir.

Oxucuda bir çox PDA, Communicator və Smartfonlar üçün oxumaq və dəstəkləmək üçün tam ekran rejimi var. Mobipocket məhsulları Palm əməliyyat sistemlərinin əksəriyyətini, Windows, Symbian, BlackBerry-ni dəstəkləyir, lakin Android-i dəstəkləmir. Oxucu WINE istifadə edərək Linux və ya Mac OS X altında işləyir.

## İstinadlar

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparison of e-book formats - By Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

