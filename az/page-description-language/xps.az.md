{
  "date": "2019-10-11",
  "keywords": [
"XPS",
"XML Kağız Xüsusiyyətləri",
"Fayl",
"Uzatma",
"Fayl Format",
"EMF",
"PDF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPS - Səhifə Düzeni Fayl Format",
  "description": "XPS faylları yarada və aça bilən XPS fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "XPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xp-azs"
}
},
  "lastmod": "2021-04-23"
}

## XPS faylı nədir?

XPS faylı Microsoft tərəfindən yaradılmış XML Kağız Xüsusiyyətlərinə əsaslanan səhifə tərtibatı fayllarını təmsil edir. O, EMF fayl formatının əvəzi kimi hazırlanmışdır və [PDF](/pdf/) fayl formatına bənzəyir, lakin sənədin tərtibatı, görünüşü və çap məlumatında XML-dən istifadə edir. Əslində, XPS-in PDF cəhdi olduğunu söyləmək daha doğrudur, lakin bir çox səbəblərə görə PDF-ə məxsus olduğu üçün kifayət qədər populyarlıq qazana bilmədi. Microsoft Windows 7-dən başlayaraq XPS fayllarının yaradılması üçün standart olaraq XPS Sənəd Yazıçısını təmin edir. Sənədi çap edərkən printer kimi Microsoft XPS Document Writer seçilərək XPS faylları yaradıla bilər.

XPS izləyiciləri Windows Vista, Windows 7, Windows 8 və Internet Explorer 6 və ya daha sonrakı versiyaların bir hissəsi kimi inteqrasiya olunur. XPS faylları yaradıldıqdan sonra yalnız oxunur. Bu, istifadəçinin sənədin həqiqiliyi üçün XPS kimi göndərilən qəbul edilmiş sənədlərə inamını artırır. XPS sənədi orijinal sənəddən çevrilmiş bir və ya daha çox səhifədən ibarət ola bilər.

## Qısa tarix ##

Microsoft XPS spesifikasiyasını Ecma International-a təqdim etdi. 2007-ci ilin iyun ayında OpenXPS Kağız Spesifikasiyalarına əsaslanan standart hazırlamaq üçün Ecma Texniki Komitəsi 46 (TC46) yaradılmışdır. Ecma International 2009-cu ilin iyun ayında 97-ci Baş Assambleyada Ecma Standartını (ECMA-388) [XPS specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) təsdiqlədi.

## XPS Fayl Format ##

XPS formatı sənədin kompozisiyasını və hər bir səhifənin vizual görünüşünü, həmçinin sənədin nümayişi və ya çapı üçün göstərmə qaydalarını müəyyən edən XML işarəsindən ibarətdir. İstənilən sistemdə sənədi yenidən yaratmaq üçün bütün məlumatları özündə saxlayır ki, bu da onu həmin sistemdə mövcud olan resurslardan müstəqil edir. Format mahiyyətcə ZIP arxividir və fayl uzantısının adını ZIP olaraq dəyişdirsəniz, sənəd məlumatlarını ehtiva edən tərkib fayllarını görəcəksiniz. Bu sənədlərə aşağıdakılar daxildir:

* sənəd səhifəsi faylları (.fpage) - Sənəd məzmunu və sənəd formatı parametrlərini ehtiva edir. XPS sənədindəki hər səhifədə bir FPAGE faylı var.

* sənəd parametrləri faylı (.fdoc) - XPS arxivinə daxil edilmiş parametrləri saxlayır.

* sənəd fraqment faylları (.frag) - Faktiki XPS faylı üçün parametrləri müəyyən edir və sənəddəki hər səhifənin öz .frag faylı var.


{{< figure src="../XPS-1.png" alt="XPS fayl formatı" >}}

Bu fayllar sənədin məzmununu elə saxlayır ki, məsələn, kiminsə maşınında eyni şriftlər quraşdırılmayıbsa, XPS görüntüləyicisi yenə də həmin orijinal şriftləri göstərəcək. Bu, hər biri üçün XML işarələmə faylının daxil edilməsini nəzərdə tutur:

* Səhifə

* Mətn

* Daxili şriftlər

* Raster şəkillər

* 2D vektor qrafikası

* Rəqəmsal hüquqların idarə edilməsi


XPS Sənəd formatına hər biri sənəddə müəyyən bir məqsədi yerinə yetirən dəqiq müəyyən edilmiş hissələr və əlaqələr dəsti daxildir. Format həmçinin rəqəmsal imzalar, miniatürlər və interleaving daxil olmaqla paket xüsusiyyətlərini genişləndirir.

Tipik bir XPS sənədi aşağıdakı kimi görünür və XPS fayl formatının spesifikasiyası işığında təhlil edilə bilər.

{{< figure src="../XPS-2.png" alt="XPS fayl formatı" >}}


## İstinadlar ##

* [XPS Fayl Formatının Xüsusiyyətləri](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)

* [XPS - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)


