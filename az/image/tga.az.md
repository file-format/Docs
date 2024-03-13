{
  "date": "2019-10-11",
  "keywords": [
"tga faylı",
"tga fayl formatı",
"tga faylı nədir",
"fayl",
"tga misal",
"tga fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGA Fayl Format - TARGA Qrafik Şəkil Faylı",
  "description": "TGA fayl formatı və TGA faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "TGA",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-tg-aza"
}
},
  "lastmod": "2019-09-10"
}

## TGA faylı nədir?

.tga genişləndirilməsi olan fayl rastr qrafik formatıdır və Truevision Inc tərəfindən yaradılmışdır. O, TARGA (Truevision Advanced Raster Adapter) lövhələri üçün nəzərdə tutulmuşdur və IBM-ə uyğun gələn kompüterlər üçün Highcolor/truecolor displey dəstəyi ilə təmin edilmişdir. O, piksel başına 8, 16, 24 və 32 bit və 8 bitlik alfa kanalını dəstəkləyir. O, həmçinin təsvir ölçüsünü azaltmaq üçün tətbiq oluna bilən itkisiz RLE sıxılmanı dəstəkləyir. Rəqəmsal fotoşəkillər və fakturalar TGA şəkil formatından istifadə edir.

## Qısa tarix

TGA fayl formatının formalaşması 1984-cü ildə AT&T tərəfindən rəngli çərçivə tamponları üçün işlənib hazırlanmış yeni texnologiyaların marketinqi üzərində işləyən AT&T EPICenter (sonradan çıxarılaraq Truevision kimi tanınan müstəqil bir qurum kimi formalaşdı) tərəfindən yarandı. EPICenter artıq ilk iki kartı, VDA (Video Ekran Adapteri) və ICB (şəkil çəkmə lövhəsi) üzərində işləyirdi ki, onlar üçün iki fayl növü, .vda və .icb üzərində işləyirlər. Bu fayl formatları kodlaşdırıldı və daha az geniş spesifik fayl formatı TGA təqdim edildi. TGA artıq istifadə edilənlərin bir uzantısı idi və genişlik, hündürlük, piksel dərinliyi, əlaqəli rəng xəritəsi və təsvirin mənşəyi kimi məlumatları təmin etdi.

TGA-nın 1989-cu ildə nəşr olunan 2.0 versiyası bir neçə təkmil funksiyaları özündə birləşdirdi, məsələn:

 * Miniatürlər
 * Alfa kanalı
 * Qamma Dəyəri
 * Mətn metadata

TGA-nın 2.0 versiyasına əsas töhfə verənlər arasında Truevision-dan Shawn Steiner, Kevin Fiedly və David Spoelstra var.

## TGA TARGA Fayl Formatının Xüsusiyyətləri

TGA faylı 2 əsas hissədən ibarətdir:

 * Başlıq
 * Color Pixel məlumatı

TGA faylındakı bütün dəyərlər format spesifikasiyasına uyğun olaraq littl-endian-dadır.

### TGA Başlığı

TGA fayl başlığı aşağıdakı 5 sahədən ibarətdir.

|Sahə nömrəsi.|Uzunluq |Sahənin adı |Təsvir|
---|---|---|---|
|1| 1 bayt |ID uzunluğu| Şəkil ID sahəsinin uzunluğu (0-255)|
|2| 1 bayt |Rəng xəritəsi növü| Rəngli xəritənin daxil olub-olmaması (0 - bu şəkilə heç bir rəngli xəritə məlumatının daxil edilmədiyini göstərir. 1 - rəng xəritəsinin bu şəkilə daxil olduğunu bildirir.)|
|3| 1 bayt |Şəkil növü| Sıxılma və rəng növləri (0- Şəkil Məlumatı Daxil Olmayıb. 1- Sıxılmamış, Rəngli təsvir edilmiş şəkil, 2- Sıxılmamış, Həqiqi Rəngli Şəkil, 9- Uzunluğu kodlanmış, Rəngli xəritələnmiş şəkil, 11- Uzunluğu kodlanmış, Qara və ağ şəkil )|
|4| 5 bayt |Rəng xəritəsinin spesifikasiyası| Rəng xəritəsini təsvir edir|
|5| 10 bayt |Şəkil spesifikasiyası| Şəkil ölçüləri və formatı|

### Şəkil və Rəng Xəritə Məlumatı

|Sahə №. |Uzunluq |Sahə |Təsvir|
---|---|---|---|
|6 |Şəkil ID uzunluğu sahəsindən| Şəkil ID| İdentifikasiya məlumatını ehtiva edən əlavə sahə|
|7 |Rəng xəritəsinin spesifikasiyası sahəsindən| Rəngli xəritə məlumatları| Rəngli xəritə məlumatlarından ibarət axtarış cədvəli|
|8 |Şəkil spesifikasiyası sahəsindən| Şəkil datası| Şəkil deskriptoruna uyğun saxlanılır|

### Tərtibatçı Sahəsi (İstəyə görə)

TGA Version 2.0 bir çox tərtibatçının daha çox məlumat saxlamaq istədiyi əlavə təkmilləşdirmələr/əlavələr üçün dəstək verir. Məlumat isteğe bağlıdır ki, TGA dekoderi onu şərh edə bilmirsə, ona məhəl qoyulmayacaq.

### Uzatma Sahəsi (İstəyə görə)

|Sahə nömrəsi.| Uzunluq| Sahə |Təsvir|
---|---|---|---|
|10| 2 bayt |Genişləndirmə ölçüsü |Genişləndirmə sahəsinin bayt ölçüsü, həmişə 495|
|11| 41 bayt| Müəllifin adı |Müəllifin adı. İstifadə edilmirsə, baytlar NULL (\0) və ya boşluq|-a təyin edilməlidir
|12| 324 bayt| Müəllif şərhi| Hər biri 80 simvol və NULL|-dan ibarət dörd sətir kimi təşkil edilmiş şərh
|13| 12 bayt| Tarix/vaxt möhürü |Şəklin yaradıldığı tarix və vaxt|
|14| 41 bayt| İş ID||
|15| 6 bayt| İş vaxtı| Faylın yaradılmasına sərf olunan saatlar, dəqiqələr və saniyələr (hesab üçün və s.)|
|16| 41 bayt| Proqram İD |Faylı yaradan proqram.|
|17| 3 bayt| Proqram təminatı versiyası||
|18| 4 bayt| Açar rəngi||
|19| 4 bayt| Piksel aspekt nisbəti||
|20| 4 bayt| Qamma dəyəri||
|21| 4 bayt| Rəng korreksiyası ofseti |Faylın əvvəlindən mövcud olduqda rəng korreksiyası cədvəlinə qədər baytların sayı|
|22| 4 bayt| Poçt markası | Əgər varsa, faylın əvvəlindən poçt markası şəklinə qədər olan baytların sayı|
|23| 4 bayt| Skan xətti ofset| Əgər varsa, faylın əvvəlindən skan xətləri cədvəlinə qədər baytların sayı|
|24| 1 bayt| Atributların növü| Alfa kanalını müəyyən edir|

### Fayl Altbilgisi (Könüllü)

Faylın son 26 baytı altbilgini təmsil edir, əgər varsa, TGA versiyası 2 faylı deməkdir.

|Sahə No.| Uzunluq| Sahə| Təsvir|
---|---|---|---|
|28| 4 bayt| Uzatma ofseti| Faylın əvvəlindən baytlarla ofset|
|29| 4 bayt| Developer sahəsi ofset| Faylın əvvəlindən baytlarla ofset|
|30| 16 bayt| İmza| Tərkibində TRUEVISION-XFILE|
|31| 1 bayt| | Tərkibində .|
|32| 1 bayt| | NULL| ehtiva edir


## İstinadlar

 * [TGA 2.0 File Format Specifications](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
 * [TGA by Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

