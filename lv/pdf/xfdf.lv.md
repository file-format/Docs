{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XFDF faila formāts — kas ir XFDF fails?",
  "description": "Uzziniet par XFDF failiem un API, kas var izveidot un atvērt XFDF failus.",
  "linktitle": "XFDF",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-xfd-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir XFDF fails?

A file with .xfdf extension is an XML Forms Data Format that is generated with Adobe Acrobat software. Like [FDF](/pdf/fdf/), XFDF contains form elements description and their values in XML format. This can include the names and values of text fields in the PDF form. XFDF are saved in human-readable format and can be read programatically read using programming languages such as C#.

## XFDF faila formāts — vairāk informācijas

XFDF faili tiek saglabāti XML faila formātā, kas ir universāls formāts, ko izmanto datu importēšanai un eksportēšanai. XFDF faila struktūra sastāv no galvenes, kam seko lauku vērtības un elementu dati, kā parādīts tālāk.

|Elements|Atribūts|Saturs|
---|---|---|
|\<XFDF> ||Augšējais elements|
|\<fields> ||Visas lauka vērtības šai veidnei|
|<field (T)> |nosaukums |Lauka nosaukums|
|<value (V)> |vērtība |Lauka vērtība|

## Atsauces

* [FDF formāta atbalsts, ko nodrošina Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)

* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

