{
  "date" : "2019-10-11",
  "keywords" :[ "odg-bestand", "odg-bestandsindeling", "wat is een odg-bestand", "bestand", "odg-voorbeeld", "odg-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODG-bestandsindeling",
  "description":"Meer informatie over de ODG-bestandsindeling en API's die ODG-bestanden kunnen maken en openen.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een ODG-bestand?

Het ODG-bestandsformaat wordt gebruikt door Apache OpenOffice's Draw-toepassing om tekenelementen op te slaan als een vectorafbeelding. Het volgt de op XML gebaseerde specificaties voor bestandsindelingen zoals uiteengezet door Advancement of Structural Information Standards (OASIS). ODG geeft tekeningen weer als vectorafbeeldingen met punten, lijnen en krommen. Naast OpenOffice bieden LibreOffice en andere toepassingen ook ondersteuning voor het werken met het ODG-bestandsformaat. Andere formaten die door OpenOffice worden ondersteund, zijn bijvoorbeeld [ODT](/nl/tekstverwerking/odt/), ODF, [ODP](/nl/presentation/odp/) en [ODS](/nl/spreadsheet/ods/).


## Specificaties ODG-bestandsindeling

ODG-bestandsindeling is gebaseerd op OpenDocument-indeling, een gestructureerde XML-documentindeling met een goed gedefinieerd schema.
Elke structurele component van een OpenDocument-indeling wordt vertegenwoordigd door een element met bijbehorende attributen. De op XML gebaseerde structuur is gebruikelijk voor alle documenttypen, zoals een tekstdocument, spreadsheet of een tekenbestand. Een document kan verschillende stijlen bevatten. Een OpenDocument-bestandsstructuur bestaat uit de volgende elementen.
* Document root
* Metagegevens document
* Lichaamselementen en documenttypen
* Applicatie instellingen
* Scripts
* Lettertypeverklaringen
* Stijlen
* Paginastijlen en lay-outs

## Documentwortels ##

Een documenthoofdelement bevat het volledige document en is het primaire element van een bestand in OpenDocument-indeling. Dezelfde typen documenthoofdelementen zijn van toepassing op alle soorten documenten, zoals tekst, documenten, spreadsheets en tekendocumenten.

### Wortelelementen ###
Een enkel XML-document wordt vertegenwoordigd door zijn eigen root-element. De vijf verschillende ondersteunde wortelelementen zijn als volgt.

`<office:document>` - Compleet office-document in één XML-document.
`<office:document-content>` - Documentinhoud en automatische stijlen die in de inhoud worden gebruikt.
`<office:document-styles>` - Stijlen die worden gebruikt in de documentinhoud en automatische stijlen die in de stijlen zelf worden gebruikt.
`<office:document-meta>` - Document meta-informatie, zoals de auteur of het tijdstip van de laatste opslagactie.
`<office:document-settings>` - Toepassingsspecifieke instellingen, zoals de venstergrootte of printerinformatie.

### ODG-document metagegevens ###
Het OpenDocument bevat alle metadata-elementen in de \<office:meta> element. Deze algemene informatie over een document staat aan het begin van het document en toepassingen kunnen meerdere exemplaren van dezelfde elementen bijwerken.

### Body-element en documenttypen ###
De hoofdtekst van het document geeft het type inhoud aan dat in het document is opgenomen met behulp van het documenttype-element. Deze documenttypen zijn:
* tekstdocumenten
* tekendocumenten
* presentatie documenten
* spreadsheetdocumenten
* kaartdocumenten
* afbeeldingsdocumenten

### Applicatie instellingen ###
De instellingen voor kantoortoepassingen vertegenwoordigen verschillende instellingen die verband houden met de documentconfiguratie of het uiterlijk van het document. Elke categorie wordt vertegenwoordigd door een `<config:config-item-set>`. Voorbeelden van dergelijke instellingscategorieën zijn:
* Documentinstellingen bijv. standaardprinter
* Instellingen bekijken, bijv. zoomniveau

### Scripts ###
Het is gebruikelijk dat een document meerdere scripts bevat. Elk script in een OpenDocument-bestand wordt vertegenwoordigd door een `<office:script>`-element. Deze scriptelementen bevinden zich in een enkele `<office:scripts>`-element. Scripts werken een document niet bij terwijl het document wordt geladen.
### Lettertypeverklaringen ###

Een lettertypedeclaratie bevat informatie over de lettertypen die door de auteur van een document worden gebruikt. Deze informatie helpt bij het vinden van deze lettertypen op andere systemen.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Stijlen ###
De volgende stijlen worden ondersteund door het OpenDocument-formaat.

`Common Styles` - De XML-representaties van dergelijke stijlen worden stijlen genoemd
`Automatische stijlen` - Bevat opmaakeigenschappen die in de gebruikersinterface van een document worden toegewezen aan een object zoals een alinea.
`Mater Styles` - een veelgebruikte stijl die opmaakinformatie en aanvullende inhoud bevat die wordt weergegeven bij de documentinhoud wanneer de stijl wordt toegepast. Een voorbeeld van een stramienstijl zijn stramienpagina's.

## Referenties ##
* [OASIS Open Document Formaat voor Office-toepassingen](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument-indeling - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

