{
  "date": "2019-12-10",
  "keywords": [
"ODS",
"fil",
"udvidelse",
"filformat",
"OpenDocument-regneark"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Din filformatguide for at vide, hvad en ODS-fil og API'er er, der kan oprette og åbne dem.",
  "title": "Hvad er ODS fil? ",
  "linktitle": "ODS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-od-das"
}
},
  "lastmod": "2019-12-10"
}

## Hvad er ODS fil?

Filer med filtypenavnet .ods står for OpenDocument Spreadsheet Document-format, der kan redigeres af brugeren. Data gemmes i ODF-filen i rækker og kolonner. Det er XML-baseret format og er en af flere undertyper i Open Document Formats (ODF)-familien. Formatet er specificeret som en del af ODF 1.2-specifikationerne udgivet og vedligeholdt af OASIS. En række applikationer på Windows såvel som andre operativsystemer kan åbne ODS-filer til redigering og manipulation, herunder Microsoft Excel, NeoOffice og LibreOffice. ODS-filer kan også konverteres til andre regnearksformater såvel som [XLS](/spreadsheet/xls/), [XLSX](/spreadsheet/xlsx/) og andre af forskellige applikationer.

## Kort historie ##

ODS filformatspecifikationer er baseret på standarden udviklet som ODF-specifikationer. Disse specifikationer har udviklet sig over tidligere i form af tre versioner udviklet og udgivet af OASIS som følger:

`2005`- Version 1.0 blev offentliggjort i maj 2005

`2007` - Version 1.1 blev offentliggjort i februar 2007

`2011` - Version 1.2 blev offentliggjort i september 2011

Der var ret små ændringer i overgangen fra ODF 1.0 til 1.1 versioner. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) er den seneste version for ODF-specifikationer og bør konsulteres af udviklere for udvikling af applikationer relateret til ODS-læsning/skrivning.

## ODS-filformat ##

OpenDocument-formatet understøtter dokumentrepræsentation som et enkelt XML-dokument samt en samling af flere underdokumenter i en pakke som [ZIP](/compression/zip/)-arkiv. Hver af filerne fra ZIP-arkivet gemmer en del af det komplette dokument. Hvert underdokument gemmer et bestemt aspekt af dokumentet. For eksempel indeholder et underdokument stilinformationen, og et andet underdokument indeholder indholdet af dokumentet. Et typisk ODF-dokument har følgende komponenter:

* `content.xml` – Dokumentindhold og automatiske stilarter, der bruges i indholdet.

* `styles.xml` – Typografier brugt i dokumentindholdet og automatiske typografier brugt i selve typografierne.

* `meta.xml` – Dokument metaoplysninger, såsom forfatteren eller tidspunktet for den sidste gemte handling.

* `settings.xml` – Programspecifikke indstillinger, såsom vinduesstørrelse eller printeroplysninger.


Udover disse kan der i pakken være mange andre underdokumenter som dokumentminiature, billeder osv.

Regnearksdokumentfiler er den delmængde af ODF-filer, hvor indholdet (arkene) er gemt i content.xml-underdokumentet.

## Referencer ##

* [OpenDocument - Af Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


