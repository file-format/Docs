{
  "date" : "2021-01-20",
  "keywords" :["xslt", "Datei", "Erweiterung", "Dateiformat", "Dateierweiterung", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLT-Dateiformat",
  "description":"Erfahren Sie mehr über das XSLT-Dateiformat und APIs, die XSLT-Dateien erstellen und öffnen können.",
  "linktitle" :"XSL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Was ist eine XSLT-Datei?

Eine Datei mit der Erweiterung .xslt ist eine Extensible Stylesheet Language Transformation-Datei, die verwendet wird, um eine XML-Datei mithilfe von XSL-Anweisungen zu transformieren und zu formatieren. Das Format wird verwendet, um XML-Dokumente in Standardausgabeformate wie ein Textdokument oder eine .html-Webseite umzuwandeln. Diese Transformation erstellt ein neues Dokument basierend auf dem Inhalt des vorhandenen XML-Dokuments. XSLT macht es theoretisch zu beliebigen Berechnungen fähig.

## XSLT-Dateiformat

Das XLST-Dateiformat enthält Transformationsanweisungen im Nur-Text-Format, die in jedem Texteditor angezeigt werden können. Es gab drei Überarbeitungen der Sprache.

* „XSLT 1.0“ – XSLT 1.0 wurde als W3C-Empfehlung im November 1999 veröffentlicht.
* `XSLT 2.0` - Es enthält Modifikationen wie String-Manipulation mit regulären Ausdrücken, Funktionen und Operatoren zum Manipulieren von Datumsangaben, Uhrzeiten und Dauern, mehrere Ausgabedokumente, Gruppierung und ein reichhaltigeres Typsystem und eine starke Typprüfung.
* `XSLT 3.0` - Es wurde am 8. Juni 2017 Teil der W3C-Empfehlung und die wichtigsten neuen Funktionen umfassen Streaming-Transformation, Pakete zur Verbesserung der Modularität großer Stylesheets, verbesserte Behandlung dynamischer Fehler mit beispielsweise einer xsl:try-Anweisung, und Unterstützung für Karten und Arrays, sodass XSLT sowohl JSON als auch XML verarbeiten kann.

### XSLT-Beispiel

Das folgende Beispiel stammt aus [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## Verweise ##

* [XSLT – Von Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [XSLT-Elemente](https://en.wikipedia.org/wiki/XSLT_elements)

