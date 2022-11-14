{
  "date" : "2021-01-20",
  "keywords" :["xslt", "File", "Extension", "File Format", "File Extension", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLT-bestandsindeling",
  "description":"Meer informatie over XSLT-bestandsindelingen en API's die XSLT-bestanden kunnen maken en openen.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Wat is een XSLT-bestand?

Een bestand met de extensie .xslt is een Extensible Stylesheet Language Transformation-bestand dat wordt gebruikt om een XML-bestand te transformeren en op te maken met behulp van XSL-instructies. Het formaat wordt gebruikt om XML-documenten om te zetten in standaard uitvoerformaten zoals een tekstdocument of .html-webpagina. Deze transformatie creëert een nieuw document op basis van de inhoud van het bestaande XML-document. XSLT maakt het theoretisch in staat tot willekeurige berekeningen.

## XSLT-bestandsindeling

Het XLST-bestandsformaat bevat transformatie-instructies in platte tekst die in elke teksteditor kunnen worden bekeken. Er zijn drie herzieningen van de taal geweest.

* `XSLT 1.0` - XSLT 1.0 werd in november 1999 gepubliceerd als een W3C-aanbeveling.
* `XSLT 2.0` - Het bevat aanpassingen zoals String-manipulatie met behulp van reguliere expressies, functies en operators voor het manipuleren van datums, tijden en duur, meerdere uitvoerdocumenten, groepering en een rijker typesysteem en sterke typecontrole.
* `XSLT 3.0` - Het werd op 8 juni 2017 onderdeel van de W3C-aanbeveling en de belangrijkste nieuwe functies zijn onder meer streaming-transformatie, pakketten om de modulariteit van grote stylesheets te verbeteren, verbeterde verwerking van dynamische fouten met bijvoorbeeld een xsl:try-instructie, en ondersteuning voor kaarten en arrays, waardoor XSLT zowel JSON als XML kan verwerken.

### XSLT-voorbeeld

Het volgende voorbeeld is afkomstig uit [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Referenties ##

* [XSLT - Door Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [XSLT-elementen](https://en.wikipedia.org/wiki/XSLT_elements)

