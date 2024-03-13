{
  "date": "2019-12-10",
  "keywords": [
"XLTM",
"fayl",
"uzadılması",
"fayl formatı",
"Excel Açıq XML Makro",
"Elektron cədvəl"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "XLTM faylının və onları yarada və aça bilən API-lərin nə olduğunu bilmək üçün fayl formatı bələdçisi.",
  "title": "XLTM faylı nədir?",
  "linktitle": "XLTM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-azm"
}
},
  "lastmod": "2019-12-10"
}

## XLTM faylı nədir?

XLTM fayl uzantısı Microsoft Excel tərəfindən Makro-aktiv şablon faylları kimi yaradılan faylları təmsil edir. XLTM faylları struktur baxımından [XLTX](/spreadsheet/xltx/) faylına bənzəyir, lakin sonrakılar makrolarla şablon faylları yaratmağı dəstəkləmir. Belə şablon faylları oxşar XLSX fayllarının yaradılmasını asanlaşdırmaq üçün makroslarla yanaşı düzümü, formatlaşdırmanı və digər parametrləri yaratmaq və qurmaq üçün istifadə olunur.

## Qısa tarix ##

2000-ci ilin əvvəllərində Microsoft **Office Open XML** standartına uyğunlaşmaq üçün dəyişikliyə getməyə qərar verdi. Bu yeni Standarta uyğun olaraq müxtəlif növ sənədlər genişləndirmələrində X əlavə edilməklə müəyyən edilmişdir, burada X XML üçündir. 2007-ci ilə qədər bu yeni fayl formatı Office 2007-nin bir hissəsi oldu və Microsoft Office-in yeni versiyalarında da davam etdirilir. Yeni fayl növü kiçik fayl ölçüləri, daha az korrupsiya dəyişiklikləri və yaxşı formatlaşdırılmış şəkillərin təqdim edilməsi kimi üstünlükləri əlavə etdi.

## XLTM Fayl Formatının Xüsusiyyətləri ##

XLTM faylları Office OpenXML fayl formatına əsaslanır və faylın ölçüsünü azaltmaq üçün XML və [ZIP](/compression/zip/) istifadə edir. Bunlar faylı iki dəfə klikləməklə Microsoft Excel ilə açıla bilər. XLTM fayl formatında faylların təşkili faylın adını ZIP olaraq dəyişdirərək və sonra məzmununu diskə çıxarmaqla müşahidə edilə bilər.

### [Məzmun_Növləri].xml ###

Bu, zip çıxarıldıqda baza səviyyəsində tapılan yeganə fayldır. Paketdəki hissələrin məzmun növlərini sadalayır. Paketə daxil olan XML fayllarına bütün istinadlar bu XML faylında istinad edilir.

### \_rels (Qovluq) ###

Bu, paket səviyyəli əlaqələri saxlayan tək XML faylı olan Əlaqələr qovluğudur. Xltx fayllarının əsas hissələrinə keçidlər bu faylda URI kimi var. Bu URI-lər hər bir əsas hissənin paketlə əlaqə növünü müəyyən edir. Bura xl/workbook.xml kimi yerləşən əsas ofis sənədi ilə əlaqə və əsas və genişləndirilmiş xüsusiyyətlər kimi docProps daxilindəki digər hissələr daxildir.

### docProps ###

Bu qovluq ümumi sənəd xüsusiyyətlərini ehtiva edir. Bunlara əsas xassələr dəsti, genişləndirilmiş və ya tətbiqə xas xassələr dəsti və sənədin kiçik təsvirinə baxış daxildir. Boş iş kitabında bu qovluqda iki fayl var, yəni app.xml və core.xml. core.xml-də müəllif, yaradılan və saxlanılan və dəyişdirilmiş tarix kimi məlumatlar var. App.xml faylın məzmunu haqqında məlumat ehtiva edir.

### xl (Qovluq) ###

Bu, iş kitabının məzmunu ilə bağlı bütün təfərrüatları ehtiva edən əsas qovluqdur. Varsayılan olaraq, aşağıdakı qovluqlara malikdir:

* \_rels

* mövzu

* iş vərəqləri


və aşağıdakı xml faylları:

* styles.xml

* workbook.xml


## İstinadlar ##

* [MS-XLSX Fayl Format](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


