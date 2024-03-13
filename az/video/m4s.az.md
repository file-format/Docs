{
  "date": "2022-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4S Faylı - M4S faylı nədir?",
  "description": "M4S fayl formatı və M4S fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "M4S",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-azs"
}
},
  "lastmod": "2022-07-18"
}

## M4S faylı nədir?

M4S faylı **MPEG-DASH** axın texnikasından istifadə edərək internet üzərindən yayımlanan videonun kiçik bir hissəsidir. İkili məlumatlar şəklində video seqmentini ehtiva edir. Qəbul edən proqram (adətən veb-brauzer və ya media pleyerləri) bu seqmentləri alındıqları ardıcıllıqla oynayır. İlk M4S seqmenti onun ehtiva etdiyi başlatma məlumatları ilə müəyyən edilir. **xülasə** olaraq, M4S faylları tam faylın kiçik fərdi media seqmentləridir.

## M4S fayl formatı

M4S faylları [ISO Base Media File (ISOBMFF) format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)-ə əsaslanır. Böyük bir faylın bu kiçik seqmentləri HTTP vasitəsilə müstəqil olaraq endirilə bilər. Beləliklə, böyük [MP4](/video/mp4/) film faylınız varsa, onu M4S seqment faylları kimi seqmentləşdirərək MPEG-DASH (HTTP üzərindən Dinamik Adaptiv Yayım) texnikasından istifadə etməklə yayımlana bilər. Bu böyük film faylı diskə M4S olaraq endirilirsə, bir neçə M4S faylı endirilir. Bütün bu .m4s seqmentləri birləşdirilərsə, tam oxuna bilən fayl yaranır. Birinci başlatma seqmenti də faylda mövcud olmadıqda, media pleyerləri faylı oynata bilməz.

## MPEG-DASH axını haqqında

MPEG-DASH, internet üzərindən yüksək keyfiyyətli media məzmununu yayımlamağa imkan verən adaptiv bit sürəti axın texnikasından istifadə edir. Bu, məzmunu HTTP üzərindən yayımlanan kiçik seqmentlər ardıcıllığına bölmək yolu ilə həyata keçirilir. Film, podkastlar və ya idman tədbirinin canlı yayımı kimi böyük media faylları bu şəkildə yayımlana bilər. Bu seqmentlər müxtəlif bit sürətlərində kodlanır. MPEG-DASH ilə aktivləşdirilmiş media pleyerləri avtomatik olaraq bit sürətinə uyğunlaşma alqoritmindən istifadə edərək ən yüksək bit sürətinə malik seqmenti seçir. Bu, oxutmada hadisələrin dayandırılmasının və ya yenidən buferlənməsinin qarşısını alır.

### M4S faylları üçün Açıq Mənbə API

M4S fayllarını oxumaq və çevirmək üçün istifadə edilə bilən açıq mənbə API-ləri mövcuddur.

 * [libdash](https://github.com/bitmovin/libdash) - M4S faylları üçün .NET API
 * [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - M4S faylı üçün Javascript müştəri
 * [Dash Faylları yaratmaq üçün Kitabxanaya gedin](https://github.com/zencoder/go-dash)

### M4S-i MP4-ə çevirmək üçün Açıq Mənbə API

 * [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## İstinadlar ###

* [ISO Əsas Media Faylı (ISOBMFF) formatı](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)

* [HTTP üzərindən Dinamik Adaptiv Yayım - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)


