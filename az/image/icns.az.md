{
  "date": "2021-06-29",
  "keywords": [
"ICNS",
"uzadılması",
"fayl",
"format",
"şəkil",
"Apple ikonası şəkli",
"macOS",
"alma",
"İkon"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICNS - Apple Icon Image",
  "description": "ICNS fayl formatı və ICNS fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "ICNS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-icn-azs"
}
},
  "lastmod": "2021-06-29"
}

## ICNS faylı nədir? ##

MacOS proqramları tərəfindən istifadə edilən ikon formatına ICNS faylı deyilir. O, 1-bit və 8-bit alfa diapazonlarına icazə verir və adətən [PNG](/image/png/) sənədlərdən hazırlanmış bir və ya daha çox şəkli saxlayır. macOS brauzeri və interfeysindəki proqram ikonu ICNS fayllarından istifadə etməklə göstərilir.

Məkandan asılı olaraq, eyni stil ikonasında bir neçə parametr ola bilər. ICNS formatı çoxsaylı dəyişikliklərə məruz qalmış və indi müxtəlif uyğun formatlar üçün əsas kimi istifadə oluna biləcəyi nöqtəyə qədər inkişaf etmişdir. Burada bilməli olduğunuz digər vacib məqamlar var:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource və Mac OS icons Resource digər adlardan bəziləridir. 

* Simge məlumatı üçün resurs bölməsindəki mənbədən istifadə olunur.

* Əksər hallarda faylda çoxsaylı şəkillər olur. 1612 piksel kvadrat və 1024, 512, 256, 128, 48, 32 və 16 piksel kvadrat şəkil ölçüləri dəstəklənir.



## ICNS Fayl Formatı ##

ICNS məlumat formatı bir və ya daha çox təsvir üçün kapsuldur, 1-bitlik diapazonları və çoxsaylı görüntü vəziyyətini dəstəkləyir.
Əməliyyat sistemi tələb olunan displey ölçüsünə uyğun ikon şəkillərinin ölçüsünü dəyişə bilər. Daha böyük ikon şəkilləri adətən [JPEG](/image/jpeg/) 2000 və ya [PNG](/image/png/) faylları kimi saxlanılır. Həm sıxılmış, həm də sıxılmamış ICNS fayllarının bir növü mümkündür.

Başlıq və ikili nişan məlumatları ICNS faylının strukturunu təşkil edir. Başlıqda 8 bayt məlumat var, onlardan dördü sehrli hərfi, dördü isə faylın uzunluğudur. Hər bir ikon şəklinin növü və ölçüsü ikona datası bölməsində saxlanılır, ondan sonra ikili təsvir məlumatları verilir. Şəklin ölçüsü ikili hissənin ölçüsünü müəyyən edir.

## Texniki Spesifikasiya ##

### Başlıq ###

|Offset|Ölçü|Məqsəd
---|---|---|
|0|4|Sehrli hərf, icns olmalıdır (0x69, 0x63, 0x6e, 0x73)
|4|4|Faylın uzunluğu, baytla, ilk olaraq msb


### İkon datası ###

|Offset|Ölçü|Məqsəd
---|---|---|
|0|4|İkonanın növü
|4|4|Məlumatların uzunluğu, baytla (növ və uzunluq daxil olmaqla), ilk olaraq msb
|8|Dəyişən|İkon məlumatları

### Sıxılma ###

Piksel məlumatları müəyyən dərəcədə sıxılır. 32-bit (is32, il32, ih32, it32) və ARGB (ic04, ic05) piksellər çox vaxt PackBits-ə bənzər şəkildə (kanal başına) sıxılır.

|Aparıcı Dəyər|Tail Baytları|Nəticə (sıxılmamış)
---|---|---|
|0 - 127|1 - 128|1 - 128 bayt
|128 - 255|1 Bayt|3 - 130 Nüsxə

## İstinad ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)


