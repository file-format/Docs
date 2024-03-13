{
  "date": "2021-02-15",
  "keywords": [
"asf faylı",
"asf fayl formatı",
"asf faylı nədir",
"fayl",
"asf misal",
"asf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASF - Advanced Systems File Format",
  "description": "ASF fayl formatı və ASF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "ASF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-as-azf"
}
},
  "lastmod": "2021-02-16"
}

## ASF faylı nədir?

.asf uzantısı olan fayl şəbəkə üzərindən rəqəmsal media axınlarını saxlamaq və oynamaq üçün multimedia fayl formatıdır. Bu, onlayn yayım üçün həm video, həm də audio məzmuna malik ola bilən konteyner fayl formatıdır. Siz ASF fayllarına nadir hallarda rast gələcəksiniz və çox güman ki, müvafiq kodeklərlə kodlanmış məzmuna malik ASF fayllarını təyin edən Windows Media Audio ([WMA](/audio/wma/)) və Windows Media Video ([WMV](/video/wmv/)) faylları ilə rastlaşacaqsınız. Windows media faylları Windows Media Format SDK istifadə edərək yaradıla və oxuna bilər.

## ASF fayl formatı

ASF faylı çoxlu müstəqil və ya asılı axınlardan ibarət ola bilər. Buraya çoxkanallı audio və ya çoxlu bitreytli video axınları üçün çoxlu audio axını daxil ola bilər. Çoxlu bit sürətləri axınları müxtəlif bant genişlikləri üzərində ötürülməyə uyğun edir. Üstəlik, ASF faylındakı axınlar sıxılmış və ya sıxılmamış formatda ola bilər. Ən yaxşı sıxılma Microsoft Windows Media Audio və Video 9 Series kodekləri ilə əldə edilir. ASF fayl formatının tam spesifikasiyası [Microsoft Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc) saytında mövcuddur.

### ASF Yüksək Səviyyəli Fayl Strukturu

ASF faylları məntiqi olaraq üç növ yüksək səviyyəli obyektləri ehtiva edir:

* `Başlıq Obyekt` - məcburidir və hər ASF faylının əvvəlində yerləşdirilməlidir

* `Data Object` - məcburidir və başlıq obyektinə əməl etməlidir

* `İndeks Obyekt(ləri)` - isteğe bağlıdır, lakin ASF fayllarına vaxta əsaslanan təsadüfi girişi təmin etmək üçün faydalıdır


Aşağıdakı şəkil ASF fayllarının yüksək səviyyəli fayl strukturunu göstərir.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF Üst Səviyyə Başlıq Obyekti

Başlıq obyekti ASF fayllarının əvvəlində tanınmış bayt ardıcıllığını təmin edir və isteğe bağlı olaraq biblioqrafik məlumat kimi metaməlumatları ehtiva edə bilər. O, məlumat obyektindəki məlumatı düzgün şərh etmək üçün tələb olunan bütün məlumatları ehtiva edir. Başlıq Obyektinə bir neçə standart obyekt daxil ola bilər, lakin bunlarla məhdudlaşmır:

 * Fayl Xüsusiyyətləri Obyekti - Qlobal fayl atributlarını ehtiva edir.
 * Stream Properties Object - Rəqəmsal media axını və onun xüsusiyyətlərini müəyyənləşdirir.
 * Başlıq Uzatma Obyekti - Geriyə uyğunluğu qoruyarkən ASF faylına əlavə funksionallıq əlavə etməyə imkan verir.
 * Məzmun Təsviri Obyekt - Biblioqrafik məlumatları ehtiva edir.
 * Skript Əmr Obyekti - Oxutma qrafikində yerinə yetirilə bilən əmrləri ehtiva edir.
 * Marker Obyekt - Fayl daxilində adlandırılmış keçid nöqtələrini təmin edir.

Başlıq Obyekti aşağıdakı strukturdan istifadə etməklə təmsil olunur:

|Sahənin adı |Sahənin növü |Ölçü (bit)|
---|---|---|
|Obyekt ID-si| GUID| 128|
|Obyekt Ölçüsü| QWORD| 64|
|Başlıq Obyektlərinin Sayı| DWORD| 32|
|Qorundu1| BYTE| 8|
|Qorundu2| BYTE| 8|

#### ASF Yüksək Səviyyəli Məlumat Obyekti

ASF faylı üçün bütün rəqəmsal media məlumatları məlumat obyektində yerləşir və ASF məlumat paketləri şəklində saxlanılır. Hər bir məlumat paketi sabit uzunluqdadır və bir və ya bir neçə rəqəmsal media axını üçün məlumatları ehtiva edir.

#### ASF Top-Level Index Objects

ASF yüksək səviyyəli indeks obyektləri aşağıdakı iki növə malikdir:

 * `Sadə İndeks Obyekti` - ASF faylında video verilənlərin vaxta əsaslanan indeksini ehtiva edir. İndeks qeydləri arasındakı vaxt intervalı sabitdir və Sadə İndeks Obyektində saxlanılır.
 * `İndeks Obyekti` - Formatları oxşar olan İndeks Obyektinə, Media Obyekt İndeks Obyektinə və Timecode İndeks Obyektinə istinad edir. Sadə İndeks Obyekti kimi, İndeks Obyekti də sabit vaxt intervalı ilə zamana görə indekslənir, lakin video axınları ilə məhdudlaşmır.

## İstinadlar

* [ASF Fayl Format - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)

* [QuickTime Fayl Format - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)


