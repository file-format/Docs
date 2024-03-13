{
  "date": "2021-06-09",
  "keywords": [
"m4p",
"mp3",
"fayl",
"uzadılması",
"format",
"m4p fayl formatı nədir",
"musiqi",
"m4p fayl formatı",
"M4b vs MP3",
"m4p fayl formatının spesifikasiyası"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "M4P faylları yarada, çevirə və aça bilən M4P fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "M4P - MPEG-4 Audiobook Fayl Format",
  "linktitle": "M4P",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-azp"
}
},
  "lastmod": "2021-06-09"
}

## M4P faylı nədir?
.m4p uzantılı fayl adətən yükləmək üçün Apple iTunes mağazasında mövcud olan audio fayldır. Başqa sözlə deyə bilərik ki, M4P bir AAC faylıdır, lakin Rəqəmsal Hüquqların İdarə Edilməsi (DRM) istifadə edərək kopyalanmadan qorunur. Bu o deməkdir ki, M4P faylları yalnız səlahiyyətli sistemlərdə və ya cihazlarda oxuna bilər. Adətən M4P faylları Apple multimedia cihazlarına xasdır. Beləliklə, bu fayllar yalnız Apple macbooks, podkastlar, iPhone 6 və ya iPhone 7 kimi ağıllı telefonlarda oxuna bilər.

## M4P fayl formatı
M4P MPEG 4 Protected (audio) deməkdir və o, audionu qabaqcıl audio kodek (AAC) ilə kodlayır və faylı icazəsiz istifadədən qoruyur. Bu fayl formatı adətən iTunes Musiqi Mağazasının audio fayl formatı kimi qəbul edilir. Apple M4P fayllarını qorumaq üçün FairPlay Digital Rights Management (DRM) sistemindən istifadə edir. FairPlay DRM Veridisc tərəfindən hazırlanmış texnologiyaya əsaslanır. Onun mühafizə mexanizmi AES şifrələməsindən istifadə edərək AAC audio axınını şifrələməklə işləyir. İstifadəçi şifrənin açılması üçün onun hesabına təyin edilmiş əsas açarı alır. Bu fayl formatı MP3 fayl formatının əvəzi kimi təqdim edilmişdir, çünki MP3 əvvəlcə audio fayl kimi deyil, MPEG 1 və ya 2 video faylında III təbəqə kimi nəzərdə tutulmuşdu.


## M4P Fayl Formatının Xüsusiyyətləri

[M4A](/audio/m4a/) kimi, M4P faylları da ardıcıl parçalardan ibarətdir. Hər bir parçanın 8 bayt başlığı var və aşağıdakı kimi alt hissələrə bölünür:
- 4 baytlıq parça ölçüsü (böyük endian, əvvəlcə yüksək bayt)
- 4 baytlıq yığın növü - əvvəlcədən müəyyən edilmiş imzalardan biri: mdat, moov, pnot, moof, udta, uuid, free, skip, ftyp, jP2 , geniş, yük, imap, mat, çap, kmat, klip, crgn, sync, tmcd, PICT, scpt , ctab, ssrc.

Similar to M4A the First chunk in M4P will be of type "ftype" and has a sub-type at offset 8. M4P M4P_ olmalıdır alt tip ilə müəyyən edilir.

Naməlum tipli parça aşkarlanana qədər təkrarlanan parçalar, M4P (MPEG-4 Audio) faylını təşkil edəcəkdir.

## İstinadlar ##

* [MPEG-4 Part 14 - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 Hissə 14 Audio (M4A,M4B,M4P) Format və Bərpa Nümunəsi](https://www.file-recovery.com/m4a-signature-format.htm)


