{
  "date" : "2021-01-20",
  "keywords" :["xslt", "File", "Extension", "File Format", "File Extension", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru XSLT",
  "description":"Další informace o formátu souborů XSLT a rozhraních API, která mohou vytvářet a otevírat soubory XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Co je soubor XSLT?

Soubor s příponou .xslt je soubor Extensible Stylesheet Language Transformation, který se používá k transformaci a stylování souboru XML pomocí instrukcí XSL. Formát se používá k transformaci dokumentů XML do standardních výstupních formátů, jako je textový dokument nebo webová stránka .html. Tato transformace vytvoří nový dokument založený na obsahu existujícího XML dokumentu. XSLT jej činí teoreticky schopným libovolných výpočtů.

## Formát souboru XSLT

Formát souboru XLST obsahuje pokyny pro transformaci ve formátu prostého textu, který lze zobrazit v libovolném textovém editoru. Byly provedeny tři revize jazyka.

* `XSLT 1.0` - XSLT 1.0 byl publikován jako doporučení W3C v listopadu 1999.
* `XSLT 2.0` - Zahrnuje úpravy, jako je manipulace s řetězci pomocí regulárních výrazů, funkcí a operátorů pro manipulaci s daty, časy a trváním, více výstupních dokumentů, seskupování a bohatší typový systém a silná kontrola typu.
* `XSLT 3.0` – stal se součástí doporučení W3C dne 8. června 2017 a mezi hlavní nové funkce patří transformace streamování, balíčky pro zlepšení modularity velkých stylů, vylepšené zpracování dynamických chyb, například pomocí instrukce xsl:try, a podpora pro mapy a pole, což umožňuje XSLT zpracovat JSON i XML.

### Příklad XSLT

Následující příklad je převzat z [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Reference ##

* [XSLT – z Wikipedie](https://en.wikipedia.org/wiki/XSLT)
* [prvky XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

