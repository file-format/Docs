{
  "date": "2019-12-10",
  "keywords": [
"XLTX",
"fayl",
"uzadılması",
"fayl formatı",
"Excel Açıq XML",
"Elektron cədvəl"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "XLTX faylının və onları yarada və aça bilən API-lərin nə olduğunu bilmək üçün fayl formatı bələdçisi.",
  "title": "XLTX faylı nədir?",
  "linktitle": "XLTX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-azx"
}
},
  "lastmod": "2019-12-10"
}

## XLTX faylı nədir?

.xltx uzantısı olan fayllar Office OpenXML fayl formatı spesifikasiyalarına əsaslanan Microsoft Excel Şablon fayllarını təmsil edir. O, XLTX faylında göstərildiyi kimi eyni parametrləri nümayiş etdirən [XLSX](/spreadsheet/xlsx/) faylları yaratmaq üçün istifadə edilə bilən standart şablon faylı yaratmaq üçün istifadə olunur.

## Qısa tarix

2000-ci ilin əvvəlində Microsoft **Office Open XML** standartına uyğunlaşmaq üçün dəyişikliyə getməyə qərar verdi. Bu yeni Standarta uyğun olaraq müxtəlif növ sənədlər genişləndirmələrində X əlavə edilməklə müəyyən edilmişdir, burada X XML üçündir. 2007-ci ilə qədər bu yeni fayl formatı Office 2007-nin bir hissəsi oldu və Microsoft Office-in yeni versiyalarında da davam etdirilir. Yeni fayl növü kiçik fayl ölçüləri, daha az korrupsiya dəyişiklikləri və yaxşı formatlaşdırılmış şəkillərin təqdim edilməsi kimi üstünlükləri əlavə etdi.

## XLTX Fayl Formatının Xüsusiyyətləri

XLTX faylları Office OpenXML fayl formatına əsaslanır və faylın ölçüsünü azaltmaq üçün XML və [ZIP](/compression/zip/) istifadə edir. O, ikili XLT fayl formatını əvəz etmək üçün Microsoft Office 2007-nin buraxılışı ilə yaradılmışdır. XLTX kimi, XLT fayl formatı Microsoft Excel 2003 və 2007-dən istifadə edərək [XLS](/spreadsheet/xls/) faylları yaratmaq üçün istifadə edilə bilər. Bunlar faylı iki dəfə klikləməklə Microsoft Excel ilə açıla bilər. XLTX fayl formatında faylların təşkili, faylın adını ZIP olaraq dəyişdirərək və sonra məzmununu diskə çıxarmaqla müşahidə edilə bilər.

### [Məzmun_Növləri].xml ###

Bu, zip çıxarıldıqda baza səviyyəsində tapılan yeganə fayldır. Paketdəki hissələrin məzmun növlərini sadalayır. Paketə daxil olan XML fayllarına bütün istinadlar bu XML faylında istinad edilir.

### \_rels (Qovluq) ###

Bu, paket səviyyəli əlaqələri saxlayan tək XML faylı olan Əlaqələr qovluğudur. Xltx fayllarının əsas hissələrinə keçidlər bu faylda URI kimi var. Bu URI-lər hər bir əsas hissənin paketlə əlaqə növünü müəyyən edir. Bura xl/workbook.xml kimi yerləşən əsas ofis sənədi ilə əlaqə və əsas və genişləndirilmiş xüsusiyyətlər kimi docProps daxilindəki digər hissələr daxildir.

### docProps ###

Bu qovluq ümumi sənəd xüsusiyyətlərini ehtiva edir. Bunlara əsas xassələr dəsti, genişləndirilmiş və ya tətbiqə xas xüsusiyyətlər dəsti və sənədin miniatür təsviri daxildir. Boş iş kitabında bu qovluqda iki fayl var, yəni app.xml və core.xml. core.xml-də müəllif, yaradılan və saxlanılan və dəyişdirilmiş tarix kimi məlumatlar var. App.xml faylın məzmunu haqqında məlumat ehtiva edir.

### xl (Qovluq) ###

Bu, iş kitabının məzmunu ilə bağlı bütün təfərrüatları ehtiva edən əsas qovluqdur. Varsayılan olaraq, aşağıdakı qovluqlara malikdir:

* \_rels

* mövzu

* iş vərəqləri


və aşağıdakı xml faylları:

* styles.xml

* workbook.xml


## İstinadlar ##

* [[MS-XLSX] - .Xlsx Fayl Formatı](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


