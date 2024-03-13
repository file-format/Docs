{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDLC - Hesabat Tərifi Dili Müştəri tərəfi",
  "keywords": [
"rdlc",
"hesabatın tərif dili",
"mkv formatı",
"XSD",
"hesabat tərifi dili müştəri tərəfi"
],
  "description": "SQL Server Reporting Services hesabat tərifinin XML təqdimatı olan RDLC fayl formatı haqqında məlumat əldə edin.",
  "linktitle": "RDLC",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rdl-azc"
}
},
  "lastmod": "2021-03-02"
}

## RDLC faylı nədir? ##

RDLC Report Definition Language Client tərəfini ifadə edir. Əslində bu, Microsoft hesabat texnologiyasından istifadə etməklə yaradılmış hesabat faylının uzantısıdır. Bu faylları yaratmaq üçün Report Designer proqramının SQL Server 2005 versiyası istifadə olunur. Müştəri tərəfindəki **ReportViewer** nəzarəti RDLC hesabatlarını birbaşa icra edə bilər.

## RDL VS RDLC Faylları
|.rdl faylları |.rdlc faylları|
---|---|
|RDL faylları Report Designer-in SQL Server 2005 versiyası tərəfindən yaradılmışdır|RDLC faylları Report Designer-in Visual Studio 2005 versiyası tərəfindən yaradılmışdır|
|SQL Server Reporting Services-də istifadə olunur|Visual Studio-da istifadə olunur|
|Bu uzaq hesabatdır|Bu yerli hesabatdır|
|İşlətmək üçün Reporting Services instansiyasına ehtiyac var|Reporting Services instansiyasına ehtiyac yoxdur|

## Müştəri Hesabatı Tərifi (.rdlc) Fayllarının yaradılması
ReportViewer nəzarəti nəzarətin daxili emal qabiliyyətindən istifadə edərək müştəri hesabatının tərifi (.rdlc) fayllarını işə salmaq üçün istifadə olunur. Müştəri, yerli emal rejimində işlədiyinizi bildirir, tətbiq layihənizdə asanlıqla yaradıla bilər. Hesabat yaratmaq üçün aşağıdakı yanaşmalar var:

- Yeni müştəri hesabatı tərifini (.rdlc) yaratmaq üçün **Hesabat Sihirbazından** istifadə edin.

- Visual Studio istifadə edərək yeni müştəri hesabatı tərifi (.rdlc) faylı yaradın.

- Proqramlı şəkildə hesabat tərifini yaradın.


Siz hesabatı yalnız **ReportViewer** nəzarətində işlətməklə nəzərdən keçirə bilərsiniz. Nəzərə alın ki, siz istənilən vaxt hesabat tərifini aça və redaktə edə, sonra nəticələri yoxlamaq üçün proqramı yarada və ya yerləşdirə bilərsiniz.

## İstinadlar ##

- [Creating Client Report Definition (.rdlc) Files](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

