{
  "date": "2022-05-06",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FIT Fayl Format - Garmin Fəaliyyət Faylı",
  "description": "FIT fayl formatı və FIT fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "FIT",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-fi-azt"
}
},
  "lastmod": "2022-05-06"
}

## FIT faylı nədir?

FIT faylı Garmin idman geyilə bilən cihazları tərəfindən yaradılmış GIS faylıdır. Bu cihazları taxaraq hərəkət edən şəxsin fəaliyyətini qeyd etmək üçün istifadə olunur. Fəaliyyət datasına GPS cihazı tərəfindən qeydə alınan yer və vaxt daxildir. FIT faylları həmçinin veb API-lərdən istifadə edərək qeydə alınmış fəaliyyət məlumatlarını ötürmək üçün istifadə olunur. Buna görə də FIT faylları fitness məlumatlarını digər fitness platformaları ilə paylaşmaq üçün ən çox istifadə olunan fayl formatıdır. Digər ümumi fayl formatlarına [GPX](/gis/gpx/), TCX və [KML](/gis/kml/) daxildir.

## FIT Fayl Format - Ətraflı Məlumat

FIT faylları fəaliyyət üçün Garmin cihazları tərəfindən qeydə alınan məlumatla ikili fayllar kimi diskdə saxlanılır. FIT faylında saxlanılan məlumatlara aşağıdakılar daxildir:

 * Tarix vaxt
 * İdman növləri
 * Dövrə və bölünmə datası
 * GPS izi
 * Sensor məlumatları
 * Aktiv sessiya üçün tədbirlər

Fəaliyyət məlumatları real vaxt rejimində faylda qeyd oluna bilər və ya fəaliyyət qeydi tamamlandıqdan sonra ixrac edilə bilər.

### FIT Fəaliyyət Mesajları

FIT fəaliyyət faylına bəzi tələb olunan mesaj növləri daxil ola bilər. Aşağıdakılar fəaliyyət faylı üçün tələb olunan mesajlardır.

|Mesaj|Məqsəd|
---|---|
|Fayl İD| Fayl İd mesajı bütün FIT fayl növləri üçün tələb olunur və faylda ilk mesaj olması gözlənilir. Fəaliyyət faylları üçün Type xassəsi 4.| olaraq təyin edilməlidir
|Fəaliyyət| FIT Fəaliyyət faylında tək Fəaliyyət mesajı tələb olunur. Fəaliyyət mesajına Yerli Vaxt Damgası və Sessiya Sayı xassələri daxildir. Yerli vaxt möhürü fayldakı bütün vaxt ştamplarına tətbiq oluna bilən vaxt qurşağı ofsetini müəyyən etmək üçün istifadə olunur. Əksər cihazlar FIT fayllarını real vaxt rejimində qeyd edir və sessiyanın sayı qeydin sonuna qədər məlum olmayacaq. Buna görə Fəaliyyət mesajı çox vaxt faylda son mesaj olacaq.|
|sessiya| Fəaliyyət fayllarında bir və ya daha çox Sessiya mesajı olacaq. Sessiya mesajı Xülasə mesaj növüdür. Başlama Vaxtı, Toplam Keçən Vaxt, Ümumi Taymer vaxtı və Zaman möhürü bütün xülasə mesajları üçün tələb olunan sahələrdir.|
|Lap| Döngə mesajları sessiya daxilində dövrələri və ya intervalları təmsil edir. Lap mesajı Xülasə mesaj növüdür. Başlama Vaxtı, Toplam Keçən Vaxt, Ümumi Taymer vaxtı və Zaman möhürü bütün xülasə mesajları üçün tələb olunan sahələrdir.|
|Qeyd| Qeyd mesajlarına GPS koordinatı, sürət, məsafə, ürək dərəcəsi, güc və s. daxildir.|

## FIT Fayl Faydalı Resurslar

 * [FIT Fəaliyyət Fayllarının Deşifrəsi](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
 * [FIT Fəaliyyət Fayllarının Kodlanması](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 
## İstinadlar ##

* [FIT Fəaliyyət Faylı](https://developer.garmin.com/fit/file-types/activity/)


