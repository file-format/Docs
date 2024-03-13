{
  "date": "2021-03-08",
  "keywords": [
"RB",
"Nuvo Media-nın Rocket ebook cihazı",
"fayl",
"uzadılması",
"format",
"elektron kitab"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Nuvo Media-nın Rocket eBook cihazı və RB faylları yarada və aça bilən API-lər üçün RB fayl formatı haqqında məlumat əldə edin.",
  "title": "RB - Roket elektron kitab faylı",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-r-azb"
}
},
  "lastmod": "2021-03-08"
}

## RB faylı nədir?

The file with extension .rb holds the Rocket eBook content. The Rocket eBook is actually a device made by Nuvo Media; they released this device in 1998. Rocket eBook şəkilləri göstərməyə qadir olsa da, ancaq ağ-qara displeydə. 4,5 x 3 düymlük sensor ekranda 106 dpi və ya 480 x 320 piksel ekrana malikdir. Rocket eBook elektron kitabları RB fayl formatında yükləmək üçün serial port bağlantısı vasitəsilə kompüterə qoşulur. RB faylları DRM-dən istifadə edə bilir, lakin bu texnologiya müasir elektron kitablarda istifadə edilmir. RB faylı şərti olaraq şəkilləri olan HTML faylı və bütün metadata (.info) ilə psevdo-OPF faylını ehtiva edir.

## RB Fayl Formatının Texniki Spesifikasiyası ##

Faylın ilk 4 baytında sehrli nömrə (hex şəklində) görünür: B0 0C B0 0C.

Göründüyü kimi, növbəti iki bayt əsas versiya 2 və kiçik versiya 0 olan 02 00 kimi versiya nömrəsidir.

Növbəti dörd baytda NUVO mətni var, ardınca 4 bayt 00h.

The next 4-byte is the date when the book was created, encoded as an int16. Bu, bizi 0Eh ofsetinə qoyur. ORocketLibrary-nin köhnə versiyası ilin tam dəyərini kodlaşdırdı (yəni, 1999-cu il CF 07, 2000-ci il D0 07 idi). Son versiyada tm_year sözlə, yəni 2000-ci il üçün 100 (64 00) saxlanılır. İldən sonra 1-nisbi ay sayını təmsil edən int8 və ayın gününü təmsil edən int8 gəlir.

Növbəti 6 bayt 00 saatdır. Vaxt təyin etmək üçün bunlar rezerv edilə bilər.

Mündəricatın mütləq ofseti 18 saat ofsetdə int32-də yer alır.

Bundan sonra .rb faylının uzunluğunu ehtiva edən int32. Bu, faylların tam olub olmadığını müəyyən etmək üçün istifadə olunur.

Bu bütün bayt yığını (20 saatdan 128 saata qədər) yalnız şifrələnmiş başlığa ehtiyac duyduğu görünür. Şifrələnməmiş başlıqlarda onlar həmişə sıfırdır.

Əksər hallarda, məzmun cədvəli aşağıdakı kimidir (ofset 128-də). Bu, ToC-da səhifə daxiletmələrinin (.rb-fayl bölmələri) sayının int32 sayı ilə başlayır. Hər bir giriş bir addan (sıfırla doldurulmuş 32 bayta), ardınca 3 int32-dən ibarətdir: məlumat seqmentinin uzunluğu, .rb faylındakı mövqe və bu giriş üçün bayraq. Bu gündən məlum olan dəyərlər: 1 (şifrələnmiş), 2 (məlumat səhifəsi) və 8 (deflated). Adlar, hamısının unikal olmasını təmin etmək üçün lazım olduqda uyğunlaşdırılır.

## İstinadlar

* [E-Reader - MobileRead tərəfindən](https://en.wikipedia.org/wiki/E-reader)


