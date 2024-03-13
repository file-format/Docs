{
  "date": "2019-12-16",
  "keywords": [
"XLS",
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
  "description": "XLS faylının və onları yarada və aça bilən API-lərin nə olduğunu bilmək üçün fayl formatı bələdçisi.",
  "title": "XLS fayl formatı nədir? Fayl Format Mütəxəssislərindən öyrənin!",
  "linktitle": "XLS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-azs"
}
},
  "lastmod": "2019-12-16"
}

## XLS faylı nədir?

Files with XLS extension represent Excel Binary File Format. Such files can be created by Microsoft Excel as well as other similar spreadsheet programs such as OpenOffice Calc or Apple Numbers. File saved by Excel is known as Workbook where each workbook can have one or more worksheets. Data is stored and displayed to users in table format in worksheet and can span numeric values, text data, formulas, external data connections, images, and charts. Applications like Microsoft Excel lets you export workbook data to several different formats including [PDF](/pdf/), [CSV](/spreadsheet/csv/), [XLSX](/spreadsheet/xlsx/), [TXT](/word-processing/txt/), [HTML](/web/html/), [XPS](/page-description-language/xps/), and several others. The XLS file format was replaced with a more open and structured format, XLSX, with the release of Microsoft Excel 2007. The latest versions still provide support for creating and reading XLS files, though XLSX is the first choice of use now.

## Qısa tarix

XLS was created by Microsoft for use with Microsoft Excel and is also known as Binary Interchange File Format (BIFF). This file type was introduced for the first time by making it part of Excel for Windows in 1987. XLS file format specifications were made public for the first in June 2008 as Revision 1. After that, the specifications were continuously updated and the latest revision available is as of August 2018 that is marked as Revision 8.0. A brief history of different versions of XLS file format is as follow:

* Version 7.0 (released with office 95):  This version of excel was the most robust and faster among all the versions and internal stream rewrites were updated to 32 bits.
* Versiya 8 (ofis 97 ilə buraxıldı): VBA standart dil kimi təqdim edildi və çıxarılan təbii dil etiketləri ilk dəfə olaraq bu versiyaya daxil edildi. O, həmçinin ilk dəfə bir kağız klipi ofis köməkçisini təqdim etdi.

* Versiya 9 (office 2000 ilə buraxılmışdır): Versiya 9-da yalnız kiçik dəyişikliklər edildi, burada kağız klipi ofis köməkçisi əvvəllər mümkün olmayan bir neçə obyekti eyni vaxtda saxlaya bildi.

* Versiya 10 (Office XP ilə buraxılmışdır): Bu versiyada nəzərəçarpacaq təkmilləşmə yox idi.

* Version 11 (Released with office 2003): Major update in version 11, excel 2003 was the introduction of new tables.

## XLS Fayl Formatının Xüsusiyyətləri ##

Data Microsoft tərəfindən [MS-CFB]. Data is stored in the compound file by using storages, streams, and substreams that contain information about the content and structure of a workbook, including workbook data such as worksheet definitions. Each stream or substream contains a series of binary records. Each binary record contains zero or more structured fields that contain the workbook data. This section gives a brief overview of XLS File Structure, but for detailed file format specifications, one must consult the [XLS File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx) sənədində təsvir olunduğu kimi mürəkkəb fayl şəklində ikili axınlar kimi XLS faylında yerləşdirilir.

#### Axın və alt axın ####

İş kitabı iş kitabı axını ilə təmsil olunur. İş kitabındakı hər bir iş vərəqi Substreams ilə təmsil olunur. Bundan əlavə, Qlobal Alt axını izləyən Dialoq vərəqinin alt axını, Makro vərəq alt axını və ya Dialoq vərəqinin alt axını var. İş kitabı məlumatlarını ehtiva edən hər ikili axın və ya alt axın ikili qeydlər seriyası kimi yazılmalıdır.

#### Qeyd ####

İş kitabındakı xüsusiyyətlər haqqında məlumat dəyişən uzunluqlu bayt ardıcıllığı olan qeyd kimi saxlanılır. İkili qeyd aşağıdakı üç komponentdən ibarətdir:

**Qeyd növü:** Qeyd növü iki baytlıq işarəsiz tam ədəddir və qeyd tərəfindən hansı növ məlumatın göstərildiyini və bu qeyd üçün xüsusi qeyd məlumatlarının strukturunun necə sıralandığını və strukturlaşdırıldığını müəyyən edir. Qeyd növü dəyərləri MÜTLƏQ Qeyd Sadalanmasından bir dəyər olmalıdır (bölmə 2.3) və ya qeyd gələcək qeyd arxitekturasından istifadə etməlidir (bölmə 2.1.6).

**Qeyd ölçüsü**: Qeydin ölçüsü qeyd məlumatının ümumi ölçüsünü təyin edən baytların sayını təyin edən iki baytlıq işarəsiz tam ədəddir. Qeydin ölçüsü 0-dan böyük və ya ona bərabər olmalıdır və 8224-dən kiçik və ya ona bərabər olmalıdır.

**Qeyd Məlumatı:** Qeyd məlumatı komponenti xüsusi qeyd növünə uyğun gələn və qeydin qalan hissəsini təşkil edən sahələri ehtiva edir. Verilmiş qeyd növü üçün sahələrin sırası və strukturu həmin qeyd növü üçün müvafiq bölmədə müəyyən edilir. Qeyd məlumatı komponentinin ölçüsü qeyd ölçüsünə bərabər olmalıdır. Qeyd məlumatı komponentindəki sahələr sadə dəyərləri, dəyərlər massivlərini, bir neçə sahənin strukturlarını, sahələrin massivlərini və strukturların massivlərini ehtiva edə bilər.

#### Hüceyrə Cədvəli ####

Hüceyrələr mətn, düsturlar və ədədi məlumatlar kimi iş kitabının məzmununu saxlayan iş kitabının əsas bloklarıdır. Hüceyrələr Hüceyrə Cədvəli adlanan məlumat strukturu vasitəsilə saxlanılan məlumatların qeydini saxlayır. Hüceyrə Cədvəli özü spesifikasiyalar sənədində müəyyən edilmiş CELLTABLE qaydalarına uyğun olan qeydlər ardıcıllığında saxlanılır. O, sıraların sıra bloklarında düzüldüyü bir sıra sıra bloklarından ibarətdir. Hər bir sətir bloku məlumatı ehtiva edən birinci cərgədən verilənləri ehtiva edən sonuncu sıraya qədər sətirləri ehtiva edir.

Məlumat və ya sıra formatı hər bir sıra bloku üçün Satır qeydində saxlanılır. Məlumat və ya fərdi hüceyrə formatını ehtiva edən hər bir xana qeyd ilə təmsil olunur. Hüceyrə ilə əlaqəli formatlaşdırma fərdi xana formatlaşdırmasından, sıra formatlaşdırmasından, sütun formatından və ya standart xana formatından əldə edilə bilər. Formatlaşdırma üçün prioritet sırası ən yüksək prioritetə malik fərdi xana formatlaşdırma, ardınca sıra formatlaşdırma, sonra sütun formatlaşdırma, sonra isə standart xana formatıdır. Məlumatları olmayan və fərdi formatlaşdırma olmayan xanalar saxlanmır.

#### Formulalar ####

Formula birlikdə yeni dəyər yaradan xanadakı dəyərlər, xana istinadları, adlar, funksiyalar və ya operatorların ardıcıllığıdır. Düsturlar parsed ifadələr kimi tanınan tokenləşdirilmiş təqdimatda saxlanılır. Təhlil edilmiş ifadə ekran və istifadəçi redaktəsi üçün icra zamanı mətn formuluna çevrilir. Hüceyrə düsturları Formula qeydi ilə müəyyən edilir. Massiv düsturları Array qeydi ilə müəyyən edilir. Paylaşılan düsturlar ShrFmla qeydi ilə müəyyən edilir.

#### Qrafiklər ####

Diaqram vərəqi bir diaqramı, məlumatları və ya vizual formada məlumat dəstləri arasındakı əlaqələri göstərən qrafiki və diaqram məlumatlarının keşini, diaqram məlumatlarında istifadə olunan məlumatların yerli nüsxəsini və ya xarici əlaqələrə keçidləri müəyyən edir. məlumat mənbələri pozulur. Diaqram bir və ya iki oxlu qrupları, diaqram məlumatlarının əks olunduğu oxlar dəstini və diaqramda göstərilən sıralar, trend xətləri və xəta zolağı dəstini müəyyən edir. Hər bir ox qrupu məlumatları göstərmək üçün istifadə olunan vizuallaşdırma növünü təyin edən bir-dörd diaqram qrupunu müəyyən edir. Hər bir seriya, trend xətti və xəta zolağı əlaqəli olduğu diaqram qrupunu müəyyən edir.

#### Metadata ####

Metadata müəyyən bir xana və ya onun məzmunu ilə əlaqəli əlavə məlumatdır. Metadata yalnız gələcək genişlənmə məqsədləri üçün BIFF8-də qeyd olunur.

#### Pivot Cədvəllər ####

Pivot Cədvəl həmin məlumatların paylanmasına ümumi baxış əldə etmək üçün mənbə məlumatlarının ümumiləşdirilməsi mexanizmidir. Pivot Cədvəldə mənbə məlumatlarının müvafiq sütunları məlumatları ümumiləşdirmək üçün istifadə edilə bilən sahələrə çevrilir. Pivot Cədvəlin mənbə məlumatları OLAP mənbə məlumatı olduqda, OLAP iyerarxiyaları və bəzi digər OLAP obyektləri Pivot Cədvəldə sahələrə çevrilir.
Pivot Cədvəl iki əsas hissədən ibarətdir, PivotCache və PivotTable görünüşü. Tək qeyri-OLAP PivotCache əsasında çoxlu Pivot Cədvəl görünüşü ola bilər.

#### Üslublar ####

Bu icmal vərəqdəki (1) xanalar üçün formatlaşdırma və qoruma məlumatının necə göstərildiyini təsvir edir. Hüceyrə formatı bir neçə xüsusiyyət dəstindən ibarətdir:

* Şrift xüsusiyyətləri (qalın, kursiv, şrift rəngi, şrift ölçüsü və s...)

* Doldurma xüsusiyyətləri (ön plan rəngi, fon rəngi, naxış, gradient və s.)

* Hizalama xassələri (sola, mərkəzə, sağa düzülmə və s...)

* Sərhəd xüsusiyyətləri (sol, sağ, yuxarı, aşağı, qalın və ya nazik, rəng və s...)

* Nömrə formatlaşdırma xüsusiyyətləri (tarix, vaxt, onluq yerlərin sayı və s...)

* Qoruma xüsusiyyətləri (kilidli, gizli və s...)


Bu xüsusiyyətlər, bütövlükdə, müəyyən bir hüceyrənin necə göstərildiyini və çap olunduğunu təsvir edir.

## İstinadlar ##

* [[MS-XLS] - Excel İkili Fayl Format Strukturu](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [[MS-CFB] - Mürəkkəb Fayl İkili Fayl Formatı](https://msdn.microsoft.com/en-us/library/dd942138.aspx)


