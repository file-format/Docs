{
  "date": "2020-11-11",
  "keywords": [
"DTSX",
"uzadılması",
"fayl",
"fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"Verilənlər Bazasının Faylları"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "DTSX faylları yarada və aça bilən DTSX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "DTSX Fayl Format - SQL Server DTS Parametrlər Faylı",
  "linktitle": "DTSX",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dts-azx"
}
},
  "lastmod": "2020-08-12"
}

## DTSX faylı nədir?

.dtsx (Data Transformation Services Package XML) uzantısına malik fayl, verilənlərin bir verilənlər bazasından digərinə ötürülməsi üçün verilənlərin miqrasiyası addımlarına/qaydalarına istinad etmək üçün Microsoft SQL tərəfindən istifadə edilən Data Transformation Services (DTS) faylıdır. Buraya ilkin və təyinat nöqtələri arasında məlumat ötürülməsi zamanı tələb oluna bilən transformasiyalar və istənilən əlavə emal addımları daxildir. Microsoft SQL Serverin tərkib hissəsi olan SQL Server İnteqrasiya Xidmətləri (SSIS), verilənlər bazası serverləri arasında məlumatların işlənməsi mərhələlərini müəyyən etmək üçün DTSX fayllarından istifadə edir. DTSX faylları Microsoft SQL Server 2019 ilə açıla bilər.

## DTSX fayl formatı

Verilənlər bazası serverləri arasında məlumatların hərəkəti bu əməliyyat zamanı məlumatların bütövlüyünü təmin etmək üçün qaydalar və emal addımları tələb edir. SSIS müəssisədəki müxtəlif mənbələrdən məlumatların daşınması və uyğunlaşdırılması üçün bütün bu fəaliyyətlərin rahat şəkildə həyata keçirilməsini təmin edir. DTSX buradan gəlir ki, bu addımlar vasitəsilə məlumatların işlənə biləcəyi addımları təyin etmək üçün SSIS tərəfindən istifadə ediləcək strukturları müəyyən edir.

DTSX tərəfindən təsvir edilən məlumat axını aşağıdakı şəkildə göstərildiyi kimidir.

{{< figure src="../DataFlowDTSX.png" alt="Məlumat axını DTSX" >}}

DTSX is [XML](/web/xml/)-based and is documented in [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). The enhanced refactoring of DTSX XML is DTSX 2.0 that includes new attributes to the structures, replacement of named properties as parent XML attributes, specifies defaults for most attribute values, and placement of repeated elements inside a parent element. DTSX structures are described using these [XML Schemas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) and the structural format is celar-text XML.

## İstinadlar

 * [DTSX Format - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
 * [DTSX 2 Format - Microsoft tərəfindən](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

