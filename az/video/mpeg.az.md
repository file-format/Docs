{
  "date": "2023-07-12",
  "keywords": [
"mpeg",
"mpeg faylı",
"mpeg faylı nədir",
"mpeg faylı necə açmaq olar",
"fayl",
"mpeg fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "MPEG Fayl Format - MPEG Video",
  "description": "MPEG faylları yarada və aça bilən MPEG formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "MPEG",
  "menu": {
    "docs": {
      "identifier": "video-mpeg-az",
      "parent": "video"
}
},
  "lastmod": "2023-07-12"
}

## MPEG faylı nədir?

MPEG video faylı kimi də tanınan MPEG faylı, video sıxılma üçün Hərəkətli Şəkil Mütəxəssisləri Qrupu (MPEG) standartlarından istifadə edən rəqəmsal video fayl formatıdır. MPEG video məlumatların saxlanması və ötürülməsi üçün geniş istifadə olunan formatdır.

MPEG formatı itkili sıxılmadan istifadə edir, yəni fayl ölçüsünü azaltmaq üçün bəzi məlumatlar silinir. Bu sıxılma texnikası ağlabatan video keyfiyyətini qoruyarkən video məzmunun səmərəli saxlanmasına və yayımlanmasına imkan verir. MPEG standartının bir neçə versiyası var, o cümlədən MPEG-1, MPEG-2, MPEG-4 və MPEG-7, hər biri müxtəlif sıxılma və keyfiyyət səviyyələrinə malikdir.

MPEG faylları adətən .mpeg və ya .mpg fayl uzantısına malikdir. Onlar tez-tez bir faylda birləşdirilən həm video, həm də audio məlumatları ehtiva edə bilər. MPEG faylları geniş çeşidli media pleyerləri və video redaktə proqramı ilə uyğun gəlir, bu da onları video məzmunu paylaşmaq və yaymaq üçün məşhur seçim edir.

## MPEG faylını necə açmaq olar?

MPEG fayllarını aça və oxuya bilən çoxsaylı proqram proqramları mövcuddur. Budur bəzi məşhur seçimlər:

- VLC Media Player
- Windows Media Player
- QuickTime Player
- MPC-HC
- GOM Oyunçusu
- MPlayer
- PotPlayer
- Kodi

## MPEG faylını necə çevirmək olar?

VideoLAN VLC media player, HandBrake və Apple QuickTime Player daxil olmaqla, MPEG fayllarını digər formatlara çevirə bilən bir sıra video proqramlar var. Məsələn, VLC MPEG fayllarını bu formatlara çevirə bilər

- MP4
- AVI
- MKV
- MOV
- WMV
- FLV

## MPEG fayllarının daxili strukturuna baxış

MPEG fayllarının daxili strukturu video, audio və digər əlaqəli məlumatları təşkil edən və saxlayan müxtəlif komponentlərdən və məlumat strukturlarından ibarətdir. MPEG fayllarının daxili strukturunun əsas elementlərinə ümumi baxış:

- **Sistem qatı:**

Sistemlər təbəqəsi MPEG faylının ümumi strukturunu müəyyən edir. Buraya başlıqlar, proqram axınları və deşifrə və oxutma üçün lazım olan digər sistemlə bağlı məlumatlar daxildir. Sistemlər təbəqəsi elementar axınların sinxronizasiyası və multipleksləşməsini idarə etmək üçün cavabdehdir.

- **İbtidai Axınlar:**

MPEG faylları video, audio və digər məlumat növləri üçün ayrıca elementar axınları ehtiva edir. Hər bir elementar axın onun növünə xas olan sıxılmış məlumatları daşıyır. Məsələn, video elementar axını sıxılmış video çərçivələri, audio elementar axını isə sıxılmış audio nümunələrini ehtiva edir.

- **Videonun sıxılması:**

Video keyfiyyətini qoruyarkən fayl ölçüsünü azaltmaq üçün çərçivədaxili və çərçivələrarası sıxılma kimi MPEG video sıxılma üsulları istifadə olunur. Sıxılmış video çərçivələr daxili kodlanmış (I), proqnozlaşdırılan (P) və iki istiqamətli (B) çərçivələrdən ibarət şəkil qruplarına (GOP) təşkil edilir.

- **Audio Sıxılma:**

MPEG faylları MP3, AAC və ya MPEG-1 Audio Layer II kimi müxtəlif audio sıxılma kodeklərini dəstəkləyir. Səs nümunələri bu kodeklərdən istifadə edərək sıxılır və səs məlumatlarının səmərəli saxlanmasına və ötürülməsinə imkan verir.

- **Sinxronizasiya və Zamanlama:**

MPEG faylları oxutma zamanı video və audio axınları arasında düzgün uyğunlaşmanı təmin etmək üçün vaxt ştamplarından və sinxronizasiya məlumatından istifadə edir. Bu vaxt ştampları sinxronizasiyanı qorumağa kömək edir və audio və video kadrların deşifrə edilməsi və göstərilməsi üçün dəqiq vaxtı təmin edir.

- **Metadata:**

MPEG fayllarına video və audio məzmun haqqında əlavə məlumat verən metadata daxil ola bilər. Bu metadata başlıq, müəllif, yaradılış tarixi və digər təsviri məlumatlar kimi təfərrüatlar ola bilər.

- **Paketlər və Paket Başlıqları:**

MPEG faylları məlumatları paketlərə təşkil edir. Hər bir paketdə axın növü, paket ölçüsü və vaxt məlumatları kimi paketin məzmunu haqqında məlumat verən paket başlığı var.

- ** Proqrama Xüsusi Məlumat (PSI):**

PSI MPEG fayllarında proqram və axın identifikatorları, axın növü və deskriptorlar kimi proqram axınları haqqında əlavə məlumatları daşıyan bölmədir. PSI fayl daxilində elementar axınların şifrəsini açmağa və demultipleks etməyə kömək edir.

- **Nəqliyyat axını:**

MPEG-2-də video məzmunun yayımı və ötürülməsi üçün istifadə olunan xüsusi nəqliyyat axını formatı mövcuddur. Nəqliyyat axını şəbəkələr üzərindən audio, video və digər məlumatların səmərəli ötürülməsinə və sinxronlaşdırılmasına imkan verən birdən çox proqramı bir axına multipleksləşdirir.

## MPEG Fayl Format - Ətraflı Məlumat

MPEG fayl formatı haqqında bilmək üçün bəzi vacib şeylər bunlardır:

- **Sıxılma:**

MPEG faylları ağlabatan video keyfiyyətini qoruyarkən fayl ölçüsünü azaltmaq üçün itkili sıxılma üsullarından istifadə edir. Sıxılma miqdarı MPEG versiyasından və istifadə edilən parametrlərdən asılı olaraq dəyişə bilər.

- **Video və Audio:**

MPEG faylları həm video, həm də audio məlumatları ehtiva edə bilər. Video məlumatları MPEG standartları ilə sıxılır, audio isə MP3 və ya AAC kimi müxtəlif audio kodeklər vasitəsilə sıxıla bilər.

- **MPEG versiyaları:**

   There are different versions of the MPEG standard, including MPEG-1, MPEG-2, MPEG-4, and MPEG-7. Each version has its own specifications, capabilities, and levels of compression. MPEG-1 is commonly used for VCDs (Video CDs), while MPEG-2 is used for DVDs and broadcast television. MPEG-4 is widely used for online video streaming, and MPEG-7 focuses on multimedia content description and metadata.

- **Fayl Uzatmaları:**

MPEG faylları adətən .mpeg və ya .mpg fayl uzantılarına malikdir. Bununla belə, MPEG-4 faylları üçün .mp4 və ya MPEG-1 Audio Layer 3 faylları üçün .mp3 kimi müxtəlif variasiyalar və genişlənmələr mövcud ola bilər.

- ** Çarpaz platforma uyğunluğu:**

MPEG faylları müxtəlif media pleyerlər, əməliyyat sistemləri və cihazlar tərəfindən geniş şəkildə dəstəklənir. Onları Windows, Mac və Linux sistemlərində, həmçinin smartfonlar, planşetlər və smart televizorlarda oynamaq olar.

- **Redaktə:**

MPEG faylları video redaktə proqramından istifadə etməklə redaktə edilə bilər. Bununla belə, MPEG itkili sıxılmadan istifadə etdiyi üçün faylın təkrar redaktə edilməsi və yenidən kodlaşdırılması keyfiyyətin aşağı düşməsinə səbəb ola bilər. Çox vaxt geniş redaktədən əvvəl itkisiz formatlarla işləmək və ya ehtiyat nüsxələri çıxarmaq tövsiyə olunur.

- **Yayım:**

MPEG faylları adətən internet üzərindən video məzmunun ötürülməsi üçün istifadə olunur. MPEG-4, xüsusilə, səmərəli sıxılma və yaxşı keyfiyyət-ölçü nisbətinə görə onlayn video platformaları və video paylaşma saytları üçün məşhurdur.

- **İnkişaf edən Standartlar:**

MPEG standartları texnoloji irəliləyişlərə uyğunlaşmaq üçün təkmilləşməyə davam edir. MPEG-4 Part 10 (həmçinin H.264 və ya AVC kimi tanınır) və MPEG-4 Part 14 (MP4) kimi daha yeni versiyalar və variasiyalar təkmilləşdirilmiş sıxılma səmərəliliyi və yüksək dəqiqlikli video və 3D məzmun kimi qabaqcıl funksiyalar üçün dəstək təklif edir.

- **Multimedia Proqramları:**

MPEG faylları müxtəlif sahələrdə, o cümlədən rəqəmsal televiziya, axın xidmətləri, video konfrans, video müşahidə, multimedia təqdimatları və s.

## MPEG və digər formatlar

MPEG fayl formatını digər video formatları ilə müqayisə edərkən, sıxılma səmərəliliyi, uyğunluq, xüsusiyyətlər və dəstək də daxil olmaqla bir neçə amil nəzərə alınır. MPEG-in bəzi məşhur video formatları ilə müqayisəsi:

### MPEG vs. AVI (Audio Video Interleave)

- **Sıxılma:**
   
MPEG faylları ümumiyyətlə AVI ilə müqayisədə daha yüksək sıxılma səmərəliliyi təklif edir, nəticədə daha kiçik fayl ölçüləri olur.

- **Uyğunluq:**

AVI faylları müxtəlif media pleyerləri tərəfindən geniş şəkildə dəstəklənir, lakin MPEG faylları cihazlar və platformalar arasında daha geniş uyğunluğa malikdir.

- **Xüsusiyyətləri:**

MPEG faylları çox vaxt çoxlu audio treklər, altyazılar və fəsillər kimi daha təkmil funksiyaları dəstəkləyir, AVI isə bu cür funksiyalar üçün məhdud dəstəyə malikdir.

- **Video keyfiyyəti:**

Sıxılma parametrlərindən asılı olaraq, MPEG və AVI oxşar video keyfiyyətinə nail ola bilər, lakin MPEG qabaqcıl sıxılma üsulları sayəsində tez-tez aşağı bit sürətlərində daha yaxşı keyfiyyət təmin edir.

### MPEG vs. WMV (Windows Media Video):

- **Sıxılma:**

WMV faylları ümumiyyətlə MPEG ilə müqayisədə daha yaxşı sıxılma səmərəliliyi təklif edir, nəticədə yaxşı video keyfiyyətini qoruyarkən fayl ölçüləri daha kiçik olur.

- **Uyğunluq:**

MPEG faylları müxtəlif cihazlar və platformalar arasında daha geniş uyğunluğa malikdir, WMV faylları isə ilk növbədə Windows əsaslı sistemlərlə əlaqələndirilir.

- **Xüsusiyyətləri:**

Hər iki format çoxsaylı audio treklər və altyazılar daxil olmaqla bir sıra funksiyaları dəstəkləyir, lakin MPEG tez-tez daha çox yönlülük və qabaqcıl funksiyalar üçün daha geniş dəstək verir.

- **Video keyfiyyəti:**

Oxşar sıxılma parametrləri ilə MPEG və WMV müqayisə edilə bilən video keyfiyyətinə nail ola bilər, lakin WMV qabaqcıl sıxılma üsulları sayəsində müəyyən ssenarilərdə daha yaxşı çıxış edə bilər.

### MPEG vs. MP4 (MPEG-4 Hissə 14):

- **Sıxılma:**

Həm MPEG, həm də MP4 oxşar sıxılma üsullarından istifadə edir və sıxılma səmərəliliyi müqayisə edilə bilər. Bununla belə, MP4 daxilində MPEG-4 Part 10 (H.264/AVC) çox vaxt köhnə MPEG formatlarından daha yaxşı sıxılma təmin edir.

- **Uyğunluq:**

Həm MPEG, həm də MP4 cihazlar və platformalar arasında geniş uyğunluğa malikdir. MP4 geniş dəstəyi və qəbulu sayəsində son illərdə əhəmiyyətli dərəcədə populyarlıq qazanmışdır.

- **Xüsusiyyətləri:**

MP4 altyazılar, fəsillər, interaktiv menyular və H.264 və HEVC (H.265) kimi təkmil video kodeklər üçün dəstək də daxil olmaqla daha təkmil funksiyalar və imkanlar təklif edir. MP4 daxilində MPEG-4 Part 2 (DivX, Xvid) də qabaqcıl funksiyaları dəstəkləyir.

- **Video keyfiyyəti:**

MPEG və MP4 müqayisə edilə bilən sıxılma parametrlərindən istifadə edərkən oxşar video keyfiyyətinə nail ola bilər. Bununla belə, MP4-ün daha təkmil video kodeklər üçün dəstəyi aşağı bit sürətlərində daha yaxşı keyfiyyət əldə etməyə imkan verir.

## İstinadlar
* [MPEG-1](https://en.wikipedia.org/wiki/MPEG-1)


