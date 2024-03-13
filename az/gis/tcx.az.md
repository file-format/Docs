{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TCX Fayl Format - Təlim Mərkəzi XML Faylı",
  "description":"TCX fayl formatı və TCX fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx-az",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## TCX faylı nədir?

TCX (Təlim Mərkəzi XML) faylı fitness cihazları arasında məlumat mübadiləsi üçün istifadə edilən məlumat mübadiləsi formatıdır. 2008-ci ildə Garmin Təlim Mərkəzinin məhsulu ilə təqdim edilmişdir. Ürək döyüntüsü, qaçış tempi, velosiped ritmi, kalorilər və dövrə vaxtı kimi məşq datası TCX faylında [XML](/web/xml/) formatında saxlanılır. Bundan əlavə, məşq treki haqqında ümumi məlumat da TCX faylına daxil edilmişdir. TCX faylları Garmin idman geyilə bilən cihazları ilə yaradılmış [FIT](/gis/fit/) fayllarına bənzəyir.

## TCX fayl formatı - Ətraflı məlumat

TCX faylları diskdə XML faylları kimi saxlanılır, hər bir qeyd fəaliyyət kimi saxlanılır. Fəaliyyət vaxt, dövrə vaxtı, İd, ürək döyüntüsü, intensivlik, kadans və {{HYPERLINK1-ə bənzər ən uzun mövqe üçün vaxt möhürü ilə birlikdə mövqe cütlərini ehtiva edən trek məlumatı kimi məşqin bütün datasından ibarətdir. }} fayl.

### TCX Fayl Format Versiyaları

Garmin tərəfindən idarə olunan öz XML sxemləri ilə bu formatın iki versiyası var. Onlardan bir neçəsi aşağıdakılardır:

 * https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
 * https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
 * https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX Məlumat Protokolu

A swift version of TCX XML format is available on Github as [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## İstinadlar ##

* [Tədris Mərkəzi XML](https://en.wikipedia.org/wiki/Training_Center_XML)

* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)


