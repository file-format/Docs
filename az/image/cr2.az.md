{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR2 Fayl Format - Canon Raw 2 Şəkil Faylı",
  "description":"CR2 fayl formatı və CR2 fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2-az",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## CR2 faylı nədir?

CR2 (Camera RAW 2) faylı Canon rəqəmsal kameraları tərəfindən yaradılmış RAW şəkil faylıdır. O, kamera tərəfindən çəkilmiş orijinal emal olunmamış itkisiz görüntü məlumatlarını saxlayır. CR2 fayl formatı Canon tərəfindən rəqəmsal kameraları üçün işlənib hazırlanmışdır və 14 bit RGB-ə qədər yüksək keyfiyyətli şəkillər yaza bilir. Bu, kifayət qədər post emal otağı ilə yüksək keyfiyyətli şəkillər istehsal edir. CR2 şəkil formatı Canon tərəfindən 350D, 20D və 1D kamera modellərində istifadə edilmişdir. CR2 faylları RAW fayllarıdır və kamera məlumatı, obyektiv məlumatı, braket məlumatı, ağ balansı və digər parametrlər kimi əlavə metadata məlumatlarını ehtiva edir.

## CR2 Fayl Formatı

CR2 faylları kameranın yaddaş kartında ikili fayllar kimi Canon mülkiyyət fayl formatında saxlanılır. CR2 fayl formatı ilkin istifadə olunan CRW fayl formatını əvəz etdi və daha sonra Canon RAW 3 fayl formatı ilə əvəz olundu. CR2 fayl formatı 4 Şəkil Fayl Kataloquna (IFDs) malik olan [TIFF](/image/tiff/) spesifikasiyasına əsaslanır.

|Ofset |Məzmun |Şərh|
---|---|---|
|0x0000 |Başlıq |bayt sıralamasını, versiyanı və RAW şəklin ofsetini ehtiva edir|
|hesablanmış |IFD#0 |bu hissə Makernotes bölməsini ehtiva edən Exif bölməsini ehtiva edir.
Şəkil#0| haqqında məlumat
|hesablanmış |şəkil#0 |şəklin kiçik versiyası (orijinalın dörddə biri ölçüsü), Jpeg-də sıxılmış|
|hesablanmış |IFD#1 |Şəkil#1 haqqında məlumat.|
|hesablanmış |şəkil#1 |şəklin kiçik versiyası, Jpeg-də sıxılmış|
|hesablanmış |IFD#2 |Şəkil#2 haqqında məlumat.|
|hesablanmış |şəkil#2 |şəklin kiçik versiyası, sıxılmamış|
|başlıqda| IFD#3| Şəkil #3 haqqında məlumat, tam ölçülü RAW şəkil|
|hesablanmış |şəkil#3 |RAW şəkil datası, Jpeg-də itkisiz sıxılmışdır (RGB datası deyil!)|

## CR2 Fayl Formatının üstünlüyü

Şəkillərin RAW formatında saxlanması, Ağ Balansın tənzimlənməsi kimi fotoşəkilə bir çox sonrakı emal etməyə imkan verir. Bu, [JPEG](/image/jpeg/) kimi digər şəkil fayl formatları ilə daha çətin və böyük keyfiyyət itkisi ilə olur.

## CR2 JPEG-dən yaxşıdır?

CR2 faylları heç bir məlumat itkisi olmayan və buna görə də keyfiyyət itkisi olmayan xam fayllardır. Digər tərəfdən JPEG itkili şəkil fayl formatıdır, çünki faylı azaltmaq üçün bəzi məlumatları itirir. Beləliklə, CR2 faylları yüksək keyfiyyətə malikdir və retuş və təkmilləşdirmələr üçün daha uyğundur.

## İstinadlar

 * [CR2 Fayl Format](http://lclevy.free.fr/cr2/)

