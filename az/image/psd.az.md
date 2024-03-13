{
  "date": "2019-10-11",
  "keywords": [
"psd faylı",
"psd fayl formatı",
"psd faylı nədir",
"fayl",
"psd nümunəsi",
"psd fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSD - Photoshop Şəkil Fayl Formatı",
  "description": "PSD fayl formatı və PSD faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "PSD",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-azd"
}
},
  "lastmod": "2019-09-10"
}

## PSD faylı nədir?

PSD, Photoshop Document, qrafik dizaynı və inkişafı üçün istifadə olunan Adobe Photoshop-un doğma fayl formatını təmsil edir. PSD fayllarına şəkil qatları, tənzimləmə təbəqələri, təbəqə maskaları, annotasiyalar, fayl məlumatı, açar sözlər və digər Photoshop-a xas elementlər daxil ola bilər. Photoshop faylları .PSD kimi standart genişlənməyə malikdir və maksimum hündürlüyü və eni 30.000 piksel və uzunluq həddi iki gigabaytdır.

## PSD Fayl Formatının Xüsusiyyətləri ##

PSD faylındakı məlumatlar böyük endian bayt sırası ilə saxlanılır. Bu, Windows platformasında oxuyarkən və ya yazarkən qısa və uzun tam ədədlərin dəyişdirilməsini nəzərdə tutur. Photoshop fayl formatı beş əsas hissəyə bölünür. Bir bölmədən digərinə keçmək üçün istifadə edilə bilən bir çox uzunluq işarəsi var. Uzunluq markerləri adətən ən yaxın 2 və ya 4 bayt intervala yuvarlaqlaşdırmaq üçün baytlarla doldurulur. Beş əsas hissə bunlardır:

* Fayl başlığı

* Rəng rejimi məlumatları

* Şəkil Resursları

* Qat və Maska Məlumatı

* Şəkil məlumatları


Uyğunluq üçün məlumatlar bölmənin bütün bu sahələrinə yazılmalıdır, çünki Photoshop bütün bölməni oxumağa cəhd edə bilər. Bu, həmçinin fayla yazarkən atlanmış sahələrə sıfırların yazılmasını nəzərdə tutur. Uzunluğu ilə ayrılmış bölmələrdəki uzunluq sahəsi oxumağın nə vaxt dayandırılacağına qərar vermək üçün istifadə edilməlidir. Əksər hallarda, uzunluq sahəsi qeydlərin deyil, baytların sayını göstərir. Faylı oxuyarkən aşağıdakı məqamları yadda saxlamaq lazımdır.

* Bütün cədvəllərdə "Uzunluq" sütunundakı qiymətlər baytlardadır.

* Unicode sətri kimi təyin olunan bütün dəyərlər aşağıdakılardan ibarətdir:

* Sətirdəki simvolların sayını göstərən 4 bayt uzunluğunda sahə (bayt deyil).

* Unicode dəyərlər sətri, hər simvol üçün iki bayt.


### Fayl başlığı ###

Fayl başlığı təsvirin əsas xüsusiyyətlərini ehtiva edir.

|Uzunluq|Təsvir
---|---|
|4|İmza: həmişə '8BPS' bərabərdir. İmza bu dəyərə uyğun gəlmirsə, faylı oxumağa çalışmayın.
|2|Version: always equal to 1. Versiya bu dəyərə uyğun gəlmirsə, faylı oxumağa çalışmayın. (~*~*PSB~*~* versiya 2-dir.)
|6|Rezerv edilib: sıfır olmalıdır.
|2|İstənilən alfa kanalları daxil olmaqla, şəkildəki kanalların sayı. Dəstəklənən diapazon 1 ilə 56 arasındadır.
|4|Şəkilin piksellərlə hündürlüyü. Dəstəklənən diapazon 1 ilə 30.000 arasındadır.
|4|Şəklin piksellə eni. Dəstəklənən diapazon 1 ilə 30.000 arasındadır.
|2|Dərinlik: kanal başına bitlərin sayı. Dəstəklənən dəyərlər 1, 8, 16 və 32-dir.
|2|Faylın rəng rejimi. Dəstəklənən dəyərlər bunlardır: Bitmap # 0; Boz rəng №1; İndekslənmiş # 2; RGB # 3; CMYK # 4; Çoxkanal №7; Duoton # 8; Laboratoriya № 9.

### Rəng Rejimi Məlumat Bölməsi ###

Rəng rejimi məlumat bölməsi aşağıdakı kimi qurulmuşdur:


|Uzunluq|Təsvir
---|---|
|4|Aşağıdakı Rəng məlumatının uzunluğu
|dəyişən|Rəng məlumatları

Rəng rejimi məlumatları yalnız Fayl Başlığı bölməsindəki rejim sahəsi ilə müəyyən edilmiş indekslənmiş rəng və duoton üçün mövcuddur. Bütün digər rejimlər üçün bu bölmə 4 baytlıq sıfırlanmış dəyərlərlə təmsil olunur. İndekslənmiş rəngli şəkillər üçün uzunluq 768-dir və rəng məlumatı şəkil üçün rəng cədvəlini, interleaved olmayan qaydada ehtiva edir. Duotone şəkilləri üçün rəngli məlumat iki ton spesifikasiyasını ehtiva edir (formatı sənədləşdirilməyib). Photoshop fayllarını oxuyan digər proqramlar iki tonlu təsvirə boz şəkil kimi baxa bilər və faylı oxuyarkən və yazarkən sadəcə olaraq iki ton məlumatının məzmununu qoruya bilər.

### Şəkil Resursları Bölməsi ###

Faylın üçüncü bölməsində şəkil resursları var. Bu, uzunluq sahəsi ilə başlayır, ardınca bir sıra resurs blokları.


|Uzunluq|Təsvir
---|---|
|4|Şəkil resursu bölməsinin uzunluğu. Uzunluğu sıfır ola bilər.
|Dəyişən|Şəkil Resursları (Şəkil Resurs Blokları)

Şəkil resursları qələm aləti yolları kimi şəkillərlə əlaqəli qeyri-piksel verilənləri saxlamaq üçün istifadə olunur. Onlara resurs blokları deyilir, çünki onlar Photoshop-un ilkin versiyalarında Macintosh resursunda saxlanılan məlumatları saxlayırlar. Şəkil resurs bloklarının əsas strukturu aşağıda göstərildiyi kimidir:


|Uzunluq|Təsvir
---|---|
|4|İmza: '8BIM
|2|Resurs üçün unikal identifikator. Şəkil resurs identifikatorları Photoshop tərəfindən istifadə edilən resurs identifikatorlarının siyahısını ehtiva edir.
|Dəyişən|Ad: Paskal sətri, ölçüsü bərabər etmək üçün doldurulmuşdur (null ad 0-dan iki baytdan ibarətdir)
|4|Aşağıdakı resurs məlumatlarının faktiki ölçüsü
|Dəyişən|Fərdi resurs növləri üzrə bölmələrdə təsvir olunan resurs məlumatları. Ölçüsü bərabər etmək üçün yastıqlıdır.

Şəkil resursları bir neçə standart ID nömrələrindən istifadə edir.

### Qat və Maska Məlumatı ###

Photoshop faylının dördüncü bölməsində təbəqələrin sayı, təbəqələrdəki kanallar, qarışdırma diapazonları, tənzimləmə təbəqəsi düymələri, effekt qatları və maska parametrləri kimi təbəqələr və maskalar haqqında məlumatlar var. Əgər təbəqələr və ya maskalar yoxdursa, bu bölmə sıfırlanmış 4 baytlıq sahə ilə təmsil olunur. Sıfırlanmış dəyərlərə görə bu bölməni oxuyarkən bölmələrin uzunluğuna xüsusi diqqət yetirilməlidir. Layer və Maska bölməsinin düzülüşü aşağıdakı kimidir:


|Uzunluq|Təsvir
---|---|
|4|Qatın və maskanın məlumat bölməsinin uzunluğu. (PSB uzunluğu 8 baytdır.)
|Dəyişən|Layer haqqında məlumat
|Dəyişən|Qlobal təbəqə maskası məlumatı
|Dəyişən|Müxtəlif tipli verilənləri ehtiva edən işarələnmiş bloklar seriyası.

#### Qat məlumatı ####

Aşağıdakı cədvəldə təbəqə məlumatının yüksək səviyyədə təşkili göstərilir.


|Uzunluq|Təsvir
---|---|
|4|Length of the layers info section, rounded up to a multiple of 2. (PSB uzunluğu 8 baytdır.)
|2|Qatın sayı. Mənfi rəqəmdirsə, onun mütləq dəyəri təbəqələrin sayıdır və birinci alfa kanalı birləşdirilən nəticə üçün şəffaflıq məlumatlarını ehtiva edir.
|Dəyişən|Hər bir təbəqə haqqında məlumat. Bax Layer qeydləri hər bir təbəqə üçün bu məlumatın strukturunu təsvir edir.
|Dəyişən|Kanal təsviri məlumatları. Hər qat üçün bir və ya bir neçə şəkil məlumat qeydini ehtiva edir. Qatlar təbəqə məlumatında olduğu kimi eyni sıradadır

### Şəkil Data ###

Şəkil piksel məlumatları faylın Şəkil Məlumatı bölməsində yerləşir. Image Data bölməsində verilənlərin düzülüşü müstəvi qaydadadır, yəni əvvəlcə bütün qırmızı verilənlər, sonra bütün yaşıl məlumatlar və s. aşağıdakı cədvəldə göstərildiyi kimi.

|Uzunluq|Təsvir
---|---|
|2|Compression method: *0 = Raw image data * 1 = RLE sıxılmış şəkil datası bütün skan xətləri (sətir * kanallar) üçün bayt sayları ilə başlayır, hər sayı iki baytlıq dəyər kimi saxlanılır. RLE sıxılmış verilənləri, hər bir skan xətti ayrıca sıxılmış şəkildə izlənilir. RLE sıxılması Macintosh ROM rutin PackBits və TIFF standartı tərəfindən istifadə edilən eyni sıxılma alqoritmidir. *2 = Proqnozsuz ZIP *3 = Proqnozla ZIP.
|Dəyişən|Şəkil məlumatı. Planar sıra = RRR GGG BBB və s.

## İstinadlar ##

* [PSD Fayl Formatının Xüsusiyyətləri - Adobe tərəfindən](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)

* [Adobe Photoshop Fayl Format](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


