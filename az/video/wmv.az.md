{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMV fayl formatı",
  "description": "WMV fayl formatı və WMV faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "WMV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-wm-azv"
}
},
  "lastmod": "2019-09-16"
}

## WMV faylı nədir?

Advanced Systems Format (ASF) əsasən media axınlarını saxlamaq və ötürmək üçün nəzərdə tutulmuş rəqəmsal multimedia konteyneridir. Microsoft Windows Media Video (WMV) sıxılmış video formatıdır və Microsoft Windows Media Audio (WMA) Microsoft tərəfindən hazırlanmış ASF konteynerindəki əlavə metadata ilə birlikdə sıxılmış audio formatıdır. WMV və ya WMA faylları Windows Media Video və Windows Media Audio kodekləri ilə kodlaşdırıldıqdan sonra onlar .asf uzantısı ilə təmsil olunurlar. WMV videonun keyfiyyətini qoruyarkən şəbəkə üzərindən daha yaxşı ötürmə sürəti üçün böyük faylları sıxır. WMV xüsusi olaraq bütün Windows cihazlarında işləmək üçün nəzərdə tutulmuşdur. Kino və Televiziya Mühəndisləri Cəmiyyəti (SMPTE) tərəfindən standartlaşdırmadan sonra WMV indi açıq standart format hesab olunur.

## Tarix ##

With the help of Microsoft proprietary codecs new compressed video format was developed in 1999 known as WMV7 which was based on MPEG-4 Part 2. Təkmilləşdirmələr daha iki versiyada, yəni WMV8 və 9-da əlavə edildi. Microsoft 2003-cü ildə standartlaşdırma üçün SMPTE-yə WMV-nin 9^^th^^ versiyasını təqdim etdi və nəticədə 2006-cı ildə VC-1 kimi tanınan SMPTE 421M kimi standartlaşdırıldı. WMV-nin arxasında duran ideya Microsoft tərəfindən dəstəklənən bütün aparat və proqram təminatı tərəfindən dəstəklənə bilən media formatı hazırlamaq idi. Bundan əlavə, başqa bir əsas məqsəd optimal ssenaridə video axınlarını internet üzərindən ötürmək idi. SMPTE-dən standartlaşdırmadan sonra WMV də Blu-ray diskləri üçün video formatına çevrildi.

## Fayl Formatının Xüsusiyyətləri

### Konteyner

Ümumiyyətlə, WMV bir ASF konteynerinə qablaşdırılır, lakin əlavə olaraq, Matroska və ya AVI konteyner də onu müvafiq olaraq .mkv və .avi genişləndirmələri ilə dəstəkləyə bilər.

### Windows Media Video 9

Windows Media Video 9 seriyasında rəqəmsal medianın yaradılması və oxunması üçün müxtəlif audio və video kodeklər mövcud olsa da, WMV-9 kodek ən yeni və ən yaxşı video kodekdir, çünki o, çox aşağı bit sürətlərindən, yəni 160 x-dən optimal sıxılma əldə edə bilir. Müxtəlif HD videolar üçün 10 Kb/s-də 120-dən 4-8 Mbit/s-də 1920 x 1080-ə qədər.

### Codec strukturu

WMV-9 8 bitlik 4:2:0 daxili rəng formatına malikdir. Bütün digər məşhur video sıxılma standartları MPEG-1 və H.261 kimi, WMV-9 blok əsaslı hərəkət kompensasiyası və məkan çevrilmə sxemindən istifadə edir. Ümumiyyətlə, deyə bilərik ki, bu standartlar hərəkət vektoru (MV) adlanan 2 ölçülü kəmiyyətin köməyi ilə əvvəlki rekonstruksiya edilmiş çərçivədən məkan yerdəyişməsini siqnal etmək üçün blok-blok hərəkət kompensasiyasını həyata keçirir. Cari blok hərəkət vektoru ilə cari mövqedən kənarlaşdırılan eyni ölçülü əvvəlki yenidən qurulmuş çərçivədən dəyərlərin proqnozlaşdırılmasının köməyi ilə formalaşır. Nəhayət, qalıq xəta hərəkətlə kompensasiya edilmiş proqnozlaşdırılan blok ilə faktiki blok arasındakı fərq kimi hesablanır. Bu qalıq xəta xətti enerji sıxlaşdıran transformasiyadan istifadə edərək çevrilir, sonra kvantlaşdırılır və entropiya kodlanır.

Quantized transform coefficients are entropy decoded, de-quantized, and inverse transformed to produce an approximation of the residual error on the decoder side, which is then added to the motion-compensated prediction to generate the reconstruction. The high-level description of the codec is shown in the following image.

Bölmənin qalan hissəsində WMV-9-da onu MPEG standartları kimi digər video kodlaşdırma həllərindən fərqləndirən yeni təkmilləşdirmələr müzakirə olunacaq. WMV-9 daxili (I), proqnozlaşdırılan (P) və iki istiqamətli proqnozlaşdırılan (B) çərçivələrə malikdir. Daxili çərçivələr müstəqil kodlaşdırılan və digər çərçivələrdən asılı olmayan çərçivələrdir. Proqnozlaşdırılan çərçivələr keçmişdə bir çərçivədən asılı olan çərçivələrdir. Proqnozlaşdırılan çərçivənin dekodlanması yalnız ən son (I) çərçivədən başlayaraq cari çərçivədən əvvəlki bütün istinad çərçivələri deşifrə edildikdən sonra baş verə bilər. B çərçivələri iki istinadı olan çərçivələrdir - biri müvəqqəti keçmişdə, digəri isə müvəqqəti gələcəkdə. B çərçivələri istinadlarından sonra ötürülür, bu o deməkdir ki, B çərçivələri onların arayışlarının deşifrə zamanı mövcud olmasını təmin etmək üçün sıradan çıxarılır. WMV-9-da B çərçivələri sonrakı kadrlar üçün istinad kimi istifadə edilmir. Bu, B çərçivələrini dekodlaşdırma dövrəsindən kənarda yerləşdirir, B çərçivələrinin dekodlanması zamanı sürüşmə və ya uzunmüddətli vizual artefaktlar olmadan qısa yolların götürülməsinə imkan verir. I, P və B çərçivələrinin yuxarıdakı tərifi həm mütərəqqi, həm də bir-birinə qarışmış ardıcıllıqlara aiddir.

Video kodeklərin performansı onların dərəcəsi-təhrif (RD) süjeti ilə müqayisə edilir. Bu, müəyyən bit sürətində sıxılma nəticəsində yaranan təhrifi göstərən 2 ölçülü əyridir.

WMV-9 bu problemi aşağıda sadalanan müxtəlif texnikaların tətbiqi ilə həll etdi:

1. Adaptiv blok ölçüsü transformasiyası

2. Məhdud dəqiqlikli transformasiya dəsti

3. Hərəkət kompensasiyası

4. Kvantlaşdırma və dekvantlaşdırma

5. Təkmil entropiya kodlaşdırması

6. Döngə filtrləmə

7. Təkmil B çərçivə kodlaşdırması

8. Interlace kodlaşdırma

9. Üst-üstə düşən hamarlama

10. Aşağı qiymətli alətlər

11. Solğun kompensasiya

## İstinadlar

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html )

* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


