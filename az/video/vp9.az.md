{
  "date": "2021-03-12",
  "keywords": [
"VP9",
"Fayl",
"Uzatma",
"Fayl Format",
"Video Format",
"TrueMotion Video",
"VPX",
"On2 Texnologiyaları"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VP9 - TrueMotion Video Faylı",
  "description": "VP9 faylları yarada və aça bilən VP9 fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "VP9",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-az9"
}
},
  "lastmod": "2021-03-27"
}

## VP9 faylı nədir?

Google has developed the VP9 codec as a royalty-free, open-source video coding standard as the successor to VP8. O, əvvəlcə YouTube-da ultra HD məzmunu sıxışdırmaq üçün nəzərdə tutulmuşdu, çünki o, sələfinin kodlaşdırma səmərəliliyini genişləndirir və artırır. Orijinal VPX kodeklərindən danışırıqsa, onlar 2010-cu ildə Google tərəfindən mənimsənilmiş On2 Technologies-dən gəlirlər. Google daha sonra kodekləri açıq mənbə ilə təmin etdi. VP8 və VP9 formatlarının hər ikisi pulsuz BSD lisenziyası altında mövcuddur ki, bu da operatorlara həm eksklüziv proqram təminatında, həm də açıq mənbəli proqram təminatında onların mənbə kodunu açıqlamadan kodlaşdırma və ya deşifrə bacarıqlarını təşkil etməyə imkan verir.

## VP9-un Texniki Xüsusiyyətləri

* VP9, Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 və sRGB ilə 120 kadr/s-ə qədər maksimum 8192x4352 təsvir ölçüsünü və çoxlu rəng boşluqlarını təmin edir.
* 10/12-bit kodlaşdırma və HDR üçün əlavə dəstək ilə aşağı bit sürəti sıxılmadan yüksək keyfiyyətli ultra-HD-yə qədər veb və mobil istifadə hallarının tam çeşidi bu format tərəfindən tam dəstəklənir.
* O, digərləri ilə müqayisədə video bit sürətlərini 50%-ə qədər azalda bilər
* O, adaptiv axın üçün hazırlanmışdır və YouTube və digər tanınmış veb video provayderləri tərəfindən istifadə olunur
* Chrome, Opera, Edge, Firefox və Android cihazları, eləcə də milyonlarla smart televizorlar bu kodekin dekodlanmasını dəstəkləyir
* 1080p-dən böyük video qətnamələri VP9 vasitəsilə dəyişdirilir və itkisiz sıxılmaya imkan verir
* Tövsiyə kimi müxtəlif rəng boşluqları. 601, Töv. 709, Töv. 2020, SMPTE-170, SMPTE-240 və sRGB VP9 tərəfindən dəstəklənir
* Hybrid Log-Gamma və Perceptual Quantizer istifadə edən HDR video VP9 tərəfindən də dəstəklənə bilər


## Qısa tarix

 *  VP9 video kodekinin hazırlanması 2011-ci ildə başlamışdır və onun dekoderi 2012-ci ilin dekabrında Chromium veb brauzerinə əlavə edilmişdir.
 *  Onun ilk Google Chrome veb-brauzer versiyası 2013-cü ilin fevralında buraxıldı və o zaman deşifrə buraxıldı
 *  Google, 2013-cü ilin avqustunda VP9 yekun dəstəyi ilə Chrome 29.0.1547-ni buraxdı
 *  2013-cü ilin oktyabr ayında FFmpeg-ə instinktiv VP9 dekoderi əlavə edildi
 *  Mozilla 2013-cü ilin dekabrında Firefox-a VP9 əlavə etdi, sonra 18 mart 2014-cü ildə buraxılmış 2-ci versiya
 
## VP9-un işləməsi

Adətən, 4K video xüsusi pikselləri kiçik etməklə şəkil keyfiyyətini artırır, VP9 kodek və HEVC bit sürətini və fayl ölçüsünü azaltmaq üçün onları böyüdür. Bu ziddiyyətli görünsə də, kodlaşdırma mühərriki daha böyük pikselləri götürür və onları daha yaxşı ayırdetmə məhsuldarlığına çevirir. Video çərçivələri ehtiva edən mənbə video sıxılmış video bit axını yaratmaq üçün kodlaşdırılır və ya sıxılır. Hər bir ayrı çərçivə əvvəlcə piksel bloklarına bölünür. Daha sonra bloklar üçölçülü işdən çıxarılma üçün yoxlanılır və dəyişdirilə bilməyən sahələrdən faydalanmaq üçün çərçivələr arasında ardıcıl əlaqələr qiymətləndirilir. Bunlar növbəti çərçivədə verilmiş blokun keyfiyyətlərini təmin edən hərəkət vektorları vasitəsilə kodlanır. Qalıq məlumat effektiv ikili sıxılma ilə kodlanır.

## İstinadlar

 * [VP9 Vikipediya](https://en.wikipedia.org/wiki/VP9)
 * [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
 * [Kokos](https://www.coconut.co/)

