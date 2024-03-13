{
  "date": "2019-10-11",
  "keywords": [
"webp faylı",
"webp fayl formatı",
"webp faylı nədir",
"fayl",
"webp nümunəsi",
"webp fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WEBP - Google Raster Şəkil Fayl Formatı",
  "description": "WEBP fayl formatı və WEBP fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "WEBP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-webp"
}
},
  "lastmod": "2019-09-10"
}

## WEBP faylı nədir?

Google tərəfindən təqdim edilən WebP, itkisiz və itkili sıxılmaya əsaslanan müasir rastr veb təsvir fayl formatıdır. Şəkil ölçüsünü əhəmiyyətli dərəcədə azaldaraq eyni görüntü keyfiyyətini təmin edir. Veb səhifələrin əksəriyyəti şəkilləri məlumatların effektiv təmsili kimi istifadə etdiyi üçün veb səhifələrdə WebP şəkillərinin istifadəsi veb səhifələrin daha sürətli yüklənməsi ilə nəticələnir. Google-a görə, WebP itkisiz şəkillər [PNGs](/image/png/) ilə müqayisədə ölçü baxımından 26%, WebP itkili şəkillər isə müqayisə edilən [JPEG](/image/jpeg/) şəkillərdən 25-34% kiçikdir. Şəkillər WebP və digər şəkil fayl formatları arasında Struktur Oxşarlıq (SSIM) indeksinə əsasən müqayisə edilir. WebP [WebM](https://en.wikipedia.org/wiki/WebM) multimedia konteyner formatının bacı layihəsidir.

## WebP Xüsusiyyətlərinə Baxış ##

WebP şəkilləri ətraf bloklardan piksellərin proqnozlaşdırılması əsasında sıxılma prosesindən istifadə edir, nəticədə piksellər bir faylda bir neçə dəfə istifadə olunur. O, animasiya şəkillərini dəstəkləyir və gələcəkdə daha çox funksiyanı dəstəkləyəcəyi gözlənilir. Google, lazım olduqda istifadə etmək üçün kodlayıcı və dekoder üçün [online](https://developers.google.com/speed/webp/download) mənbə kodunu əlçatan etdi. WebP şəkli aşağıdakıları dəstəkləyir:

* **İtkili sıxılma:** İtkili sıxılma [VP8](https://en.wikipedia.org/wiki/VP8) əsas çərçivə kodlaşdırmasına əsaslanır. VP8, VP6 və VP7 formatlarının davamçısı olaraq On2 Technologies tərəfindən yaradılmış video sıxılma formatıdır.

* **İtkisiz sıxılma:** İtkisiz sıxılma formatı WebP komandası tərəfindən hazırlanmışdır.

* **Şəffaflıq:** 8-bit alfa kanalı qrafik şəkillər üçün faydalıdır. Alpha kanalı itkili RGB ilə birlikdə istifadə edilə bilər, bu xüsusiyyət hazırda hər hansı digər formatda mövcud deyil.

* **Animasiya:** O, əsl rəngli animasiya şəkillərini dəstəkləyir.

* **Metadata:** O, EXIF və XMP metadatasına malik ola bilər (məsələn, kameralar tərəfindən istifadə olunur).

* **Rəng Profili:** O, daxil edilmiş ICC profilinə malik ola bilər.


Lossy WebP sıxılma, təsviri kodlaşdırmaq üçün proqnozlaşdırıcı kodlaşdırmadan istifadə edir, eyni üsulla VP8 video kodek tərəfindən videolardakı əsas kadrları sıxışdırmaq üçün istifadə olunur. Proqnozlaşdırıcı kodlaşdırma blokdakı dəyərləri proqnozlaşdırmaq üçün qonşu piksel bloklarındakı dəyərlərdən istifadə edir və sonra yalnız fərqi kodlayır.

İtkisiz WebP sıxılma yeni pikselləri dəqiq şəkildə yenidən qurmaq üçün artıq görünən şəkil fraqmentlərindən istifadə edir. Maraqlı uyğunluq tapılmadıqda yerli palitradan da istifadə edə bilər.

## Fayl Format ##

WebP fayl formatı RIFF (resurs mübadiləsi fayl formatı) sənəd formatına əsaslanır. WebP konteyneri yalnız VP8 əsas çərçivəsi kimi kodlanmış bir təsviri ehtiva etməkdən daha çox və yuxarı funksiyalar üçün dəstək verir. RIFF faylının əsas elementi aşağıdakılardan ibarət bir parçadır:


|Sahə|Təsvir
---|---|
|Chunk FourCC: 32 bit|AscII dörd simvollu kod yığının identifikasiyası üçün istifadə olunur
|Chunk Size: 32 bits (uint32)|The size of the chunk not including this field, the chunk identifier or paddi-azng
|Yükləmə Yükü: Parça Ölçüsü baytları|Məlumat yükü. Parça Ölçüsü təkdirsə, 0 ~-~- olması lazım olan tək doldurma baytı ~-~- əlavə edilir.
|ChunkHeader ('ABCD')|Ayrı-ayrı parçaların FourCC və Parça Ölçüsü başlığını təsvir etmək üçün istifadə olunur, burada 'ABCD' yığın üçün FourCC-dir. Bu elementin ölçüsü 8 baytdır.

### WebP Başlığı ###

WebP faylının başlığı aşağıdakı kimidir:

* RIFF başlığı - 'R' 'I' 'F' 'F' ASCII simvollarını təmsil edən 32 bit

* Fayl Ölçüsü - ofset 8-dən başlayan baytlarda faylın ölçüsünü təmsil edən 32 bit (uint32). Bu sahənin maksimum dəyəri 2^32 minus 10 baytdır və beləliklə, bütün faylın ölçüsü ən çox 4GiB minus 2 baytdır. .

* 'WEBP' - 'W' 'E' 'B' 'P' ASCII simvollarını təmsil edən 32 bit


### İtkin Fayl Format ###

Şəkil itkili kodlaşdırmaya əsaslanırsa və şəffaflıq, canlı, alfa və s. kimi təkmil/genişləndirilmiş funksiyalar tələb etmirsə, WebP şəkilləri itkili fayl formatından istifadə edir. İtkili şəkillər daha kiçikdir və köhnə proqramlar tərəfindən də dəstəklənir.

Bu halda WebP faylı aşağıdakılardan ibarətdir:

* 12 bayt WebP fayl başlığı

* VP8 yığını


[VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) VP8 bit axını formatının spesifikasiyalarını göstərir.

### İtkisiz Fayl Format ###

Bu layout şəkil itkisiz kodlaşdırmaya əsaslandıqda və xarici formatın təmin etdiyi qabaqcıl funksiyalara ehtiyac olmadığı zaman istifadə olunur. Köhnə proqramlar belə faylları oxuya bilməyə bilər.

Bu halda WebP faylı aşağıdakılardan ibarətdir:

* 12 bayt WebP fayl başlığı

* VP8L yığını


## İstinadlar ##

* [WebP Tərtibatçısının Arayışı - Google tərəfindən](https://developers.google.com/speed/webp/)

* [WebP Fayl Format - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/WebP)


