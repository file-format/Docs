{
  "date": "2019-12-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "_XLSX faylının və _XLSX fayllarını yarada və aça bilən API-lərin nə olduğunu bilmək üçün fayl formatı bələdçisi.",
  "title": "_XLSX faylı nədir?",
  "linktitle": "_XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-_xls-azx"
}
},
  "lastmod": "2021-11-22"
}

## _XLSX faylı nədir?

.\_xlsx uzantısı olan fayl əslində başqa proqram tərəfindən adı dəyişdirilən [XLSX](/spreadsheet/xlsx/) fayldır. Bu, müəyyən hallarda fayl adında . fayl adının sonunda. \_XLSX faylları Microsoft Excel-də XLSX fayllarına bənzər şəkildə yenidən adlarını .xlsx uzantısına dəyişdirməklə açıla bilər.

## _XLSX Fayl Format - Ətraflı məlumat

The _XLSX files are no different than the XLSX files and use the Open XML standard adopted by Microsoft back in 2000. XLSX-dən əvvəl [XLS](/spreadsheet/xls/) sənədləri ikili formatda saxlamaq üçün Excel cədvəlləri ilə işləmək üçün istifadə edilən əsas fayl formatı idi. Bu yeni XML əsaslı fayl formatı kiçik fayl ölçüləri, faylın korlanmasına qarşı müqavimət və yaxşı formatlaşdırılmış şəkillər təqdimatı kimi üstünlüklərə malikdir. Bu yeni XML əsaslı fayl formatı Office 2007-nin bir hissəsi oldu və Microsoft-un yeni versiyalarında da həyata keçirilir.

## \_XLSX Fayl Formatının Xüsusiyyətləri

\_XLSX faylı adı dəyişdirilmiş XLSX faylı olduğundan, orijinal fayl ilə eyni xüsusiyyətlərə malikdir. Bu, sadəcə olaraq [ZIP](/compression/zip/) arxiv faylı formatına əsaslanan arxiv faylıdır. Bu arxivin məzmununu görmək istəyirsinizsə, sadəcə olaraq faylın adını .zip uzantısına dəyişdirin və bu Excel iş kitabının tərkib fayllarına baxmaq üçün onu çıxarın. Boş iş dəftəri öz fayllarına çıxarıldıqda aşağıdakı tərkib fayl və qovluqlara malikdir.

### [Məzmun_Növləri].xml

Bu, zip çıxarıldıqda baza səviyyəsində tapılan yeganə fayldır. Paketdəki hissələrin məzmun növlərini sadalayır. Paketə daxil olan XML fayllarına bütün istinadlar bu XML faylında istinad edilir.

### \_rels (Qovluq)

Bu, paket səviyyəli əlaqələri saxlayan tək XML faylı olan Əlaqələr qovluğudur. Xlsx fayllarının əsas hissələrinə keçidlər bu faylda URI kimi var. Bu URI-lər hər bir əsas hissənin paketlə əlaqə növünü müəyyən edir. Bura xl/workbook.xml kimi yerləşən əsas ofis sənədi ilə əlaqə və əsas və genişləndirilmiş xüsusiyyətlər kimi docProps daxilindəki digər hissələr daxildir.

### docProps

Bu qovluq ümumi sənəd xüsusiyyətlərini ehtiva edir. Bunlara əsas xassələr dəsti, genişləndirilmiş və ya tətbiqə xas xüsusiyyətlər dəsti və sənədin miniatür təsviri daxildir. Boş iş kitabında bu qovluqda iki fayl var, yəni app.xml və core.xml. core.xml-də müəllif, yaradılan və saxlanılan və dəyişdirilmiş tarix kimi məlumatlar var. App.xml faylın məzmunu haqqında məlumat ehtiva edir.

### xl (Qovluq)

Bu, iş kitabının məzmunu ilə bağlı bütün təfərrüatları ehtiva edən əsas qovluqdur. Varsayılan olaraq, aşağıdakı qovluqlara malikdir:

* \_rels

* mövzu

* iş vərəqləri


və aşağıdakı xml faylları:

* styles.xml

* workbook.xml


## İstinadlar

* [MS-XLSX - .xlsx Fayl Format](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


