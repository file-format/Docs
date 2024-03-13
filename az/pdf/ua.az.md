{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/UA Fayl Formatı",
  "description": "PDF/UA fayl formatı və PDF/UA faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "PDF/UA",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-u-aza"
}
},
  "lastmod": "2019-09-10"
}

# PDF/UA faylı nədir? #

PDF/UA 2012-ci ilin avqustunda [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) adı ilə nəşr edilib və bu günə qədər hamı üçün əlçatan olan PDF sənədləri üçün tələblər toplusunun ilk tam tərifidir. Universal əlçatan termini [PDF](/pdf/) sənədində olan məlumatın ümumilikdə hər kəs və xüsusən də əlilliyi olan insanlar üçün bərabər və müstəqil şəkildə əlçatan olması anlayışına istinad edir. PDF/UA standartının tətbiqi PDF məzmununu yaratmaq və oxumaq üçün alətlər və proqramlar yaratmaq üçün əsas addım hesab edilə bilər.

## Fayl Format Tələbləri ##

PDF/UA-nın əsasında bu standartın mahiyyəti kimi çıxış edən müəyyən tələblər var. Əslində, bunlar PDF-lərin etiketlənməsinə əsaslanır, yəni bütün PDF/UA sənədləri düzgün etiketlənməlidir. O, həmçinin teqlərin semantik cəhətdən uyğun və məntiqi qaydada olmasını tələb edir. Bu, PDF/UA spesifikasiyası ilə yaradılmış son sənədin daha etibarlı və əlçatan olmasını təmin edir. Bu, PDF müəlliflərini bütün bu tələblər haqqında hər şeyi bilməli olduqlarını sual altına qoya bilər? Xoşbəxtlikdən, bu, belə deyil, çünki PDF/UA uyğunluq alətləri PDF-ə əlçatanlığı əlavə etmək və qorumaq üçün məsuliyyət daşıyır.

PDF/UA üçün fayl formatı tələbləri aşağıdakı kimidir.

* Məzmun iki yoldan biri ilə təsnif edilir: mənalı məzmun və dekorativ səhifə elementləri kimi artefaktlar. Bütün mənalı məzmun etiketlənməli və sənəd daxilindəki bütün teqlərin struktur ağacına inteqrasiya edilməlidir. Artefaktlar isə yalnız belə qeyd edilməlidir.

* Mənalı məzmun teqlərlə qeyd edilməli və sənəddəki digər teqlərlə birlikdə tam struktur ağacı yaratmalıdır.

* Mənalı məzmun müvafiq semantik etiketlərlə qeyd edilməlidir.

* Sənəd teqləri ilə yaradılmış struktur ağacı sənədin məntiqi oxunma qaydasını əks etdirməlidir.

* Yalnız PDF 1.7-də müəyyən edilmiş standart etiketlərdən istifadə edilə bilər; hər hansı digər teqlər istifadə olunarsa, rol təyinatı girişi hər birinin hansı standart teqi təmsil etdiyini qeyd etməlidir.

* Məlumat yalnız vizual vasitələrdən istifadə etməklə ötürülə bilməz (məsələn, kontrast, rəng və ya səhifədəki mövqe).

* İstər JavaScript tərəfindən idarə olunan effektlər, istərsə də PDF-ə daxil edilmiş hər hansı videoların bir hissəsi kimi heç bir titrəmə, yanıb-sönən və ya yanıb-sönən məzmuna icazə verilmir.

* Sənədin başlığı verilməlidir və sənəd elə qurulmalıdır ki, pəncərə başlığında başlıq (fayl adı deyil) görünsün.

* Bütün məzmunun dili qeyd edilməli və dil dəyişiklikləri açıq şəkildə belə qeyd edilməlidir.


## PDF/UA Uyğunluğu ##

PDF/UA standartı məzmun, oxucular və köməkçi texnologiya üçün spesifikasiyaları müəyyən edir. Bu üç aspekt sənədin məzmununa əsasən bir-biri ilə əlaqələndirilir. Bunların hər biri üçün uyğunluq tələbləri aşağıda qeyd edildiyi kimidir.

## Uyğun fayllar ##

Files conforming to PDF/UA standard should contain features that are valid as per the [PDF 1.7 specifications](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). However, features that are forbidden by PDF/UA specifically should be excluded.

## Uyğun Oxucular ##

Uyğun oxucu PDF 1.7 spesifikasiyaları ilə yazılmış qaydalara əməl etməlidir. Xüsusilə, o, dəstəkləməlidir:

* əlçatanlıq üçün göstərilən bütün teqlər, atributlar və əsas dəyərlər. O, həmçinin rəqəmsal imzaları, annotasiyaları və Əlavə Məzmunu emal etmək və təmsil etmək qabiliyyətinə malik olmalıdır.

* rəqəmsal imzaları, annotasiyaları və Əlavə Məzmunu emal edin və təmsil edin

* müxtəlif vasitələrlə sənəddə naviqasiya edin


## Uyğun Yardımçı Texnologiya ##

Uyğun köməkçi texnologiya PDF/UA xüsusiyyətlərini dəstəkləmək üçün bağlıdır. Bunlara, məsələn, məzmunun və oxucunun xüsusiyyətləri daxildir və səhifə etiketləri, sənəd strukturu və ya kontur üzrə naviqasiyaya imkan verməlidir. O, həmçinin istifadəçiyə standart naviqasiya miqyasını ləğv etməyə imkan verməlidir.

## İstinadlar ##

* [PDF/UA - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/PDF/UA)

* [Qısaca PDF/UA](https://pdfa.org/pdfua-in-a-nutshell/)


