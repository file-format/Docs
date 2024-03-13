{
  "date": "2019-10-11",
  "keywords": [
"djvu faylı",
"djvu fayl formatı",
"djvu faylı nədir",
"fayl",
"djvu nümunəsi",
"djvu fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DJVU Fayl Format",
  "description": "DJVU faylları yarada və aça bilən DJVU fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DJVU",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-djv-azu"
}
},
  "lastmod": "2019-09-10"
}

## DJVU faylı nədir?

déjà vu” kimi tələffüz edilən DjVu skan edilmiş sənədlər və kitablar üçün nəzərdə tutulmuş qrafik fayl formatıdır, xüsusən mətn, çertyojlar, şəkillər və fotoşəkillərin birləşməsindən ibarət olanlar. AT&T Labs tərəfindən hazırlanmışdır. O, mətn və fon şəkillərinin şəkil qatının ayrılması, mütərəqqi yükləmə, arifmetik kodlaşdırma və bitonal şəkillər üçün itkili sıxılma kimi bir çox texnikadan istifadə edir. DJVU faylı sıxılmış, lakin yüksək keyfiyyətli rəngli şəkilləri, fotoşəkilləri, mətnləri və çertyojları ehtiva edə bildiyindən və daha az yerdə saxlanıla bildiyindən internetdə elektron kitablar, dərsliklər, qəzetlər, qədim sənədlər və s. kimi istifadə olunur.

DjVu [PDF](/pdf/) üçün üstün alternativ olaraq qiymətləndirilə bilər. DjVu ilə əlaqəli fayl uzantıları .DJVU və ya .DJV-dir. DjVu sıxılma əmsallarına rəngli sənədlər üçün [JPEG](/image/jpeg/) və [GIF](/image/gif/) kimi mövcud üsullardan təxminən 5 – 10, qara və ağ sənədlərdə isə [TIFF](/image/tiff/) ilə müqayisədə 3 – 8 dəfə daha yaxşı nail ola bilər. 25 MB-a qədər tam rəngli 300 DPI-da skan edilmiş sənədlər 30-dan 100 KB-a qədər sıxıla bilər. Eynilə, ağ və qara sənədlər 5-30 KB-a qədər sıxıla bilər. Orta HTML səhifəsi 50 KB-a qədər ola bilər, buna görə də bu sənədləri heç bir problem olmadan şəbəkəyə yükləmək olar.

## Qısa tarix ##

The DjVu technology was developed in AT&T labs by [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner, and Paul G from 1996 to 2001. DjVu fayl formatı ən son 2005-ci ildəki müxtəlif reviziyalardan keçmişdir.


|Versiya|Çıxış tarixi|Qeydlər
---|---|---|
|1–19|1996–1999|Bunlar inkişaf versiyalarıdır.
|20|Aprel 1999|Bir səhifə Çoxsəhifəli formata dəyişdirildi.
|23|İyul 2002|CID yığını
|24|Fevral 2003|LTAnno parça
|21|Sentyabr 1999|Dolaylı yaddaş formatı dəyişdirildi. Mətn axtarış təbəqəsi əlavə edildi.
|22|Aprel 2001|Səhifə oriyentasiyası, rəng JB2
|25|May 2003|NAVM yığını. DjVu əlfəcinləri üçün dəstək əlavə edildi.
|26|Aprel 2005|Mətn/sətir annotasiyaları

## DjVu Fayl Format ##

DjVu documents are IFF85 files. The structure provides a hierarchy of containers which holds information in a DjVu file. These containers are also called “Chunks”. Chunk type and Chunk ID describes how the chunk is used. There is a 4byte header followed by IFF structure. The first four bytes of a DjVu file are 0x41 0x54 0x26 0x54. Bu bölmədə müxtəlif növ DjVu sənədləri və onların ibarət olduğu müvafiq hissələr müzakirə olunur.


|Böyük ID|İstifadə
---|---|
|FORM|İkinci identifikator olan FORM yığınının ilk dörd məlumat baytına malik olan kompozit yığın.
|FORM:DJVM|Çoxsaylı DjVu sənədi. DIRM yığınını ehtiva edən kompozit yığın.
|FORM:DJVU|Bir səhifəlik DjVu sənədi. Djvu sənədində səhifəni təşkil edən parçaları ehtiva edən kompozit parça.
|FORM:DJVI|INCL yığını vasitəsilə daxil edilən paylaşılan” DjVu faylı. Paylaşılan annotasiyalar və forma lüğəti.
|FORM:THUM|Daxil edilmiş miniatürlər olan TH44 parçalarını ehtiva edən kompozit parça.
|DIRM|Çox səhifəli sənədlər üçün səhifə adı məlumatı.
|NAVM|Əlfəcin məlumatı
|ANTa, ANTz|Annotasiyalar həm ilkin görünüş parametrləri, həm də üst-üstə qoyulmuş hiperlinklər, mətn qutuları və s.
|TXTa, TXTz|Unicode Mətn və tərtibat məlumatı.
|Djbz|Paylaşılan forma cədvəli.
|Sjbz|BZZ maskanı saxlamaq üçün istifadə edilən sıxılmış JB2 bitonal data.
|FG44|IW44 verilənləri ön planı saxlamaq üçün istifadə olunur
|BG44|IW44 verilənləri fon saxlamaq üçün istifadə olunur
|TH44|IW44 verilənləri daxili kiçik şəkilləri saxlamaq üçün istifadə olunur
|WMRM|Su nişanını silmək üçün JB2 datası tələb olunur
|FGbz|Rəngli JB2 məlumatı. Müvafiq Sjbz yığınında hər biri üçün rəng təmin edir (blit və ya forma?).
|MƏLUMAT|DjVu səhifəsi haqqında məlumat
|INCL|Daxil edilmiş FORM-un ID-si:DJVI yığını.
|BGjp|JPEG kodlu fon
|FGjp|JPEG kodlu ön plan
|Smmr|G4 kodlu maska

### DJVU sıxılması

Tək şəkil çoxlu müxtəlif şəkillərə bölünür və sonra hər bir şəkil ayrıca sıxılır. DjVu faylının yaradılması üçün şəkil əvvəlcə üç şəkilə, fon, ön plan və maska şəklinə ayrılır. Tipik olaraq arxa plan və ön plan şəkilləri aşağı ayırdetmə ölçülü rəngli şəkillərdir; lakin maska şəkli daha yüksək keyfiyyətli təsvirdir və adətən mətn orada saxlanılır. Ayrıldıqdan sonra ön plan və arxa plan şəkilləri dalğacık əsaslı sıxılma alqoritmi IW44 vasitəsilə sıxılır, maska şəkli isə JB2 adlı başqa üsulla sıxılır.

JB2 kodlaşdırma metodu, müəyyən bir şriftdə simvolun çoxsaylı təkrarlanması kimi səhifədə eyni formaları müəyyən etməklə mətn təsvirindəki çoxluqların çoxunu aradan qaldırır. JB2 əvvəlcə oxşar formalar arasında artıqlıqdan istifadə edərək hər bir unikal formanın bitmapını kodlayır. Sonra o, hər bir formanın səhifədə göründüyü yerləri kodlayır. Həm JB2, həm də IW44, Şennon limitinin bir neçə faizi daxilində qalan ehtiyatları sıxışdıran ZP-koder adlanan yeni tip adaptiv ikili hesab kodlayıcısına əsaslanır. ZP-koder adaptivdir və digər təxmini ikili arifmetik kodlayıcılardan daha sürətlidir.

## İstinadlar ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)

* [DjVu File Format](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

