{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XFDF-tiedostomuoto - Mikä on XFDF-tiedosto?",
  "description": "Opi XFDF-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata XFDF-tiedostoja.",
  "linktitle": "XFDF",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-xfd-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on XFDF-tiedosto?

A file with .xfdf extension is an XML Forms Data Format that is generated with Adobe Acrobat software. Like [FDF](/pdf/fdf/), XFDF contains form elements description and their values in XML format. This can include the names and values of text fields in the PDF form. XFDF are saved in human-readable format and can be read programatically read using programming languages such as C#.

## XFDF-tiedostomuoto - lisätietoja

XFDF-tiedostot tallennetaan XML-tiedostomuodossa, joka on yleinen muoto, jota käytetään tietojen tuontiin ja vientiin. XFDF-tiedostorakenne koostuu otsikosta, jota seuraa kenttäarvot ja elementtitiedot alla olevan kuvan mukaisesti.

|Elementti|Attribuutti|Sisältö|
---|---|---|
|\<XFDF> ||Ylin elementti|
|\<fields> ||Kaikki tämän mallin kentän arvot|
|<field (T)> |nimi |Kentän nimi|
|<value (V)> |arvo |Kentän arvo|

## Viitteet

* [Acrobatin FDF-muototuki](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)

* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

