{
  "date": "2019-10-11",
  "keywords": [
"jp2 faylı",
"jp2 fayl formatı",
"jp2 faylı nədir",
"fayl",
"jp2 nümunəsi",
"jp2 fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JP2 - Şəkil Fayl Formatı",
  "description": "JP2 faylları yarada və aça bilən JP2 fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "JP2",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-az2"
}
},
  "lastmod": "2020-08-10"
}

## JP2 faylı nədir? ##

JPEG 2000 (**JP2**) şəkil kodlaşdırma sistemi və ən müasir təsvir sıxılma standartıdır. Bir anda istənilən keyfiyyətdə itkisiz məzmunu kodlaşdırmaq üçün dalğacık texnologiyasından istifadə edir. Üstəlik, kodlaşdırma səmərəliliyində heç bir ciddi cəza olmadan, JPEG 2000 eyni məzmuna daxil olmaq və effektiv şəkildə müxtəlif digər qətnamə və keyfiyyətlərdə deşifrə etmək imkanına malikdir. JPEG 2000-dəki kod axınları məkana təsadüfi giriş imkanı təmin edən maraq bölgələrinə malik olmaqla əhəmiyyətli dərəcədə genişlənə bilir.

JPEG 2000 ən genişlənən standartlardan biri kimi seçilir. Təsvirin müxtəlif hissələri müxtəlif keyfiyyətlərdən istifadə etməklə saxlanıla bilər. Kod axınını müxtəlif yollarla sifariş etməklə diqqətəlayiq performans artımına nail olmaq olar. Buna baxmayaraq, JP2 bu çevikliyin nəticəsi olaraq mürəkkəb və hesablama baxımından çətin kodlayıcılar/dekoderlər tələb edir. JPEG ilə müqayisədə, JPEG 2000 yalnız təsvirin kənarına yaxın halqalar yaradan və bulanıq ola bilən zəng çalan artefaktlar istehsal edir, JPEG isə həm zəng çalan, həm də bloklayan artefaktlar ola bilən 8×8 vizual artefakt bloklarından istifadə edir. Terapikslərdə ölçüləri və 38 bit/nümunə qədər yüksək dəqiqliyə malik 16384-ə qədər müxtəlif komponentə sahib olmaq.

## Tarix ##

2000-ci ildə Birgə Fotoqrafiya Mütəxəssisləri Qrupu komitəsi JP2-ni bu yeni dalğa-əsaslı metodla diskret kosinus transformasiyasına əsaslanan JPEG standartını təkmilləşdirmək məqsədi ilə dizayn etdi. JPEG komitəsi öz əsas metodlarını lisenziya haqqı olmadan təmin etməyi qarşısına məqsəd qoymuşdu. 20 şirkət arasında rəqabət qazanan JP2 lisenziyasında onlar bığla qalib gəldilər. JPEG 2000 ISO standartı kimi elan edilmişdir, baxmayaraq ki, əksər veb-brauzerlər 2017-ci ildən bəri JPEG 2000-ə kömək etməyə hazır deyillər.

## JPEG 2000 şəkil kodlaşdırma sisteminin hissələri ##

Aşağıda JPEG 2000 standartlarının tam dəstini təşkil edən əsas hissələr verilmişdir.


|Hissə|Başlıq|Təsvir|Nömrə
---|---|---|---|
|1-ci hissə|Əsas kodlaşdırma sistemi| Kod axınının sintaksisini müəyyənləşdirir. JPEG 2000 şəkillərinin dekodlanması ilə bağlı müxtəlif mərhələlər. Əsas fayl formatı JP2, metadata və təmin ediləcək İP hüquqlarını izah edir.|ISO/IEC 15444-1
|2-ci hissə|Genişləndirmələr|Fayl formatı kod axını üçün genişlənmələri müəyyənləşdirir və HDR nümunə nümayişlərinə, rəng məkanının spesifikasiyasına, kəsmə, həndəsi transformasiyalara imkan verir; müxtəlif animasiyalar, metadata və çoxlu kod axını.|ISO/IEC 15444-2
|3-cü hissə|Motion JPEG 2000 (MJ2 və ya MJP2)|Müstəqil kod axınında şəkilləri kodlaşdıran hərəkət ardıcıllığı üçün fayl formatını təqdim edin.|ISO/IEC 15444-3
|Part 4|Uyğunluq|Kodlaşdırma və dekodlaşdırma üçün test üsullarını bildirir və faylları həm çılpaq kod axınları, həm də JP2 faylları üçün yoxlayır.|ISO/IEC 15444-4
|Part 5|İstinad proqramı|Core kodlaşdırma sistemini həyata keçirən və açıq mənbə lisenziyaları altında mövcud olan iki mənbə kodu paketindən (Java, C) ibarətdir.|ISO/IEC 15444-5
|Part 6|Mürəkkəb şəkil fayl formatı|JPM fayl formatını müəyyən edir və faks kimi proqramlar üçün çox səhifəli sənəd təsvirinə imkan verir. JBIG2 və JPEG istifadəsini dəstəkləyir.|ISO/IEC 15444-6
|Part 8|JPEG 2000 Secured (JPSEC)|Tranzaksiyaların, məzmunun və texnologiyaların təhlükəsizliyini təmin edir və təhlükəsiz JPEG 2000 bit axınlarına icazə verir.|ISO/IEC 15444-8
|Part 9|JPIP|Metaməlumatlara və təsvirlərə daxil olmaq üçün şəbəkə mühitində alətləri müəyyənləşdirir və İnteraktiv və səmərəli protokolları bildirir|ISO/IEC 15444-9
|10-cu hissə|JP3D|1-ci hissənin həcmli genişləndirilməsi və Z ölçüsünü təqdim edir. Plitələr, kod blokları, məntəqələr və 3D maraq bölgəsi əlçatanlıq xüsusiyyətləri konsepsiyasını genişləndirir.|ISO/IEC 15444-10
|Hissə 11|JPWL|Səhvlərə meylli simsiz şəbəkə üzərindən yaxşı təşkil edilmiş ötürmə ilə məşğul olur. Bu genişləndirmə dekoderlər|ISO/IEC 15444-11 ilə uyğun gəlir
|Hissə 13|Giriş Səviyyəsi Kodlayıcı|Əsas kodlaşdırma sisteminin giriş səviyyəli kodlayıcı tətbiqini müəyyən edir.|ISO/IEC 15444-13
|14-cü hissə|JPXML|XML-də təqdimat və marker seqmentlərini və təsvirin daxili məlumatlarına daxil olmaq üsullarını izah edir.|ISO/IEC 15444-14
|Hissə 15|HTJ2K (İnkişaf mərhələsindədir)|Alternativ blok kodlaşdırma alqoritmini təyin edir. Alqoritm on qat artan ötürmə qabiliyyəti və itkisiz kodlaşdırma/deşifrə təklif edir.|

## JP2 Fayl Format ##

JPEG 2000 defines file format as well as code stream in the same way as JPEG-1. Şəkil nümunələrinin yalnız JPEG 2000 tərəfindən təsvir edilməsinə baxmayaraq, JPEG-1 rəng məkanı və təsviri kodlaşdırmaq üçün vacib olanın həlli ilə bağlı digər əlavə məlumatları ehtiva edir. Əgər şəkil JPEG 2000 faylı kimi saxlanılırsa, **.jp2** genişləndirmə kimi istifadə olunur. Bu fayl formatı animasiya mexanizmlərini və çoxsaylı kod axınlarının konfiqurasiyasını bir təsvirə təyin edən JPEG 2000 part-2 genişləndirilməsi ilə daha da təkmilləşdirilir. **.jpx** uzantısı bu genişləndirilmiş fayl formatından istifadə edərək şəkillər saxladıqda istifadə olunur. Kod axını məlumatları ilk növbədə fayllarda saxlanmadığı üçün bu məqsəd üçün heç bir standart genişləndirmə müəyyən edilmir. Baxmayaraq ki, sınaq məqsədləri üçün o, tez-tez **.jpc** və ya **.j2k** uzantısını alır. JPEG-1-dən fərqli olaraq, JPEG 2000 XML formatında metaməlumatların kodlaşdırılmasının fərqli üsulunu seçir. Standart 12234-1.4 (ISO TC42 komitəsi tərəfindən) Exif teqləri və XML komponentləri arasında istinad kimi istifadə olunur. JPEG 2000 daxilində ISO standartı, XMP ola bilər.

### Parçalar ###
JPEG 2000 faylları ardıcıl parçalardan ibarətdir. Hər bir parçanın 8 bayt başlığı var: 4 baytlıq parça ölçüsü (böyük-endian, birinci yüksək bayt) və 4 baytlıq yığın növü - əvvəlcədən müəyyən edilmiş imzalardan biri: jP və ya jP2.

Second chunk must be of type "ftyp" and has a sub-type at offset 8. JPEG 2000 dəyərlərdən biri olan alt tiplə müəyyən edilmişdir: jp2 (fayl növü \*.JP2), jp20 (fayl növü \*.JPA), jpm (fayl növü \*.JPM), jpx  (fayl növü \*.JPX).

Naməlum növ aşkarlanana qədər təkrarlanan parçalar, biz JPEG 2000 şəkil/video faylı tərtib edirik.

### Rəng çevrilməsi ###

Əvvəlcə şəkillərin RGB rəng məkanından başqa rəng məkanına çevrilməsi tələb olunur. Bu məqsədlə iki yol var: Geri Dönməz Rəng Dönüşümü (İKT) və Geri Dönüşümlü Rəng Dəyişməsi (RCT). Əvvəllər YC,,B,,C,,R,, rəng məkanından istifadə edir və fiksasiya/üzən nöqtədə, sonra isə dəyişdirilmiş YUV rəng məkanında həyata keçirilməlidir və təbiətdə geri çevrilir.// //RGB modeli, JPEG ilə məhdudlaşmır. 2000 dil çox komponentli transformasiyadan istifadə edir.

### Döşəmə ###

Rəng çevrilməsi tamamlandıqda, şəkil ayrıca çevrilə və kodlaşdırıla bilən plitələr adlanan düzbucaqlı bölgələrə çevrilir. Bütün plitələrin ölçüsü eyni olacaq və ya bütün təsviri bir kafel kimi qəbul etmək olar. Dekoder kirəmitdən istifadə edir və daha az yaddaş istehlak edir və ya bəzi plitələri qismən kodlaya bilir. Baxmayaraq ki, bu texnikanın dezavantajı şəklin keyfiyyətinin pisləşməsidir.

### Dalğacıq çevrilməsi ###

Döşəmədən sonra görüntü ya dönməz və ya geri dönə bilən dalğalara çevrilir və bükülmə və ya qaldırma sxemindən istifadə etməklə həyata keçirilir.

### Sıxılma Oranı ###

Şəklin fiziki xüsusiyyətlərindən asılı olaraq, 20% sıxılma qazancı əldə edilir JPEG 2000-in məkan-ehtiyat proqnozu sıxılma prosesində mühüm rol oynayır və yüksək ayırdetmə təsvirləri ən çox üstünlük əldə etməyə meyllidir.

## Standart ## tərəfindən xidmət edilən proqramlar

* Çərçivə əsaslı HD videoların yazılması, redaktəsi və saxlanması

* Tibbi görüntülər və biometrik məlumatlar

* peyk şəkilləri, uzaqdan zondlama və hərəkət aşkarlanması

* Müştəri/server rabitəsi, şəbəkə paylanması və saxlanması.

* Rəqəmsal kinoteatr, Canlı HDTV yayımı, Rəqəmləşdirilmiş Audio-vizual materiallar


## İstinadlar ##

* [JPEG 2000-ə baxış](https://jpeg.org/jpeg2000/)

* [JPEG 2000 şəkil kodlaşdırma sistemi](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)


