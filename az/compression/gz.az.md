{
  "date": "2019-10-11",
  "keywords": [
"gz faylı",
"gz fayl formatı",
"gz faylı nədir",
"fayl",
"gz misal",
"gz fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GZ Fayl Format - GNU Zipped Arxiv Faylı",
  "description": "GZ faylının nə olduğu və GZ faylları yarada və aça bilən API-lər haqqında öyrənin.",
  "linktitle": "GZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-g-azz"
}
},
  "lastmod": "2019-09-10"
}

## GZ faylı nədir?

GZ faylı standart [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) sıxılma alqoritmi ilə yaradılmış sıxılmış arxivdir. O, çoxlu sıxılmış faylları, qovluqları və fayl kötüklərini ehtiva edə bilər. Bu format əvvəlcə UNIX sistemlərində sıxılma formatlarını əvəz etmək üçün hazırlanmışdır. və hələ də Linux sistemlərində ən çox yayılmış arxiv növlərindən biridir. [WinZip](https://www.winzip.com/en/) kimi proqramlar həm Windows, həm də MacOS-da məzmununa baxmaq üçün GZ fayllarını aça bilər.

## GZ Fayl Format - Ətraflı Məlumat

Gzip arxivin sıxılması üçün [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) alqoritmindən istifadə edir və [ZIP](/compression/zip/) arxiv formatından sıxılma alqoritmini fərdi fayllara deyil, tam arxivə tətbiq etməklə fərqlənir. Internet Engineering Task Force (IETF) tərəfindən nəşr olunan GZIP fayl formatı spesifikasiyalarının 4.3 versiyası fayl formatı haqqında ətraflı məlumatı ehtiva edir. Fayl formatı aşağıdakılardan ibarətdir:

* Fayl başlığı

* Könüllü Başlıqlar

* Sıxılmış Məlumat

* Fayl altbilgisi


## GZ Fayl Başlığı ##

GZ fayl başlığı aşağıdakı kimi 10 baytdan ibarətdir:

|Offset|Ölçü|Dəyər|Təsvir
---|---|---|---|
|0|2|0x1f 0x8b|Fayl tipini müəyyən edən sehrli nömrə
|2|1| |Compression Method * 0-7 (Ehtiyatda) * 8 (Söndürmə)
|3|1| |Fayl Bayraqları
|4|4| |32-bit vaxt damğası
|8|1| |Sıxılma bayraqları
|9|1| |Əməliyyat sistemi ID

### Fayl Bayraqları ###

|Dəyər|İdentifikator|Təsvir
---|---|---|
|0x01|FTEXT|Qeyd edilibsə, sıxılmamış verilənlər ikili məlumat əvəzinə mətn kimi qəbul edilməlidir. Bu bayraq çarpaz platforma mətn faylları üçün sətir sonu çevrilməsinə işarə edir, lakin onu tətbiq etmir.
|0x02|FHCRC|Faylda başlıq yoxlama cəmi var (CRC-16)
|0x04|FEXTRA|Faylda əlavə sahələr var
|0x08|FNAME|Faylda orijinal fayl adı sətri var
|0x10|FCOMMENT|Faylda şərh var
|0x20| |Qorundu
|0x40| |Qorundu
|0x80| |Qorundu

### Əməliyyat sistemi ###

|Dəyər|Təsvir
---|---|
|0|FAT fayl sistemi (MS-DOS, OS/2, NT/Win32)
|1|Amiqa
|2|VMS (və ya OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|HPFS fayl sistemi (OS/2, NT)
|7|Macintosh
|8|Z-Sistem
|9|CP/M
|10|TOPS-20
|11|NTFS fayl sistemi (NT)
|12|QDOS
|13|Akorn RISCOS
|255|naməlum

## GZ Könüllü Başlıqlar ##

Əlavə başlıqlar fayl bayraqları ilə işarələnənlərdir və orijinal fayl adı, əlavə sahələr, şərhlər və başlıq yoxlama məbləği kimi məlumatları ehtiva edir.

## Sıxılmış Məlumat ##

Bu bölmə DEFLATE sıxılma alqoritmi ilə sıxılmış məlumatları ehtiva edir.

## GZ Fayl Altbilgisi ##

Fayl altbilgisinin ölçüsü 8 baytdır və aşağıdakı məlumatları ehtiva edir.

|Ofset|Ölçü|Təsvir
---|---|---|
|0|4|Yoxlama məbləği (CRC-32)
|4|4|Sıxılmamış verilənlər ölçüsünün baytlarda dəyəri

## İstinadlar ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

* [RFC1952: GZIP fayl formatının spesifikasiyası](https://datatracker.ietf.org/doc/html/rfc1952), IETF tərəfindən.


