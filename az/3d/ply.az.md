{
  "date": "2019-12-12",
  "keywords": [
"PLY",
"fayl",
"uzadılması",
"format",
"3D fayl formatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "PLY fayl formatı və PLY faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "PLY - Poliqon 3D Fayl Format",
  "linktitle": "PLY",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-pl-azy"
}
},
  "lastmod": "2019-09-10"
}

## PLY faylı nədir?

PLY, Poliqon Fayl Format, çoxbucaqlılar toplusu kimi təsvir edilən qrafik obyektləri saxlayan 3D fayl formatını təmsil edir. Bu fayl formatının məqsədi geniş çeşidli modellər üçün faydalı olmaq üçün kifayət qədər ümumi olan sadə və asan fayl tipi yaratmaq idi. PLY fayl formatı kompakt saxlama və sürətli saxlama və yükləmə üçün ASCII, eləcə də Binary format kimi gəlir. Fayl formatı 3D faylları oxumağa dəstək verən müxtəlif proqramlar tərəfindən istifadə olunur.

PLY formatında olan obyektlər bu elementlərə əlavə oluna bilən rəng və normal istiqamət kimi xassələrlə yanaşı təpələr, üzlər və digər elementlər toplusu ilə təsvir olunur. Obyektlə birlikdə saxlanıla bilən digər xüsusiyyətlərə aşağıdakılar daxildir:

* Səth normaları

* faktura koordinatları

* şəffaflıq

* diapazon məlumatlarının etibarlılığı

* poliqonun ön və arxa xüsusiyyətləri


PLY formatı ilə təmsil olunan obyekt əl ilə rəqəmsallaşdırılmış obyektlər, modelləşdirmə proqramlarından çoxbucaqlı obyektlər, diapazon məlumatları, yürüş kublarından üçbucaqlar, ərazi məlumatları və radioziyyət modelləri kimi müxtəlif mənbələrin nəticəsi ola bilər.

## Qısa tarix

PLY formatı 1990-cı illərdə Qreq Turk və başqaları tərəfindən Stanford qrafik laboratoriyasında işlənib hazırlanmışdır və buna görə də o, Stenford Üçbucaq Format kimi də tanınır. Fayl formatı o vaxtdan bəri 1.0 versiyasına malikdir və heç bir əlavə dəyişiklik edilməmişdir.

## PLY Fayl Format

Sadə PLY obyekti obyektin təsviri üçün elementlər toplusundan ibarətdir. O, təpələrin (x,y,z) üçlü siyahısından və təpələr siyahısına faktiki indeks olan üzlərin siyahısından ibarətdir. Təpələr və üzlər elementlərin iki nümunəsidir və PLY faylının əksəriyyəti bu iki elementdən ibarətdir. Yeni xassələr də yaradıla və obyektin elementlərinə əlavə oluna bilər, lakin bunlar elə əlavə edilməlidir ki, bu yeni xüsusiyyətlərlə qarşılaşdıqda köhnə proqramlar pozmasın. Bu cür xüsusiyyətlər tətbiqləri oxumaqla da ləğv edilə bilər. Bundan əlavə, yeni elementlər yaradıla bilər və bu elementlə xassələr də müəyyən edilə bilər.

### Fayl strukturu

PLY fayl formatının fayl strukturu aşağıdakı kimidir:

|Sahə
---|
|Fayl başlığı
|Vertex siyahısı
|Üzlərin siyahısı
|Digər elementlərin siyahısı

#### Nümunə Struktur

PLY fayl formatının müxtəlif hissələri üçün sonrakı müzakirəmizdə aşağıdakı nümunədən istifadə edəcəyik.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Fayl başlığı

PLY fayl formatının başlığı həm ASCII, həm də ikili format üçün ASCII mətnindən ibarətdir. Başlıq bölməsinin başlanğıcı və sonu qat və son başlıq açar sözləri ilə müəyyən edilir. Başlığın başlanğıcında PLY fayl formatının oxucular tərəfindən tanınması üçün istifadə olunan sehrli söz qatı var. Növbəti sətir bu fayl üçün versiya nömrəsini göstərir. PLY fayl formatında şərhlər hər şərh xəttinin əvvəlində şərh açar sözü ilə başlayır.

#### Element Açar Sözü

Bundan sonra element açar sözü faylın içərisində nə olduğunu bildirir. Bunun ardınca həmin xüsusi element növü üçün xassələr gəlir, burada hər bir mülkün öz mülkiyyət növü və aşağıda göstərildiyi kimi sırası var:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Bu xüsusi misalda, spesifik təpə elementi sıra ilə müəyyən edilmiş float tipli 3 xüsusiyyətə malikdir.

#### Məlumat növlərinin növləri

Mülkdə ola biləcək iki növ məlumat növü var.

`Skaler`: Skalar məlumat növləri aşağıda göstərildiyi kimidir:

|#Ad|#Növ|#Baytların Sayı
|xarakter|xarakter|1
|uchar|imzasız simvol|1
|qısa|qısa tam|2
|qısa|işarsız qısa tam|2
|int|Tam|4
|uint|işarəsiz Tam|4
|float|tək dəqiqlikli float|4
|ikiqat|ikiqat dəqiqlikli float|8

`Siyahı`: Siyahı məlumat növündən istifadə edən mülkiyyət təriflərinin xüsusi forması var. Buna misal yuxarıdakı kub faylındandır:

`əmlak siyahısı uchar int vertex_index`

Bu o deməkdir ki, vertex_index xassəsi əvvəlcə mülkiyyətin neçə indeksdən ibarət olduğunu bildirən işarəsiz simvoldan, sonra isə bu qədər tam ədəddən ibarət siyahıdan ibarətdir. Bu dəyişən uzunluqlu siyahıdakı hər bir tam ədəd təpənin indeksidir.

## İstinadlar ##

* [PLY Fayl Format](http://paulbourke.net/dataformats/ply/)

* [PLY - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/PLY_(file_format))


