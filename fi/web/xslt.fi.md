{
  "date": "2021-01-20",
  "keywords": [
"xslt",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"Laajennettavissa oleva tyylitaulukkokieli"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLT-tiedostomuoto",
  "description": "Opi XSLT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XSLT-tiedostoja.",
  "linktitle": "XSLT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xsl-fit"
}
},
  "lastmod": "2021-01-20"
}

## Mikä on XSLT-tiedosto?

Tiedosto, jonka tunniste on .xslt, on Extensible Stylesheet Language Transformation -tiedosto, jota käytetään XML-tiedoston muuntamiseen ja tyyliin XSL-ohjeiden avulla. Muotoa käytetään XML-dokumenttien muuntamiseen vakiomuotoisiksi tulostusmuodoiksi, kuten tekstidokumentiksi tai .html-verkkosivuksi. Tämä muunnos luo uuden asiakirjan olemassa olevan XML-dokumentin sisällön perusteella. XSLT tekee siitä teoreettisesti kykenevän mielivaltaisiin laskelmiin.

## XSLT-tiedostomuoto

XLST-tiedostomuoto sisältää muunnosohjeet vain tekstimuodossa, joita voidaan tarkastella missä tahansa tekstieditorissa. Kieleen on tehty kolme tarkistusta.

* "XSLT 1.0" - XSLT 1.0 julkaistiin W3C-suosituksena marraskuussa 1999.

* `XSLT 2.0` - Se sisältää muunnoksia, kuten merkkijonojen manipuloinnin säännöllisten lausekkeiden avulla, funktioita ja operaattoreita päivämäärien, kellonaikojen ja kestojen muokkaamiseen, useita tulosteita, ryhmittelyä sekä monipuolisemman tyyppijärjestelmän ja vahvan tyyppitarkistuksen.

* `XSLT 3.0` - Siitä tuli osa W3C-suositusta 8. kesäkuuta 2017, ja tärkeimpiä uusia ominaisuuksia ovat suoratoiston muunnos, paketit suurten tyylisivujen modulaarisuuden parantamiseksi, parannettu dynaamisten virheiden käsittely esimerkiksi xsl:try-ohjeella, ja tuki karttoille ja taulukoille, minkä ansiosta XSLT voi käsitellä JSON- ja XML-tiedostoja.


### XSLT-esimerkki

Seuraava esimerkki on otettu kohteesta {{HYPERLINKKI}}.
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
## Viitteet ##

* [XSLT - Wikipedia](https://en.wikipedia.org/wiki/XSLT)

* [XSLT-elementit](https://en.wikipedia.org/wiki/XSLT_elements)


