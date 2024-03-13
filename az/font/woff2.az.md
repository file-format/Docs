{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2 Faylı - Veb Açıq Font Format 2.0 Faylı",
  "description": "WOFF2 faylının nə olduğu və WOFF2 faylını yarada və aça bilən API-lər haqqında öyrənin.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-az2"
}
},
  "lastmod": "2023-01-10"
}

## WOFF2 faylı nədir?

WOFF2, Veb Açıq Font Formatının (WOFF) daha sıxılmış versiyası olan şrift faylı formatıdır. O, veb şriftlərinin fayl ölçüsünü azaltmaq, daha sürətli yükləmək və daha az bant genişliyindən istifadə etmək üçün bir yol kimi hazırlanmışdır. WOFF2 şrift məlumatlarını sıxmaq üçün Brotli adlı sıxılma alqoritmindən istifadə edir ki, bu da fayl ölçülərinin ekvivalent [WOFF](/font/woff/) şriftlərindən əhəmiyyətli dərəcədə kiçik olması ilə nəticələnə bilər. Bu format Chrome, Firefox, Safari, Opera və Edge (versiya 14-dən sonra) daxil olmaqla əksər müasir veb brauzerlər tərəfindən dəstəklənir.

## WOFF2 Fayl Format - Ətraflı Məlumat

WOFF2 şrift faylının daxili fayl strukturu başlıq, metadata, cədvəl kataloqu və şrift məlumatının özü daxil olmaqla bir neçə fərqli hissədən ibarətdir.

 1. Başlıqda faylın ümumi formatı, o cümlədən versiya nömrəsi və faylda mövcud olan cədvəllərin sayı haqqında məlumat var.

 1. Metadata bölməsində şrift adı, müəllif hüququ və digər şriftlə bağlı məlumatlar var.

 1. Cədvəl kataloqu şrifti təşkil edən müxtəlif cədvəllər, o cümlədən onların fayldakı yeri və uzunluğu haqqında məlumatları ehtiva edir.

 1. Şrift məlumatı özü bir neçə müxtəlif cədvələ bölünür, onların hər birində onun simvolları və onlara uyğun qliflər kimi şrift haqqında xüsusi məlumatlar var. Bu cədvəllərə aşağıdakılar daxil ola bilər:

 * Glyf' cədvəlində hər simvolun forması və ölçüsü daxil olmaqla, faktiki şrift konturları var.
 * Baş' cədvəlində şrift haqqında ümumi məlumat var, məsələn, onun versiya nömrəsi, dizayn ölçüsü və s.
 * hmtx' cədvəli şriftin ölçüləri, o cümlədən simvolların eni və mövqeləri haqqında məlumatları ehtiva edir.
 * Hər bir cədvəl kodlaşdırma prosesini tamamladıqdan sonra sıxılır və WOFF2 fayl formatında saxlanılır.

Bütövlükdə struktur sürətli təhlil və deşifrə imkan vermək üçün nəzərdə tutulmuşdur ki, veb-brauzerlər şrifti vebsaytda tez və səmərəli şəkildə yükləyə və göstərə bilsinlər.

### WOFF2 Başlığı
WOFF başlığı fayla daxil olan məlumatların növünü göstərən eyniləşdirici imzadan ibarətdir. WOFF başlığı sahələri ilə birlikdə aşağıdakı kimidir.

|Növ|Sahənin Adı|Təsvir|
---|---|---|
|UInt32|imza |0x774F4632 'wOF2' |
|UInt32| ləzzət |Giriş şriftinin sfnt versiyası.|
|UInt32| uzunluq |WOFF faylının ümumi ölçüsü.|
|UInt16| numTables |Şrift cədvəlləri kataloqunda yazıların sayı.|
|UInt16| qorunur | Qorunur; sıfıra təyin edin.|
|UInt32| totalSfntSize |sfnt başlığı, kataloqu və şrift cədvəlləri (doldurma daxil olmaqla) daxil olmaqla, sıxılmamış şrift məlumatı üçün lazım olan ümumi ölçü.|
|UInt32| totalCompressedSize Sıxılmış məlumat blokunun ümumi uzunluğu.|
|UInt16| majorVersion |WOFF faylının əsas versiyası.|
|UInt16| minorVersion |WOFF faylının kiçik versiyası.|
|UInt32| metaOffset |WOFF faylının əvvəlindən metadata blokuna ofset.|
|UInt32| metaLength |Sıxılmış metadata blokunun uzunluğu.|
|UInt32| metaOrigLength |Metadata blokunun sıxılmamış ölçüsü.|
|UInt32| privOffset |WOFF faylının əvvəlindən şəxsi məlumat blokuna ofset.|
|UInt32| privLength |Şəxsi məlumat blokunun uzunluğu.|


## İstinadlar
 * [w3 WOFF2 Fayl Format](https://www.w3.org/TR/WOFF2/)

