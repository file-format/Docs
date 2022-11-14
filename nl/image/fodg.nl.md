{
  "date" : "2019-10-11",
  "keywords" :[ "fodg-bestand", "fodg-bestandsformaat", "wat is een fodg-bestand", "bestand", "fodg-voorbeeld", "fodg-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument Tekening Bestandsformaat",
  "description":"Meer informatie over FODG-bestandsindeling en API's die FODG-bestanden kunnen maken en openen.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een FODG-bestand?

Een bestand met de extensie .fodg is een Apache OpenOffice Drawing-bestandsindeling voor het opslaan van tekenelementen. Het is gebaseerd op de bestandsformaatspecificaties die zijn uiteengezet door Advancement of Structural Information Standards (OASIS). Een ander vergelijkbaar bestandsformaat voor OpenOffice-afbeeldingen is [ODG](/nl/image/odg/) dat tekenelementen opslaat als een vectorafbeelding. FODG-bestanden kunnen zowel met OpenOffice als LibreOffice worden geopend. Andere bestandsindelingen die door OpenOffice worden ondersteund, zijn bijvoorbeeld [ODT](/nl/tekstverwerking/odt/), ODF, [ODP](/nl/presentation/odp/) en [ODS](/nl/spreadsheet/ods/).

## FODG-bestandsindeling

FODG is gebaseerd op het OpenDocument's XML-bestandsformaat dat voldoet aan OASIS OpenDocument Format ISO/IEC 26300. Het heeft Internet Media Type application/vnd.oasis.opendocument.graphics en voldoet ook aan org.oasis-open.opendocument public.composite-content . De XML-structuur is gebruikelijk voor alle documenttypen, zoals spreadsheets, tekenbestanden en tekstdocumenten. OpenOffice-documenten maken gebruik van de scheiding van zorgen door de inhoud, stijlen, metagegevens en toepassingsinstellingen te scheiden in vier afzonderlijke XML-bestanden.

`<office:document-content> ` - Documentinhoud en automatische stijlen die in de inhoud worden gebruikt.
`<office:document-styles> ` - Stijlen die worden gebruikt in de documentinhoud en automatische stijlen die in de stijlen zelf worden gebruikt.
`<office:document-meta> ` - Document meta-informatie, zoals de auteur of het tijdstip van de laatste opslagactie.
`<office:document-settings> ` - Toepassingsspecifieke instellingen, zoals de venstergrootte of printerinformatie.

## Referenties ##
* [Toekomstige specificaties voor v 1.3-standaardisatie](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [OASIS Open Document Formaat voor Office-toepassingen](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument-indeling - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

