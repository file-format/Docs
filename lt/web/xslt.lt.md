{
  "date": "2021-01-20",
  "keywords": [
"xslt",
"Failas",
"Pratęsimas",
"Dokumento formatas",
"Failo plėtinys",
"Išplečiamos stiliaus lentelės kalba"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLT failo formatas",
  "description": "Sužinokite apie XSLT failo formatą ir API, kurios gali kurti ir atidaryti XSLT failus.",
  "linktitle": "XSLT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xsl-ltt"
}
},
  "lastmod": "2021-01-20"
}

## Kas yra XSLT failas?

Failas su plėtiniu .xslt yra išplečiamo stiliaus lapo kalbos transformacijos failas, naudojamas XML failui transformuoti ir stiliui naudojant XSL instrukcijas. Formatas naudojamas XML dokumentams paversti standartiniais išvesties formatais, pvz., tekstiniu dokumentu arba .html tinklalapiu. Ši transformacija sukuria naują dokumentą pagal esamo XML dokumento turinį. XSLT leidžia teoriškai atlikti savavališkus skaičiavimus.

## XSLT failo formatas

XLST failo formate yra paprasto teksto formato transformavimo instrukcijos, kurias galima peržiūrėti bet kuriame teksto rengyklėje. Buvo trys kalbos pataisymai.

* „XSLT 1.0“ – XSLT 1.0 buvo paskelbta kaip W3C rekomendacija 1999 m. lapkričio mėn.

* „XSLT 2.0“ – apima modifikacijas, tokias kaip manipuliavimas eilutėmis naudojant reguliariąsias išraiškas, funkcijas ir operatorius, skirtas manipuliuoti datomis, laiku ir trukme, kelis išvesties dokumentus, grupavimą ir turtingesnio tipo sistemą bei stiprų tipo tikrinimą.

* „XSLT 3.0“ – 2017 m. birželio 8 d. ji tapo W3C rekomendacijos dalimi, o pagrindinės naujos funkcijos apima srautinio perdavimo transformaciją, paketus, skirtus didelių stilių lentelių moduliavimui pagerinti, patobulintą dinaminių klaidų tvarkymą naudojant, pavyzdžiui, xsl:try instrukciją, ir žemėlapių bei masyvų palaikymas, leidžiantis XSLT tvarkyti JSON ir XML.


### XSLT pavyzdys

Šis pavyzdys paimtas iš [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Nuorodos Nr.

* [XSLT – Vikipedija](https://en.wikipedia.org/wiki/XSLT)

* [XSLT elementai](https://en.wikipedia.org/wiki/XSLT_elements)


