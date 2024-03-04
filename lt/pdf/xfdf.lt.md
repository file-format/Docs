{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XFDF failo formatas – kas yra XFDF failas?",
  "description": "Sužinokite apie XFDF failą ir API, kurios gali kurti ir atidaryti XFDF failus.",
  "linktitle": "XFDF",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-xfd-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra XFDF failas?

A file with .xfdf extension is an XML Forms Data Format that is generated with Adobe Acrobat software. Like [FDF](/pdf/fdf/), XFDF contains form elements description and their values in XML format. This can include the names and values of text fields in the PDF form. XFDF are saved in human-readable format and can be read programatically read using programming languages such as C#.

## XFDF failo formatas – daugiau informacijos

XFDF failai išsaugomi XML failo formatu, kuris yra universalus formatas, naudojamas duomenims importuoti ir eksportuoti. XFDF failo struktūrą sudaro antraštė, po kurios pateikiamos lauko reikšmės ir elementų duomenys, kaip parodyta toliau.

|Elementas|Atributas|Turinys|
---|---|---|
|\<XFDF> ||Viršutinis elementas|
|\<fields> ||Visos šio šablono lauko reikšmės|
|<field (T)> |vardas |Lauko pavadinimas|
|<value (V)> |vertė |Lauko reikšmė|

## Nuorodos

* [FDF formato palaikymas, sukurtas Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)

* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

