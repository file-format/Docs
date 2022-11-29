{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "fil", "tillägg", "filformat", "Excel", "kalkylblad" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om OTS-filformat och API:er som kan skapa och öppna OTS-filer.",
  "title" :"OTS - OpenDocument Spreadsheet Template File Format",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Vad är OTS fil?

En fil med tillägget .ots är en OpenDocument Spreadsheet Template-fil som skapas med Calc-programvaran som ingår i Apache OpenOffice. Calc-programvaran liknar Excel som finns i Microsoft Office. OTS-filformat används för att skapa mallar som innehåller fördefinierade inställningar relaterade till stilar, teckensnitt, data, kalkylbladslayout och formatering. OTF-filer har `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Dessa mallfiler kan användas som utgångspunkt för att generera och spara faktiska datafiler som sparas i [ODS-filformat](/sv/spreadsheet/ods/). OTS-filer kan användas med applikationer som OpenOffice och LibreOffice.

## OTS filformat

OTS-filer sparas i OASIS OpenDocument XML-baserade filformat som består av en samling av flera underdokument med ett paket som ett [ZIP](/sv/compression/zip/)-arkiv. Varje zip-arkiv lagrar en del av det fullständiga dokumentet och varje underdokument lagrar en viss aspekt av dokumentet. Till exempel innehåller ett underdokument stilinformationen och ett annat underdokument innehåller dokumentets innehåll. Ett typiskt ODF-dokument har följande komponenter:

### OTS Content.xml

Content.xml-filen innehåller det faktiska innehållet i dokumentet. Detta inkluderar dock inte binär data som bilder.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml av OTS-filformat

Filen styles.xml innehåller stilinformation och används flitigt för formatering och layout. Stiltyper inkluderar:

* Styckestilar
* Sidstilar
* Karaktärsstilar
* Ramstilar
* Lista stilar

### Meta.xml

Meta.xml-filen innehåller information om filens metadata som författare, Senaste ändringsdatum, etc.
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

Filen `settings.xml` innehåller dokumentnivåinställningar som zoomfaktor och markörposition.

## Referenser ##

* [OpenDocument 1.2-specifikation](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Av Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

