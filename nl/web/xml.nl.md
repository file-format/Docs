{
  "date" : "2019-10-11",
  "keywords" :["xml", "Bestand", "Extensie", "Bestandsindeling", "Bestandsextensie", "uitbreidbare opmaaktaal"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XML-bestandsindeling",
  "description":"Meer informatie over XML-bestandsindeling en API's die XML-bestanden kunnen maken en openen.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een XML-bestand?

XML staat voor Extensible Markup Language en is vergelijkbaar met **[HTML](/nl/web/html/)** maar verschilt in het gebruik van tags voor het definiëren van objecten. Het hele idee achter het creëren van een XML-bestandsformaat was om gegevens op te slaan en te transporteren zonder afhankelijk te zijn van software- of hardwaretools. Zijn populariteit is te danken aan het feit dat het zowel menselijk als machinaal leesbaar is. Hierdoor kan het gemeenschappelijke gegevensprotocollen maken in de vorm van objecten die moeten worden opgeslagen en gedeeld via een netwerk zoals World Wide Web (WWW). De "X" in XML is voor uitbreidbaar, wat inhoudt dat de taal kan worden uitgebreid tot een willekeurig aantal symbolen volgens de vereisten van de gebruiker. Het is voor deze functies dat veel standaard bestandsindelingen er gebruik van maken, zoals Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/nl/web/xhtml/)** en **[SVG](/nl/page-description-language/svg/)**.

## XML-bestandsindeling

Het XML-bestandsformaat is gebaseerd op het XML Document Object Model (DOM), een programmeer-API voor HTML- en XML-documenten. De XML DOM definieert een standaardmethode om toegang te krijgen tot de XML-documentelementen en deze te manipuleren. Het maakt een boomstructuurweergave van een XML-document dat kan worden gebruikt om toegang te krijgen tot alle elementen via de DOM-boom. Bestaande elementen kunnen worden gewijzigd/verwijderd en er kunnen nieuwe elementen in de XML-boom worden gemaakt. Elk element van een XML-document wordt een knooppunt genoemd. De XML DOM is zoals weergegeven in de volgende afbeelding.

{{< figure src="../XML DOM.png" alt="XML-DOM" >}}

### Universele benadering van XML

De kracht van XML maakt het een universele taal voor datacommunicatie over het netwerk door datatransport en platformveranderingen te vereenvoudigen. Dit zorgt er ook voor dat gegevens tussen incompatibele systemen kunnen worden uitgewisseld door gegevens in platte tekst op te slaan. HTML is voor gegevensweergave via het web, terwijl XML voor gegevensuitwisseling is. De markup-tagparen die in XML worden gebruikt, definiëren de belangrijkste elementen van de structuur die door leestoepassingen moeten worden gebruikt.

## XML-voorbeeld

Het volgende is een vereenvoudigd voorbeeld van een cd-catalogus waarbij elk record informatie over cd's bevat, zoals artiest, land, bedrijf, prijs en productiejaar.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Referenties

* [XML - Door Wikipedia](https://en.wikipedia.org/wiki/XML)

