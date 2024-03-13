{
  "date": "2020-03-16",
  "keywords": [
"DWF",
"Fayl Format",
"Açıq",
"Oxuyun",
"Yaradın",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Learn about DWF file format and APIs that can create and open DWF files.",
  "title": "DWF File Format",
  "linktitle": "DWF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dwf"
}
},
  "lastmod": "2019-09-10"
}

## DWF faylı nədir?

Dizayn Veb Format (DWF) dizayn fayllarına baxmaq, nəzərdən keçirmək və ya çap etmək üçün sıxılmış formatda 2D/3D rəsmini təmsil edir. Dizayn məlumatlarının bir hissəsi kimi qrafik və mətni ehtiva edir və sıxılmış formatı səbəbindən faylın ölçüsünü azaldır. Azaldılmış fayl ölçüsü zəngin dizayn məlumatlarının yayılmasını və ünsiyyətini səmərəli edir. DWF, alıcının orijinal çertyojı yaradan CAD proqram təminatının istifadəsi haqqında bilməsini tələb etmir. DWF fayl formatının məzmunu sadə ola bilər və yalnız bir vərəq və ya şrift, rəng və şəkillərə sahib olmaq üçün kifayət qədər mürəkkəb ola bilər.

## Qısa tarix ##

Autodesk 1995-ci ildə Netscape Naviqasiya plagini WHIP-in bir hissəsi kimi DWF fayl formatını təqdim etdi. Format zaman keçdikcə 3D məzmunu daxil etmək üçün yalnız 2D formatından inkişaf etdi. Bir çox üçüncü tərəf proqramları da bu formatdan istifadə edir.

## DWF Fayl Format ##

DWF, zəngin mühəndislik dizayn məlumatlarını paylaşmaq üçün xüsusi olaraq hazırlanmış açıq, təhlükəsiz formatdır. O, həmin dizayn məlumatlarını yaratmaq üçün istifadə olunan orijinal proqram təminatı, aparat və əməliyyat sistemindən müstəqildir. Bu, CAD proqramlarından istifadə etməyən komanda üzvlərinə bina, GIS və ya məhsul dizaynlarına baxaraq rəqəmsal proseslərdə iştirak etməyə imkan verir. DWF fayl arxivi [ZIP](/compression/zip/) sıxılma ilə yaradılmış sıxılmış arxivdə birlikdə paketlənmiş bir neçə XML və ikili fayldan ibarətdir. Siz DWF fayl uzantısının adını ZIP olaraq dəyişdirə və faylın məzmununa baxa bilərsiniz. DWF paketi 2D qrafika, 3D qrafika, paket və bölmə metaməlumatları və digər resurs faylları kimi bir çox dizayn məlumatlarını ehtiva edə bilər.

**DWF metadata files** – XML files that contain information pertaining to metadata and structure (author, title, creation time, section dependencies, section ordering, resource file descriptions, roles, mimetypes, etc.) and pertaining to the section (page information, design metadata, etc.).  The structural metadata is used to create logical objects (collections of files to represent a part or page, etc.).

**Resurs faylları** – paket/bölmə metadatasından istinad edilən və adətən müxtəlif formatlarda dizayn məlumatlarının təqdimatı olan media və ya digər məzmun faylları (ZGL, W2D, [JPG](/image/jpeg/), [PNG](/image/png/), AVI, XML, [TXT](/word-processing/txt/), [DOC](/word-processing/doc/) və s.)

### Fayl Formatının Təfərrüatları ###

DWF faylları aşağıda göstərildiyi kimi üç əsas hissəyə bölünür.

* Fayl identifikasiyası başlığı

* Fayl məlumat bloku

* Faylın dayandırılması treyleri


#### Fayl İdentifikatoru Başlığı ####

The file identifier header allows for identification of DWF files by applications. It also identifies which version of DWF specifications was used for encoding the file. It is a 12 byte header that is arranged as follow:


|Bayt|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Xarakter|(|D|W|F|(boşluq)|V|0|0|.|3|0|)

Bu cədvəlin xülasəsi:

* Başlığın ilk altı baytı həmişə ASCII simvollarını təmsil edir "(DWF V"

* Aşağıdakı 5 bayt versiya nömrəsi haqqında məlumatı ehtiva edir, məsələn, formatın əsas və kiçik versiya dəyəri ilə "00.30"


DWF faylı yaradan proqramlar məlumatdan düzgün istifadə etmək üçün oxucu proqramının dəstəkləməli olduğu mümkün olan ən aşağı versiya nömrəsini göstərməlidir.

#### Fayl Məlumat Bloku ####

Fayl məlumat bloku DWF faylının 13-cü baytından başlayır və aşağıdakı cədvəldə olduğu kimi bir sıra əməliyyat kodu və operand cütlərindən ibarətdir.

|1-ci sahə|2-ci sahə|3-cü sahə|4-cü sahə|5-ci sahə|5-ci sahə|
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

DWF faylı oxunaqlı ASCII kimi əməliyyat kodu-operand cütlərini, həmçinin ikili kod və ya bunların hər ikisinin qarışığını ehtiva edə bilər. Bütün DWF əməliyyatları oxuna bilən ASCII əməliyyat kodu/operand formasına malikdir və əksər əməliyyatlar da kodlanmış ikili əməliyyat kodu/operand formasına malikdir. Əməliyyat kodları 200-dən çox əməliyyata imkan verən bir baytdadır. Genişləndirilmiş ASCII və genişləndirilmiş binar müstəsna hallardır. Əməliyyat kodlarının dəyərləri bəzi istisnalarla 0-255 arasında dəyişə bilər. Genişləndirilmiş ASCII və genişləndirilmiş binar əməliyyat kodunun iki xüsusi növü istisna olmaqla, fayl oxuyucusu operand uzunluğunu necə hesablamağı bilməlidir.

##### Qadağan edilmiş əməliyyat kodları #####

Aşağıdakılar üçün ASCII təmsilləri əməliyyat kodları kimi istifadə edilə bilməz:

Aşağıdakı ASCII təmsilləri əməliyyat kodları kimi istifadə edilə bilməz:

* Boşluq (0x20)

* Tab (0x09)

* Defis (0x2D)

* ASCII rəqəmləri 0-9 (0x30 - 0x39)

* Vaqonun qaytarılması (0x0D)

* Xətt axını (0x0A)

* Tək dırnaq işarəsi (0x27)

* İkiqat dırnaq işarəsi (0x22)

* Dövr (0x2E)

* Mötərizədə (0x28 və 0x29)

* Buruq mötərizələr (0x7B və 0x7D)

* Kvadrat mötərizələr (0x5B və 0x5D)

* Geriyə doğru kəsik (0x5C)


#### Faylın dayandırılması treyleri ####

DWF üçün faylın dayandırılması treyleri sadəcə olaraq faylın sonunu göstərən xüsusi əməliyyat kodudur. Bəzi proqramlar DWF olmayan məlumatları dayandırma əməliyyat kodundan sonra saxlaya bilər. Treyler aşağıda göstərildiyi kimidir:


|Bayt|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Xarakter|(|E|n|d|0|f|D|W|F|)

## İstinadlar ##

* [DWF - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Design_Web_Format)

* [WHIP Data Format](http://paulbourke.net/dataformats/whip/)

* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs /opc/adventures-in-packaging-episode-1)


