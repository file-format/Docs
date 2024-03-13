{
  "date": "2021-02-15",
  "keywords": [
"vp6 faylı",
"vp6 fayl formatı",
"vp6 faylı nədir",
"fayl",
"vp6 nümunəsi",
"vp6 fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VP6 - TrueMotion Video Faylı",
  "description": "VP6 faylları yarada və aça bilən VP6 fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "VP6",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-az6"
}
},
  "lastmod": "2021-02-16"
}

## VP6 faylı nədir?

VP6 is a lossy compression video format that was introduced by On2 technologies in May 2003. V3, V4 və V5 daxil olmaqla TrueMotion tərəfindən hazırlanmış video kodeklər seriyasının bir hissəsidir. Bu format qısa müddət ərzində BBC hesabatları və QuickLink proqram təminatı kimi yayım sahəsində istifadə edilmişdir. VP6 daha yaxşı sıxılma uyğunluğu ilə 2005-ci ilin yanvarında VP7 Codec ilə əvəz olundu.

## VP6 Fayl Format

Complete specifications for V6 files are not available publicly. On2 made the specifications public initially but soon these were made non-available for general users. An unofficial documentation of the VP6 file format is available at [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) that can be referred for developer's reference.

### Makrobloklar (MB)

MPEG-2, MPEG-4 hissələri 2 və 10-a bənzər olaraq, VP6 faylının hər bir video çərçivəsi 16x16 makroblok (MB) massivindən ibarətdir. Hər MB aşağıdakı rejimlərdən birində ola bilər:

 * Daxili MB
 * Inter MB, null MV, əvvəlki çərçivə istinadı
 * Inter MB, diferensial MV, əvvəlki çərçivə arayışı
 * Inter MB, dörd MV, əvvəlki çərçivə arayışı
 * Inter MB, MV 1, əvvəlki çərçivə arayışı
 * Inter MB, MV 2, əvvəlki çərçivə arayışı
 * Inter MB, null MV, işarələnmiş çərçivə istinadı
 * Inter MB, diferensial MV, işarələnmiş çərçivə arayışı
 * Inter MB, MV 1, işarələnmiş çərçivə istinadı
 * Inter MB, MV 2, işarələnmiş çərçivə arayışı

### Çərçivə Başlığı

VP6-nın çərçivə başlığı, böyük-endian bit qablaşdırmasından sonra aşağıda göstərildiyi kimidir.

|Sintaksis|Bitlərin sayı|Növ|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 çərçivədaxili| bildirir
|qp |6 |İşarəsiz |Kvantlaşdırma parametri etibarlı diapazon 0..63|
|marker| 1| Daimi| 0=VP61/62, 1=VP60|
|əgər (çərçivə_rejimi == 0) { | 0 | |INTRA_FRAME|-ə bərabərdir
|versiya |5| Daimi| 6=VP60/61, 7=VP60(Elektron İncəsənət), 8=VP62|
|versiya2 |2| Sabit |0=VP60, 3=VP61/62|
|interlace |1| Boolean |true (1) interlace istifadə olunacaq deməkdir|
|əgər (marker==1 və ya versiya2==0) {||||
|ofset |16 |İmzasız| ikincil bufer ofseti (buferin başlanğıcına uyğun baytlar)|
|}||||
|dim_y |8| İmzasız| Videonun makroblok hündürlüyü|
|dim_x |8| İmzasız| Videonun makroblok eni|
|render_y |8 |İmzasız |Videonun hündürlüyünü göstərin|
|render_x |8 |İmzasız |Videonun ekran eni|
|}başqa{||||
|əgər (marker==1 və ya versiya2==0) {||||
|ofset |16 |İmzasız |İkinci bufer ofset (buferin başlanğıcına aid bayt)|
|}||||
|}||||

## İstinadlar

* [VP6 Vikipediya](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20 və%20JavaFX%20media%20files.)


