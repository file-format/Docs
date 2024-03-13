{
  "date": "2019-12-10",
  "keywords": [
"XLSX",
"fayl",
"uzadılması",
"fayl formatı",
"Excel",
"Elektron cədvəl"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "XLSX faylı və XLSX fayllarını yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "title": "XLSX fayl formatı - XLSX faylı nədir?",
  "linktitle": "XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-azx"
}
},
  "lastmod": "2019-12-10"
}

## XLSX faylı nədir?

**XLSX** is well-known format for Microsoft Excel documents that was introduced by Microsoft with the release of Microsoft Office 2007. OOXML standartı ECMA-376-nın [Part 2](https://www.ecma-international.org/publications-and-standards/standards/ecma-376/)-də qeyd edildiyi kimi Açıq Qablaşdırma Konvensiyalarına uyğun təşkil edilmiş struktura əsaslanaraq, yeni format bir sıra XML fayllarını ehtiva edən zip paketidir. Əsas struktur və fayllar sadəcə .xlsx faylını açmaqla yoxlana bilər.

## XLSX Fayl Formatının Qısa Tarixi

XLSX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. XLSX-dən əvvəl istifadə edilən ümumi fayl formatı [XLS](/spreadsheet/xls/) idi ki, bu da xalis ikili fayl formatı idi. Yeni fayl növü kiçik fayl ölçüləri, daha az korrupsiya dəyişiklikləri və yaxşı formatlaşdırılmış şəkillərin təqdim edilməsi üstünlüklərini əlavə etdi. 2000-ci ilin əvvəllərində Microsoft **Office Open XML** standartına uyğunlaşmaq üçün dəyişikliyə getməyə qərar verdi. 2007-ci ilə qədər bu yeni fayl formatı Office 2007-nin bir hissəsi oldu və Microsoft Office-in yeni versiyalarında da davam etdirilir.

## XLSX Fayl Formatının Xüsusiyyətləri

Rəsmi [XLSX file format specifications](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) Microsoft-dan onlayn mövcuddur. XLSX faylının içərisində nə olduğunu görmək üçün genişləndirilməsini dəyişdirərək onun adını [ZIP](/compression/zip/) faylına dəyişdirin və sonra bu Excel iş kitabının tərkib fayllarına baxmaq üçün onu çıxarın. Boş iş dəftəri öz fayllarına çıxarıldıqda aşağıdakı tərkib fayl və qovluqlara malikdir.

### [Məzmun_Növləri].xml ###

Bu, zip çıxarıldıqda baza səviyyəsində tapılan yeganə fayldır. Paketdəki hissələrin məzmun növlərini sadalayır. Paketə daxil olan XML fayllarına bütün istinadlar bu XML faylında istinad edilir.

### \_rels (Qovluq) ###

Bu, paket səviyyəli əlaqələri saxlayan tək XML faylı olan Əlaqələr qovluğudur. Xlsx fayllarının əsas hissələrinə keçidlər bu faylda URI kimi var. Bu URI-lər hər bir əsas hissənin paketlə əlaqə növünü müəyyən edir. Bura xl/workbook.xml kimi yerləşən əsas ofis sənədi ilə əlaqə və əsas və genişləndirilmiş xüsusiyyətlər kimi docProps daxilindəki digər hissələr daxildir.

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


## XLSX Format Nümunəsi ##


İş kitabında olan hər bir Excel iş vərəqi üçün bir XML faylı var. Bu XML fayllarını xl/worksheets qovluğunda tapa bilərsiniz. İş vərəqindəki bütün məlumatlar XML faylında müxtəlif bölmələrdə təşkil edilir. Aşağıdakı şəkildə göstərilən iş kitabından nümunə iş vərəqini nəzərdən keçirək.

{{< figure src="../XLSX file format.png" alt="XLSX fayl formatı" >}}

Göründüyü kimi, bu iş vərəqi A1-dən B2-yə qədər xanalardakı məzmunu və təsviri ehtiva edir. Bundan əlavə, G13 xanası hazırda iş vərəqindəki aktiv xanadır. İndi bu məlumatın XML faylında necə təmsil olunduğunu görmək üçün xl/worksheets/sheet1.xml faylını nəzərdən keçirək. Bu XML faylının məzmunu aşağıda göstərildiyi kimidir.

{{< figure src="../XLSX File Format Details.png" alt="XPS fayl formatı" >}}

1. Nişanda mövzu rəngi tətbiq olunub. XML faylında etiketlə qeyd olunur<tabColor> mövzu id-dən sonra.
1. TabSelected dəyəri 1-ə təyin edilib və bu, seçilmiş vərəq olduğunu göstərir
1. Yuxarıdakı ilk şəkildə göründüyü kimi, iş vərəqindəki G13 xanası XML faylında da qeyd olunan aktiv xanadır.
1. SheetData nişanı iş vərəqində olan məlumatları təmsil edir. Bununla belə, iş vərəqinin orijinal məzmununun bu bölmənin heç bir yerində olmadığını görə bilərsiniz. Bunun səbəbi mətnin dolayı yolla sharedStrings XML vərəqindən istinad edilməsidir. Bu əlaqə hər bir mətnin yalnız bir dəfə saxlanmasını və yerə qənaət etmək üçün yenidən istinad edilə biləcəyini təmin edir.
1. Göründüyü kimi şəkilə istinad id rId2 istinad edilir

## töhfə verin

XLSX və ya Spreadsheet fayl formatları haqqında nəsə paylaşmalısan? Nəticələrinizi [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet) bölməsində yerləşdirə bilərsiniz.

## İstinadlar

* [[MS-XLSX] - XLSX Fayl Format](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


