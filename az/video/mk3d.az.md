{
  "date": "2021-23-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MK3D fayl formatı",
  "keywords": [
"mk3d",
"matroska video",
"mkv formatı",
"stereoskopik 3d",
"StereoRejim",
"video",
"fayl",
"format"
],
  "description": "Matroska və MK3D faylları yarada və aça bilən API-lər tərəfindən yaradılmış stereoskopik 3D videolar üçün MK3D fayl formatı haqqında məlumat əldə edin.",
  "linktitle": "MK3D",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk3-azd"
}
},
  "lastmod": "2021-23-02"
}

## MK3D faylı nədir? ##

MK3D faylları Matroska video formatları ailəsinə aiddir. Bu fayllar əslində Matroska 3D formatından istifadə etməklə yaradılmış **stereoskopik 3D** videolardır. MKV faylı Konteyner stereoskopik 3D video materialının növünü müəyyən etmək üçün StereoMode sahəsinin dəyərindən istifadə edir. Mavi və qırmızı rəngləri ayıraraq köhnə stereo 3D videoları göstərmək üçün StereoMode dəyəri də mövcuddur (AnaGlyph)

## Texniki təfərrüatlar ##
3D videolar aşağıdakı iki yolla sıxıla bilər:

- Hər göz üçün ayrıca yol.
- Hər bir göz izləməni bir trekdə birləşdirin.

MKV fayl konteyneri bunların hər ikisini dəstəkləyir.

İçərisində olan 3D materialı ilə daha asan olan tək trekli videolar üçün siz **StereoMode** sahəsini təyin etməlisiniz ki, bu da təyyarələrin mono və ya sol sağ birləşdirilmiş trekdə yığılmasına qərar verir. Aşağıdakı StereoMode sahə dəyərlərindən birini istifadə edə bilərsiniz:

|Dəyər | Təsvir |
|---|---|
|0| mono|
|1| yan-yana (sol göz birincidir)|
|2| yuxarı-aşağı (sağ göz birincidir)|
|3| yuxarı-aşağı (sol göz birincidir)|
|4| checkboard (sağda birincidir)|
|5| checkboard (sol birincidir)|
|6| sıra interleaved (sağ birincidir)|
|7| sıra interleaved (sol birincidir)|
|8| sütun interleaved (sağda birincidir)|
|9| sütun interleaved (sol birincidir)|
|10| anaqlif (göy/qırmızı)|
|11| yan-yana (sağ göz birincidir)|
|12| anaqlif (yaşıl/magenta)|
|13| hər iki göz bir blokda bağlanır (sol göz birincidir) (sahə ardıcıl rejimi)|
|14| hər iki göz bir blokda bağlanır (sağ göz birincidir) (sahə ardıcıl rejimi)|

Çoxsaylı treklər üçün MKV konteyneri hər bir trekin funksionallığına ayrıca qərar verməlidir. İşi yerinə yetirmək üçün **TrackCombinePlanes** ilə **TrackOperation** istifadə olunur.


## İstinadlar ##

- [Matroska Specification Notes](https://www.matroska.org/technical/notes.html)
- [MKV File Container Support for Stereo 3D Video and the MK3D Files](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

