{
  "date": "2021-24-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MKS fayl formatı",
  "keywords": [
"mks",
"matroska video",
"mkv formatı",
"fayl",
"format",
"video"
],
  "description": "Yalnız Matroska tərəfindən yaradılmış altyazılar üçün MKS fayl formatı və MKS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MKS",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-azs"
}
},
  "lastmod": "2021-25-02"
}

## MKS faylı nədir?

The MKS files are generally known as Matroska files containing subtitles only. Although the Matroska is a general file container, it avoids keeping the information of specific formats. Since subtitles are being used in some of the audio or video containers, Matroska is paying attention to store some common subtitle formats. It helps Matroska to be consistent with the growth rate. You need to follow the points as given below to store the subtitles in Matroska:

- .mks. genişləndirmə Matroska faylı tərəfindən istifadə ediləcək (yalnız altyazıları ehtiva edir).
- **CodecPrivate** bütün axın üçün qlobal olan bütün kodeklərlə əlaqəli məlumatları saxlamaq üçün istifadə olunur.
- Vaxt damğası yerli yaddaş formatında istifadə olunan Başlanğıc və dayandırma vaxt ştamplarını silin. Bunun əvəzinə Blokların vaxt möhürü və Müddəti istifadə edin.
- Şəffaf təbəqə ilə hər hansı bir şeydən, o cümlədən videodan istifadə edə bilərsiniz.

## Ümumi Altyazı Formatları

Here are some brief notes about more common subtitle formats stored in Matroska:

### Şəkillər Altyazılar
VobSub altyazı formatı Matroska-ya idxal edilən ilk şəkil altyazı formatıdır. Bu format DVD-dən altyazıları ixrac etməklə yaradılır. VobSub bir neçə axın dəstindən ibarətdirsə, Matroskada saxlanarkən treklər ayrılmalıdır.

### SRT Altyazılar
The SRT is the most simple and basic of all subtitle formats. It consists of four parts as given below:
 
 1. Altyazının ardıcıllığını göstərən nömrə.
 2. Altyazının ekranda görünmə və yox olma vaxtı.
 3. Altyazı özü.
 4. Növbəti alt yazının başlanğıcını göstərmək üçün boş sətir.
 
### SSA/ASS Subtitrləri
Sub Station Alpha (SSA) məşhur altyazı redaktoru SubStation Alpha tərəfindən istifadə edilən fayl formatıdır. SSA altyazıları pərəstişkarları tərəfindən geniş istifadə olunur. O, müasir funksiyaları, məsələn, karaoke, yerləşdirmə, üslub və s. göstərmək qabiliyyətinə malikdir.
 
### WebVTT Altyazılar
Ümumdünya Şəbəkə Konsorsiumu (W3C) Veb Video Mətn İzləri Format” kimi qısaldılmış WebVTT-ni işləyib hazırlayıb. Bu format HTML elementi ilə əlaqədar xarici mətn treki resurslarını qeyd etmək üçün istifadə olunur.

### HDMV təqdimat qrafikası altyazıları
HDMV təqdimat qrafikası altyazı formatı (HDMV PGS) bir sıra bitmaplardır və biz onu ümumiyyətlə mətn deyə bilmərik. Başqa sözlə, bunun sadəcə qrafik şəkillərin vaxtlı ardıcıllığı olduğunu söyləyə bilərsiniz. Məlumatı çıxarmaq üçün PGS-nin SRT-yə çevrilməsi zəruri bir prosesdir.

### HDMV mətn altyazıları
HDMV mətni Blu-ray-lərdə istifadə olunan mətn altyazı formatı kimi tanınır. Matroska yalnız TextST altyazılarını saxladıqda UTF-8 simvol dəstinə icazə verir.

### Rəqəmsal Video Yayım (DVB) altyazıları
DVB altyazı formatı televiziya siqnallarında bir neçə dildə altyazıların ötürülməsini və göstərilməsini tənzimləmək üçün təqdim edilmişdir. Tipik bir altyazı formatı, həmçinin ötürmə sistemlərinin istehsalçısından asılı olmayaraq istənilən tamaşaçıya DVB altyazılı ötürülmələrə baxmağa imkan verər.


## İstinadlar ##

- [Matroska Subtitles](https://www.matroska.org/technical/subtitles.html)

