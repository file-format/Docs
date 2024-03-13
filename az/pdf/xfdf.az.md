{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XFDF fayl formatı - XFDF faylı nədir?",
  "description": "XFDF faylları yarada və aça bilən XFDF faylı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "XFDF",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-xfd-azf"
}
},
  "lastmod": "2019-09-10"
}

## XFDF faylı nədir?

A file with .xfdf extension is an XML Forms Data Format that is generated with Adobe Acrobat software. Like [FDF](/pdf/fdf/), XFDF contains form elements description and their values in XML format. This can include the names and values of text fields in the PDF form. XFDF are saved in human-readable format and can be read programatically read using programming languages such as C#.

## XFDF Fayl Format - Ətraflı Məlumat

XFDF faylları məlumatların idxalı və ixracı üçün istifadə olunan universal format olan XML fayl formatında saxlanılır. XFDF fayl strukturu aşağıda göstərildiyi kimi başlıqdan, ardınca sahə dəyərlərindən və element məlumatlarından ibarətdir.

|Element|Atribut|Məzmun|
---|---|---|
|\<XFDF> ||Ən yüksək element|
|\<fields> ||Bu şablon üçün bütün sahə dəyərləri|
|<field (T)> |adı |Sahənin adı|
|<value (V)> |dəyər |Sahə dəyəri|

## İstinadlar

* [Acrobat tərəfindən FDF Format Dəstəyi](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)

* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

