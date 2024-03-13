{
  "date": "2019-10-11",
  "keywords": [
"dng faylı",
"dng fayl formatı",
"dng faylı nədir",
"fayl",
"dng nümunəsi",
"dng fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DNG - Rəqəmsal Kamera Şəkil Fayl Formatı",
  "description": "DNG faylları yarada və aça bilən DNG fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dn-azg"
}
},
  "lastmod": "2019-09-10"
}

## DNG faylı nədir?

DNG is a digital camera image format used for the storage of raw files. It has been developed by Adobe in September 2004. Əsasən rəqəmsal fotoqrafiya üçün hazırlanmışdır. DNG [TIFF](/image/tiff/)/EP standart formatının genişləndirilməsidir və metadatadan əhəmiyyətli dərəcədə istifadə edir. Rəqəmsal kameralardan alınan xam məlumatları çeviklik və bədii nəzarət asanlığı ilə manipulyasiya etmək üçün fotoqraflar raw kamera fayllarını seçirlər. JPEG və TIFF formatları kamera tərəfindən emal edilən şəkilləri saxlayır, buna görə də belə formatlarda dəyişiklik üçün çox yer yoxdur.

## DNG Fayl Formatının Tarixi və Versiyaları

Till now there have been 5 versions of DNG specification so far. Version 1.0.0.0 was launched in September 2004 along with the release of "2.3" (ACR and DNG Converter). In February 2005 version 1.1.0.0 was published.  In May 2008 version 1.2.0.0 was released and was used in "4.4". Version 1.3.0.0 was published in June 2009. 1.4.0.0 versiyası 2012-ci ildə çıxdı.

## DNG fayl formatı

Halbuki kamera xam faylları işlənməmiş və ya az işlənmiş məlumatları birbaşa sensordan alır. Onlar film neqativlərinə bənzədiklərinə görə kamera xam formatları həm də Rəqəmsal Neqativlər” kimi tanınır. Xam formatların faydası son istifadəçi üçün artan bədii nəzarətdir. İstifadəçi tələblərə uyğun olaraq müxtəlif parametr diapazonlarını tənzimləyə bilər, məsələn, ağ balansı, ton xəritəsi, səs-küyün azaldılması, kəskinləşdirmə və s. Digər tərəfdən, kameranın xam faylı hər hansı bir proqram və ya çevirici vasitəsilə hər hansı istifadə üçün işlənməlidir.

Kamera xam faylları üçün standart format olmadığı üçün bu, son istifadəçi üçün çoxlu problemlər yaratdı. Bu problemlər Adobe tərəfindən həll edildi və kamera xam faylları üçün qeyri-mülkiyyət formatı müəyyən edildi. Format Digital Negative və ya DNG kimi tanınır. DNG xam faylların emalı üçün geniş çeşiddə aparat və proqram təminatı tərəfindən istifadə oluna bilər. Bundan əlavə, DNG, ilkin olaraq kameranın öz xüsusi xam formatlarına malik olması ilə çəkilmiş şəkilləri saxlamaq üçün aralıq format kimi də istifadə edilə bilər.

### DNG Fayl Formatının Xüsusiyyətləri

Bu bölmədə biz DNG formatını TIFF 6.0-ın uzantısı kimi təsvir edəcəyik.

* **Fayl Genişləndirmələri**: DNG “.DNG” və ya “.TIF” genişləndirmələrindən istifadə edir.

* **SubIFD Ağacları**: DNG SubIFD zəncirlərini dəstəkləmir, bunun əvəzinə DNG TIFF-EP spesifikasiyalarında qeyd edildiyi kimi SubIFD ağaclarının istifadəsini tövsiyə edir. Ən yüksək keyfiyyət və ayırdetmə NewSubFileType 0-dan istifadə edə bilər, aşağı keyfiyyətli miniatürlər isə 1-ə bərabər NewSubFileType-dən istifadə etməlidir. Həmçinin tövsiyə olunur, lakin ilk IFD-nin aşağı keyfiyyətli və ya ayırdetmə rezolyusiyasına malik olması tələb olunmur.

* **Bayt Sırası**: Bayt sırası DNG oxuyucuları tərəfindən, həmçinin müəyyən kamera modelindən olan fayllar üçün dəstəklənməlidir.

* **Maskalı Piksellər**: Kamera sensorlarının əksəriyyəti qara kodlaşdırma vasitəsilə sensorun kənarındakı tam maskalanmış pikselləri hesablayır. Bu piksellər ya daxil edilə bilər, ya da şəkil DNG formatında saxlanmazdan əvvəl kəsilə bilər. Əgər maskalı piksellər kəsilməyibsə, onda bu piksellərin sahəsi ActiveArea teqində qeyd edilməlidir. Qara kodlaşdırma səviyyəsi ilə bağlı bu piksellərdən toplanan məlumat ya xam məlumat saxlanmazdan əvvəl istifadə edilməlidir, ya da qaranın səviyyəsini göstərən DNG faylına daxil edilə bilər.

* **Qüsurlu Piksellər**: Xam məlumatları DNG kimi saxlamazdan əvvəl, qüsurlu piksellər xaric edilməlidir.

* **Metaməlumat**: Metadata aşağıdakı üsullardan hər hansı biri ilə DNG-yə daxil edilə bilər:  

** TIFF-EP və ya EXIF metadata teqlərindən istifadə etməklə
** IPTC metadata etiketi vasitəsilə (33723)
** XMP metadata etiketindən istifadə (700)
* **Proprietary Data**: Adətən satıcılar öz çeviriciləri tərəfindən istifadə edilmək üçün xam fayla mülkiyyət məlumatlarını daxil edirlər. DNG öz mülkiyyət məlumatlarını şəxsi etiketlərdə, şəxsi IFD-lərdə və özəl MakerNote-da saxlayır. Satıcılar DNG fayllarını redaktə edən proqramların bu mülkiyyət məlumatlarını qoruduğuna əmin olmaq üçün DNGPrivateData və MakerNoteSafety teqlərindən istifadə etməlidirlər.


Aşağıda TIFF teqlərinin bəzi mühüm məhdudiyyətləri və uzantıları verilmişdir.

**BitsPerSample**

8 ilə 32 bit/nümunə dəstəklənir. SamplesPerPixel 1-ə bərabər olmadıqda hər nümunə üçün eyni dərinlik olmalıdır. Lakin BitsPerSample 8 və ya 16 və ya 32-yə bərabər deyilsə, o zaman bitlər TIFF standart FillOrder 1 (böyük-endian) istifadə edərək baytlara yığılmalıdır.

**Sıxılma**

İki Sıxılma etiketi dəyəri dəstəklənir:

* Dəyər # 1: Sıxılmamış məlumat.

* Dəyər # 7: JPEG sıxılmış məlumat, ya baza DCT JPEG, ya da itkisiz JPEG sıxılma.


**Fotometrik Tərcümə**

Aşağıdakı dəyərlər yalnız miniatür və önizləmə IFD-ləri üçün dəstəklənir:

* 1 = BlackIsZero. Qamma 2.2 rəng məkanında olduğu güman edilir.

* 2 = RGB. sRGB rəng məkanında olduğu güman edilir.

* 6 = YCbCr. JPEG kodlu önizləmə şəkilləri üçün istifadə olunur.


Aşağıdakı dəyərlər xam IFD üçün dəstəklənir və kameranın doğma rəng məkanı olduğu güman edilir:

* 32803 # CFA (Rəng Filtri Massivi).

* 34892 # LinearRaw.


**Orientasiya**

Orientation tag fayl brauzerləri üçün istifadə olunur ki, onlar DNG fayllarının itkisiz fırlanmasını həyata keçirə bilsinlər. DNG oxucuları güzgü istiqamətləri də daxil olmaqla bütün mümkün istiqamətləri dəstəkləməlidir.

## DNG-nin Son Versiyasında Xüsusiyyətlər

DNG Version 1.4 Oktyabr 2012 aşağıdakı təkmil xüsusiyyətlərə malikdir.

* Defolt İstifadəçi Crop

* Şəffaflıq

* Üzən nöqtə (HDR)

* İtkili sıxılma

* Proksilər


## İstinadlar ##

* [DNG Xüsusiyyətləri - Adobe tərəfindən](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0 .0.pdf)

* [Rəqəmsal Mənfi - Vikipediya](https://en.wikipedia.org/wiki/Digital_Negative)

* [DNG - Rəqəmsal kameranın xam məlumatları üçün ictimai arxiv formatı](https://helpx.adobe.com/camera-raw/digital-negative.html)


