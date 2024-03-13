{
  "date": "2021-06-09",
  "keywords": [
"m4b",
"mp3",
"fayl",
"uzadılması",
"format",
"m4b fayl formatı nədir",
"musiqi",
"m4b fayl formatı",
"M4b vs MP3",
"m4b fayl formatının spesifikasiyası"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "M4B fayl formatı və M4B fayllarını yarada, çevirə və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "M4B - MPEG-4 Audiobook Fayl Format",
  "linktitle": "M4B",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-azb"
}
},
  "lastmod": "2021-06-09"
}

## M4B faylı nədir?

.m4b uzantılı fayl ümumiyyətlə Apple kitabları və iTunes tərəfindən istifadə edilən audiokitabdır. Bu formatda istifadə edilən Audio MPEG-4-də saxlanılır və AAC kodlaşdırmasından istifadə etməklə sıxılır. M4B faylı M4A faylına çox bənzəyir, lakin əlfəcinlər və fəsil fasilələri kimi audiokitabla bağlı funksiyaları dəstəkləyir. M4B faylları həm DRM effektiv, həm də DRM pulsuz versiyalarında mövcuddur. DRM ilə şifrələnmiş audiokitablar adətən iTunes Store-dan ödənişli audiokitablardır. Halbuki, DRM pulsuz internet üzərindən asanlıqla tapıla bilər.

## M4B fayl formatı

Metadata, şəkillər, əlfəcinlər və hiperlinkləri ehtiva edən audiokitab faylları .m4a genişləndirilməsi ilə yadda saxlanıla bilər, lakin yadda saxlama zamanı ümumiyyətlə .m4b genişləndirilməsi faylın audiokitab fayl formatına malik olduğunu müəyyən etmək üçün istifadə olunur. Fairplay DRM (Rəqəmsal Hüquqların İdarə Edilməsi) tətbiq tərəfindən M4B fayllarını qorumaq üçün istifadə olunur. Beləliklə, iTunes-dan yüklənmiş fayllar yalnız səlahiyyətli cihazlarda və ya kompüterlərdə oxuna bilər.


## M4B və M4A

Həm M4B, həm də [MP3](/audio/mp3/) yalnız audio fayl formatlarıdır.

**M4B**: Hər ikisini eyni bit sürətində kodlasanız, keyfiyyət baxımından MP3 ilə müqayisədə qalib gəlir. M4B AAC kodlaşdırması ilə sıxılmış audiokitab faylıdır. O, əsasən MPEG-4 Audio Layer” ilə əlaqələndirilir, .m4b uzantısı olan fayllar MPEG-4 filmlərinin audio qatıdır, lakin əlavə audiokitabla əlaqəli xüsusiyyətlərə malikdir. Onun məqsədi MP3-ü ötmək və audio sıxılmada yeni standart olmaqdır. Bir çox cəhətdən MP3-ə çox yaxındır, lakin eyni və ya daha kiçik fayl ölçüsündə daha yaxşı keyfiyyətə sahib olmaq üçün hazırlanmışdır. M4B formatı ilk dəfə Apple tərəfindən təqdim edilmişdir. Format növü də Apple itkisiz kodlayıcı (ALE) kimi həyata keçirilir.

Buna görə də, hazırda M4B MP3-ün əsas uğurunu əldə edə bilmədi, çünki audio formatı hələ çox oxuna bilməz.

**Mp3**: Hər kəsə yaxşı tanış olan rəqəmsal audio formatı. Səhnədə çox ilk sıxılma formatı və musiqi dinləyiciləri arasında çox məşhur oldu. Onun əsas uğuru o qədər sürətlidir ki, fayl növü universal olaraq ifa edilə bilir və demək olar ki, hər şey, aparat və ya proqram təminatı ilə uyğun gəlir. Ümumi mənada, M4A daha yaxşı səs keyfiyyəti yaradacaq, lakin bir çoxları bunun doğru olub-olmamasından asılı olmayaraq səs fərqinin müqayisə edilə bilməyəcəyini və MP3 fayllarını M4A fayllarına çevirməyə çalışmağın vaxt itkisi olacağını iddia edərdi. Nəhayət, dönüşüm yalnız orijinal səs keyfiyyətini itirməyə səbəb olacaq.

## M4B fayl formatının spesifikasiyası

[M4A](/audio/m4a/) kimi, M4B faylları da ardıcıl parçalardan ibarətdir. Hər bir parçanın 8 bayt başlığı var və aşağıdakı kimi alt hissələrə bölünür:
- 4 baytlıq parça ölçüsü (böyük endian, əvvəlcə yüksək bayt)
- 4 baytlıq yığın növü - əvvəlcədən müəyyən edilmiş imzalardan biri: ftyp, mdat, moov, pnot, moof, udta, uuid, free, ctab, skip, jP2, geniş, yük, imap, mat, çap, kmat, klip, crgn, sinx, tmcd, PICT , scpt, ssrc.

Similar to M4A the First chunk in M4B will be of type "ftype" and has a sub-type at offset 8. M4B M4B_ olmalıdır alt tip ilə müəyyən edilir.

Naməlum tipli parça aşkarlanana qədər təkrarlanan parçalar, M4B (MPEG-4 Audio) faylını təşkil edəcəkdir.

## İstinadlar

* [MPEG-4 Part 14 - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 Hissə 14 Audio (M4A,M4B,M4P) Format və Bərpa Nümunəsi](https://www.file-recovery.com/m4a-signature-format.htm)


