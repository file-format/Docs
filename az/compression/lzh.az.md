{
  "date": "2021-06-16",
  "keywords": [
"LZH",
"Sıxılmış",
"Fayl",
"Uzatma",
"Fayl Format",
"Lempel-Ziv",
"Haruyasu",
"LHA"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LZH fayl formatı",
  "description": "LZH faylları yarada və aça bilən LZH fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "LZH",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-azh"
}
},
  "lastmod": "2021-06-16"
}

## LZH faylı nədir? ##

A file with .lzh and .lha extension usually relates to archive compression file format. This file format is the same as other file compression formats like [ZIP](/compression/zip/), [RAR](/compression/rar/), etc. The main purpose of these file formats is to reduce the size of the format for easily sending as well as to keep them together in compressed form. AS compare to other western companies LZH files are very popular in Japan and usually used for compressing video game data. The LZH add-on for Windows 7 is built into the Japanese version of Windows 7. Microsoft ilk dəfə Windows XP-nin Yapon versiyası üçün Microsoft Sıxılmış (LZH) Qovluq Əlavəsini buraxdı. Bu fayl formatı sıxılma müddəaları və Lempel-Ziv və Haruyasu alqoritmi tərəfindən istifadə edilən xüsusiyyətlərlə həyata keçirilir.

## LZH Spesifikasiyası ##

LZH arxivinin sıxılma üsulu beş baytlıq mətn sətri kimi göstərilir, məsələn -lz1-. Bunlar sıxılmış faylda üçüncü baytdan yeddinci baytdır.

|Spesifikasiya|Təsvir|
---|---|
|Genişləndirmə | .lzh, .lha|
|Media Növü| proqram/x-lzh-sıxılmış|
|Növ kodu| LHA_ (LHA-SPACE)|
|UTI| public.archive.lha|
|Tərəfindən hazırlanıb| Haruyasu Yoshizaki (Yoshi)|
|Növü| Sıxılma|
|-dan uzadılıb| LARc|

## LZH faylını açmaqla bağlı problemlər ##

Aşağıda LZH fayl formatının zəif işləməsinə səbəb ola biləcək bir neçə problem var:
  
* Fayl zədələnmiş ola bilər. Bu problemi həll etmək üçün faylı yenidən endirin və ya göndərəndən faylı yenidən göndərməsini xahiş edin
* İkinci səbəb bu halda faylın yoluxmuş olmasıdır
* LZH faylına düzgün olmayan bağlantılar
  *	 Removal of the description of the LZH 
* Aparat resursları kifayət deyil
* Avadanlığın köhnəlmiş sürücüləri

## İstinadlar ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
