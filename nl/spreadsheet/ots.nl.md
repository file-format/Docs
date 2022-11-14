{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "bestand", "extensie", "bestandsindeling", "Excel", "Spreadsheet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over OTS-bestandsindeling en API's die OTS-bestanden kunnen maken en openen.",
  "title" :"OTS - OpenDocument Spreadsheet-sjabloonbestandsindeling",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Wat is een OTS-bestand?

Een bestand met de extensie .ots is een OpenDocument Spreadsheet-sjabloonbestand dat is gemaakt met de Calc-toepassingssoftware die is opgenomen in Apache OpenOffice. Calc-toepassingssoftware is vergelijkbaar met Excel die beschikbaar is in Microsoft Office. OTS-bestandsindeling wordt gebruikt om sjablonen te maken die vooraf gedefinieerde instellingen bevatten met betrekking tot stijlen, lettertype, gegevens, spreadsheetlay-out en opmaak. OTF-bestanden hebben `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Deze sjabloonbestanden kunnen worden gebruikt als startpunt voor het genereren en opslaan van actuele gegevensbestanden die zijn opgeslagen in [ODS-bestandsindeling](/nl/spreadsheet/ods/). OTS-bestanden kunnen worden gebruikt met toepassingen zoals OpenOffice en LibreOffice.

## OTS-bestandsindeling

OTS-bestanden worden opgeslagen in OASIS' OpenDocument XML-gebaseerde bestandsindeling die bestaat uit een verzameling van verschillende subdocumenten met een pakket als een [ZIP](/nl/compression/zip/)-archief. Elk zip-archief slaat een deel van het volledige document op en elk subdocument slaat een bepaald aspect van het document op. Een subdocument bevat bijvoorbeeld de stijlinformatie en een ander subdocument bevat de inhoud van het document. Een typisch ODF-document heeft de volgende onderdelen:

### OTS-inhoud.xml

Het bestand content.xml bevat de feitelijke inhoud van het document. Dit omvat echter geen binaire gegevens zoals afbeeldingen.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml van OTS-bestandsindeling

Het bestand styles.xml bevat stijlinformatie en wordt veel gebruikt voor opmaak en lay-out. Stijltypen zijn onder meer:

* Alineastijlen
* Paginastijlen
* Karakterstijlen
* Framestijlen
* Lijst stijlen

### Meta.xml

Het bestand meta.xml bevat informatie over de metagegevens van het bestand, zoals auteur, datum van laatste wijziging, enz.
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
### Instellingen.xml

Het bestand `settings.xml` bevat instellingen op documentniveau, zoals zoomfactor en cursorpositie.

## Referenties ##

* [OpenDocument 1.2-specificatie](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Door Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

