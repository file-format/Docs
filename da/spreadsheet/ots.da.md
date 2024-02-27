{
  "date": "2019-12-16",
  "keywords": [
"OTS",
"fil",
"udvidelse",
"filformat",
"Excel",
"Regneark"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om OTS-filformat og API'er, der kan oprette og åbne OTS-filer.",
  "title": "OTS - OpenDocument Spreadsheet Template File Format",
  "linktitle": "OTS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-ot-das"
}
},
  "lastmod": "2021-01-19"
}

## Hvad er OTS fil?

En fil med filtypenavnet .ots er en OpenDocument Spreadsheet Template-fil, der er oprettet med Calc-applikationssoftwaren inkluderet i Apache OpenOffice. Calc-applikationssoftware ligner Excel, der er tilgængelig i Microsoft Office. OTS-filformat bruges til at oprette skabeloner, der indeholder foruddefinerede indstillinger relateret til typografier, skrifttype, data, regnearkslayout og formatering. OTF-filer har `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Disse skabelonfiler kan bruges som udgangspunkt til at generere og gemme faktiske datafiler, der er gemt i [ODS file format](/spreadsheet/ods/). OTS-filer kan bruges med programmer som OpenOffice og LibreOffice.

## OTS filformat

OTS-filer gemmes i OASIS' OpenDocument XML-baserede filformat, der består af en samling af flere underdokumenter med en pakke som et [ZIP](/compression/zip/)-arkiv. Hvert zip-arkiv gemmer en del af det komplette dokument, og hvert underdokument gemmer et bestemt aspekt af dokumentet. For eksempel indeholder et underdokument stilinformationen, og et andet underdokument indeholder indholdet af dokumentet. Et typisk ODF-dokument har følgende komponenter:

### OTS Content.xml

Content.xml-filen indeholder det faktiske indhold af dokumentet. Dette inkluderer dog ikke binære data såsom billeder.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml af OTS-filformat

Filen styles.xml indeholder information om styling og er meget brugt til formatering og layout. Stiltyper omfatter:

 * Afsnitsstile
 * Sidestile
 * Karakterstile
 * Ramme stilarter
 * Liste stilarter

### Meta.xml

Meta.xml-filen indeholder oplysninger om filens metadata såsom forfatter, dato for sidste ændring osv.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

Filen `settings.xml` indeholder indstillinger på dokumentniveau såsom zoomfaktor og markørposition.

## Referencer ##

* [OpenDocument 1.2-specifikation](https://www.oasis-open.org/standards#opendocumentv1.2)

* [OpenDocument - Af Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


