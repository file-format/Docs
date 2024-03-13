{
  "date": "2021-04-26",
  "keywords": [
"m4a",
"mp3",
"fayl",
"uzadılması",
"format",
"m4a fayl formatı nədir",
"musiqi",
"m4a fayl formatı",
"M4A vs MP3",
"m4a fayl formatının spesifikasiyası"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "M4A faylları yarada, çevirə və aça bilən M4A fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "M4A - MPEG-4 audio faylı",
  "linktitle": "M4A",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-aza"
}
},
  "lastmod": "2021-04-26"
}

## M4A faylı nədir?

**M4A fayl formatı** itkili sıxılma kimi tanınan AAC (Advanced Audio Coding) istifadə edərək yaradılmış audio fayldır. M4A sözü MPEG 4 Audio kimi qısaldılmışdır. Bu audio faylları adətən .m4a fayl uzantısına malikdir. Bu, xüsusilə qorunmayan məzmuna aiddir. O, audiokitablar, mahnılar və podkastlar kimi müxtəlif növ audio məzmunu saxlaya bilər. M4A adətən yalnız audio üçün nəzərdə tutulmayan MP3-dən daha təkmil format kimi həyata keçirilir. Bu, sadəcə MPEG 1 və ya 2 video fayllarında səs qatıdır.

M4A formatı FairPlay Digital Rights Management tərəfindən şifrlənir, çünki iTunes Store vasitəsilə .m4p genişlənməsindən istifadə edilir. Apple iPhone telefonları zəng melodiyaları üçün MPEG-4 audiodan istifadə edir, lakin bu audio faylları .m4r uzantısından istifadə edir.


## M4A vs MP3

Həm M4A, həm də [MP3](/audio/mp3/) yalnız audio fayl formatlarıdır.

**M4A**: Eyni bit sürətində kodlaşdırıldıqda keyfiyyət və ölçülər baxımından MP3-dən daha yaxşıdır. .m4a fayl uzantısı çox yaygındır, çünki onlar Apple tərəfindən iTunes Musiqi Mağazasında istifadə üçün istifadə edilmişdir. M4A MPEG-4 texnologiyası ilə sıxılmış audio fayldır; itkili sıxılma alqoritmi. O, əsasən MPEG-4 Audio Layer” ilə əlaqələndirilir, .m4a uzantısı olan fayllar MPEG-4 filmlərinin audio təbəqəsidir. O, MP3-ü ötmək və audio sıxılmada yeni standart olmaq üçün nəzərdə tutulub. Bir çox cəhətdən MP3-ə çox yaxındır, lakin eyni və ya daha kiçik fayl ölçüsündə daha yaxşı keyfiyyətə sahib olmaq üçün təqdim edilmişdir. M4A formatı ilk dəfə Apple tərəfindən təqdim edilmişdir. Format növü də Apple itkisiz kodlayıcı (ALE) kimi həyata keçirilir.

Buna görə də, hazırda M4A MP3-ün əsas uğurunu əldə edə bilmədi, çünki audio formatı hələ ümumiyyətlə oxuna bilməz. Bu, bir növ yalnız MacOS, iPod və digər Apple məhsulları ilə məhdudlaşır.

**Mp3**: Ən məşhur rəqəmsal audio formatı. Bu, həm də səhnədəki ilk sıxılma formatlarından biri idi və musiqi həvəskarları arasında çox populyarlaşdı. Onun əsas uğuru o qədər sürətlidir ki, fayl növü universal olaraq və demək olar ki, hər şeylə, aparat və ya proqram təminatı ilə ifa edilə bilir. Ümumi mənada, M4A daha yaxşı səs keyfiyyəti yaradacaq, lakin bir çoxları bunun doğru olub-olmamasından asılı olmayaraq səs fərqinin seçilə bilməyəcəyini və MP3 fayllarını M4A fayllarına çevirməyə çalışmağın vaxt itkisi olacağını iddia edərdi. Nəhayət, dönüşüm yalnız orijinal səs keyfiyyətini itirməyə səbəb olacaq.

## M4A fayl formatının spesifikasiyası

M4A faylları ardıcıl parçalardan ibarətdir. Hər bir parçanın 8 bayt başlığı var və aşağıdakı kimi alt hissələrə bölünür:
- 4 baytlıq parça ölçüsü (böyük endian, əvvəlcə yüksək bayt)
- 4 baytlıq yığın növü - əvvəlcədən müəyyən edilmiş imzalardan biri: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2 , geniş, yük, ctab, imap, mat, kmat, klip, crgn, sync, chap, tmcd, scpt , ssrc, PICT.

First chunk will be of type "ftype" and has a sub-type at offset 8. M4A_ alt növü ilə müəyyən edilmiş M4A, M4B alt növü üçün M4B_ və M4P alt növü üçün M4P_ olmalıdır.

Naməlum tipli parça aşkarlanana qədər təkrarlanan parçalar, M4A (MPEG-4 Audio) faylını təşkil edəcəkdir.

## İstinadlar ##

* [MPEG-4 Part 14 - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 Hissə 14 Audio (M4A,M4B,M4P) Format və Bərpa Nümunəsi](https://www.file-recovery.com/m4a-signature-format.htm)


