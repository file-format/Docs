{
  "date" : "2019-10-11",
  "keywords" :["xml", "Datei", "Erweiterung", "Dateiformat", "Dateierweiterung", "erweiterbare Auszeichnungssprache"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XML-Dateiformat",
  "description":"Erfahren Sie mehr über das XML-Dateiformat und APIs, die XML-Dateien erstellen und öffnen können.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine XML-Datei?

XML steht für Extensible Markup Language, die **[HTML](/de/web/html/)** ähnelt, sich jedoch in der Verwendung von Tags zum Definieren von Objekten unterscheidet. Die Grundidee hinter der Erstellung des XML-Dateiformats bestand darin, Daten zu speichern und zu transportieren, ohne von Software- oder Hardware-Tools abhängig zu sein. Seine Popularität ist darauf zurückzuführen, dass es sowohl von Menschen als auch von Maschinen lesbar ist. Dies ermöglicht es ihm, gemeinsame Datenprotokolle in Form von Objekten zu erstellen, die gespeichert und über ein Netzwerk wie das World Wide Web (WWW) geteilt werden. Das "X" in XML steht für erweiterbar, was bedeutet, dass die Sprache gemäß den Benutzeranforderungen auf eine beliebige Anzahl von Symbolen erweitert werden kann. Für diese Funktionen wird sie von vielen Standarddateiformaten wie Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/de/web/xhtml/)** und **[SVG](/de/page-description-language /svg/)**.

## XML-Dateiformat

Das XML-Dateiformat basiert auf dem XML Document Object Model (DOM), einer Programmier-API für HTML- und XML-Dokumente. Das XML-DOM definiert eine Standardmethode für den Zugriff auf und die Bearbeitung der XML-Dokumentelemente. Es erstellt eine Baumstrukturansicht eines XML-Dokuments, das für den Zugriff auf alle Elemente über den DOM-Baum verwendet werden kann. Bestehende Elemente können geändert/gelöscht sowie neue Elemente im XML-Baum erstellt werden. Jedes Element eines XML-Dokuments wird als Knoten bezeichnet. Das XML-DOM ist wie in der folgenden Abbildung dargestellt.

{{< figure src="../XML DOM.png" alt="XML-DOM" >}}

### Universelle Herangehensweise an XML

Die Leistungsfähigkeit von XML macht es zu einer universellen Sprache für die Datenkommunikation über das Netzwerk, indem Datentransport und Plattformwechsel vereinfacht werden. Dies stellt auch sicher, dass Daten zwischen inkompatiblen Systemen ausgetauscht werden können, indem Daten im Klartextformat gespeichert werden. HTML dient der Datendarstellung über das Internet, während XML dem Datenaustausch dient. Die in XML verwendeten Markup-Tag-Paare definieren die Schlüsselelemente der Struktur, die von Leseanwendungen verwendet werden sollen.

## XML-Beispiel

Das Folgende ist ein vereinfachtes Beispiel eines CD-Katalogs, in dem jeder Datensatz Informationen über CDs wie Künstler, Land, Firma, Preis und Herstellungsjahr enthält.

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

## Verweise

* [XML – Von Wikipedia](https://en.wikipedia.org/wiki/XML)

