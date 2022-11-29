{
  "date" : "2021-01-20",
  "keywords" :["xslt", "Fil", "Tillägg", "Filformat", "Filtillägg", "Utökningsbar formatmallsspråk"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLT-filformat",
  "description":"Läs mer om XSLT-filformat och API:er som kan skapa och öppna XSLT-filer.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Vad är en XSLT fil?

En fil med filtillägget .xslt är en Extensible Stylesheet Language Transformation-fil som används för att transformera och formatera en XML-fil med XSL-instruktioner. Formatet används för att omvandla XML-dokument till standardutdataformat som ett textdokument eller .html-webbsida. Denna transformation skapar ett nytt dokument baserat på innehållet i det befintliga XML-dokumentet. XSLT gör den teoretiskt kapabel till godtyckliga beräkningar.

## XSLT filformat

XLST-filformatet innehåller transformationsinstruktioner i vanligt textformat som kan visas i vilken textredigerare som helst. Det har gjorts tre ändringar av språket.

* `XSLT 1.0` - XSLT 1.0 publicerades som en W3C-rekommendation i november 1999.
* `XSLT 2.0` - Den innehåller modifieringar som strängmanipulering med reguljära uttryck, funktioner och operatorer för att manipulera datum, tider och varaktigheter, flera utdatadokument, gruppering och ett rikare typsystem och stark typkontroll.
* `XSLT 3.0` – Det blev en del av W3C-rekommendationen den 8 juni 2017 och de viktigaste nya funktionerna inkluderar streamingtransformation, paket för att förbättra modulariteten för stora stilmallar, förbättrad hantering av dynamiska fel med till exempel en xsl:try-instruktion, och stöd för kartor och arrayer, vilket gör att XSLT kan hantera JSON såväl som XML.

### XSLT-exempel

Följande exempel är hämtat från [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Referenser ##

* [XSLT - av Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [XSLT Elements](https://en.wikipedia.org/wiki/XSLT_elements)

