{
  "date" : "2021-01-20",
  "keywords" :["xslt", "File", "Extension", "File Format", "File Extension", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLT fájlformátum",
  "description":"További információ az XSLT fájlformátumról és az API-król, amelyek XSLT-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Mi az XSLT fájl?

Az .xslt kiterjesztésű fájl egy kiterjeszthető stíluslap nyelvi átalakítási fájl, amely XML-fájlok átalakítására és stílusára szolgál XSL-utasítások segítségével. A formátum az XML dokumentumok szabványos kimeneti formátumokká, például szöveges dokumentumokká vagy .html weboldalakká történő átalakítására szolgál. Ez az átalakítás egy új dokumentumot hoz létre a meglévő XML dokumentum tartalma alapján. Az XSLT elméletileg képessé teszi tetszőleges számításokra.

## XSLT fájlformátum

Az XLST fájlformátum egyszerű szöveges formátumú átalakítási utasításokat tartalmaz, amelyek bármely szövegszerkesztőben megtekinthetők. Három revízió történt a nyelven.

* `XSLT 1.0` – Az XSLT 1.0 W3C ajánlásként jelent meg 1999 novemberében.
* `XSLT 2.0` - Olyan módosításokat tartalmaz, mint például a karakterlánc-manipuláció reguláris kifejezésekkel, függvények és operátorok a dátumok, időpontok és időtartamok manipulálására, több kimeneti dokumentum, csoportosítás, gazdagabb típusrendszer és erős típusellenőrzés.
* `XSLT 3.0` – 2017. június 8-án a W3C Recommendation részévé vált, és a fő újdonságok közé tartozik a streaming átalakítás, a csomagok a nagy stíluslapok modularitásának javítására, a dinamikus hibák jobb kezelése, például egy xsl:try utasítással, valamint a térképek és tömbök támogatása, lehetővé téve az XSLT számára a JSON és az XML kezelését.

### XSLT példa

A következő példa a [w3schools](https://www.w3schools.com/xml/xsl_intro.asp) webhelyről származik.
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
## Referenciák ##

* [XSLT – a Wikipedia által](https://en.wikipedia.org/wiki/XSLT)
* [XSLT-elemek](https://en.wikipedia.org/wiki/XSLT_elements)

