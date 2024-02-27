{
  "date": "2021-01-20",
  "keywords": [
"xslt",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"Udvidbart stylesheet-sprog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLT filformat",
  "description": "Lær om XSLT-filformat og API'er, der kan oprette og åbne XSLT-filer.",
  "linktitle": "XSLT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xsl-dat"
}
},
  "lastmod": "2021-01-20"
}

## Hvad er en XSLT fil?

En fil med filtypen .xslt er en Extensible Stylesheet Language Transformation-fil, der bruges til at transformere og style en XML-fil ved hjælp af XSL-instruktioner. Formatet bruges til at transformere XML-dokumenter til standardoutputformater såsom et tekstdokument eller .html-webside. Denne transformation opretter et nyt dokument baseret på indholdet af det eksisterende XML-dokument. XSLT gør den teoretisk i stand til vilkårlige beregninger.

## XSLT filformat

XLST-filformatet indeholder transformationsinstruktioner i almindeligt tekstformat, som kan ses i enhver teksteditor. Der har været tre revisioner af sproget.

* `XSLT 1.0` - XSLT 1.0 blev offentliggjort som en W3C-anbefaling i november 1999.

* `XSLT 2.0` - Det inkluderer modifikationer såsom strengmanipulation ved hjælp af regulære udtryk, funktioner og operatorer til at manipulere datoer, klokkeslæt og varigheder, flere outputdokumenter, gruppering og et rigere typesystem og stærk typekontrol.

* `XSLT 3.0` - Det blev en del af W3C-anbefalingen den 8. juni 2017, og de vigtigste nye funktioner inkluderer streamingtransformation, pakker til at forbedre modulariteten af store stylesheets, forbedret håndtering af dynamiske fejl med for eksempel en xsl:try-instruktion, og understøttelse af kort og arrays, hvilket gør det muligt for XSLT at håndtere JSON såvel som XML.


### XSLT-eksempel

Følgende eksempel er taget fra [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Referencer ##

* [XSLT - af Wikipedia](https://en.wikipedia.org/wiki/XSLT)

* [XSLT Elements](https://en.wikipedia.org/wiki/XSLT_elements)


