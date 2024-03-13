{
  "date": "2021-04-29",
  "keywords": [
"amr",
".amr",
"fayl",
"uzadılması",
"format",
"amr faylı nədir",
"musiqi",
"amr fayl formatı",
"amr faylı",
"amr faylını mp3-ə çevirmək",
"amr faylını çalın"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "AMR fayl formatı və AMR fayllarını yarada, çevirə və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "AMR - Adaptiv Multi-Rate Codec Faylı",
  "linktitle": "AMR",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-am-azr"
}
},
  "lastmod": "2021-04-29"
}

## AMR faylı nədir?
.amr genişləndirilməsi olan fayl **Adaptive Multi-Rate** audio kodekinə uyğun olan audio data formatıdır; 7,4 kbit/s-dən başlayan pullu nitq keyfiyyəti ilə 4,75-12,2 kbit/s bit sürətində dar zolaqlı siqnalları kodlayan çox tezlikli darzolaqlı nitq kodekindən ibarətdir; əsaslanan səkkiz fərqli bit sürətindən birini seçmək üçün keçid uyğunlaşmasından istifadə edir.

## AMR fayl formatı
AMR file format uses many coding techniques, the ACELP (Algebraic Code Excited Linear Prediction) algorithm one of the best technique; designed for compressing human spoken audio in a more efficient way. The AMR was set as the standard voice or speech codec by 3GPP in 1999. AMR fayl formatı, həmçinin bir çox ağıllı telefonlar tərəfindən qeydə alınmış nitqləri saxlamaq üçün istifadə edilən **Adaptive Multi-Rate** audio kodekindən istifadə edərək danışıq səsini saxlamaq üçün istifadə olunur.

### Fayl formatı strukturu
AMR( Adaptive Multi-Rate ) audio formatıdır; müxtəlif mobil proqramlarda və cihazlarda, adətən audio pleyerdə/yazıcıda və ya VoIP tipli proqramlarda geniş istifadə olunur. AMR daha çox təsnif edilə bilər:

1. AMR-NB (NarrowBand)
2. AMR-WB (Genişzolaqlı)

Adətən, AMR AMR-NB-yə aiddir. AMR fayl formatı aşağıdakı quruluşa malikdir:

Hər bir AMR faylında faylı AMR audio kimi tanıyan 6 baytlıq başlıq var. Bu başlıq həmişə təyin edilir:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Bu, adətən, bütün AMR-NB fayllarında oxşardır. Başlıq standarta uyğundursa, çox güman ki, fayl zədələnib və istifadə edilməməlidir. AMR faylı tam sayda audio çərçivələrdən ibarətdir. Bu kadrların hər biri 20 ms audio təşkil edir. Hər bir çərçivə etibarlı AMR-NB rejimlərindən hər hansı biri ilə kodlana bilər (DTX rejimində 0-7, 8 SID). Çərçivələr müxtəlif bit sürətlərində kodlana bildiyi üçün bu tipik metod Adaptive Multi-Rate (AMR) adlanır.
#### AMR rejimləri
Aşağıda müxtəlif AMR rejimləri və onlara uyğun bit sürətləri verilmişdir:

|REJİM| BIT MƏCƏLƏLƏR|
---|---|
|0| AMR 4.75 - 4.75kbit/s-də kodlayır|
|1 | AMR 5.15 - 5.15kbit/s-də kodlayır|
|2 | AMR 5.9 - 5.9kbit/s-də kodlayır|
|3 | AMR 6.7 - 6.7kbit/s-də kodlayır|
|4 | AMR 7.4 - 7.4kbit/s-də kodlayır|
|5 | AMR 7.95 - 7.95kbit/s-də kodlayır|
|6 | AMR 10.2 - 10.2kbit/s-də kodlayır|
|7 | AMR 12.2 - 12.2kbit/s-də kodlayır|

Baytlarda AMR rejimlərinin çərçivə ölçüsü (başlıq baytı daxil olmaqla) aşağıda verilmişdir:

|CMR |REJİM |ÇƏRÇİVƏ ÖLÇÜSÜ( baytla)|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## İstinadlar ##

* [Adaptive Multi-Rate audio codec - By Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)

* [AMR və AMR-WB Audio kodekləri üçün RTP Yükləmə Formatı və Fayl Saxlama Formatı](https://tools.ietf.org/html/rfc4867#page-35)


