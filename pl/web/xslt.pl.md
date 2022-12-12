{
  "date" : "2021-01-20",
  "keywords" :["xslt", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "Rozszerzony język arkuszy stylów"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku XSLT",
  "description":"Poznaj format pliku XSLT i interfejsy API, które mogą tworzyć i otwierać pliki XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Czym jest plik XSLT?

Plik z rozszerzeniem .xslt to plik transformacji Extensible Stylesheet Language Transformation, który służy do przekształcania i stylizowania pliku XML przy użyciu instrukcji XSL. Format służy do przekształcania dokumentów XML w standardowe formaty wyjściowe, takie jak dokument tekstowy lub strona internetowa .html. Ta transformacja tworzy nowy dokument na podstawie zawartości istniejącego dokumentu XML. XSLT czyni go teoretycznie zdolnym do dowolnych obliczeń.

## Format pliku XSLT

Format pliku XLST zawiera instrukcje transformacji w formacie zwykłego tekstu, który można przeglądać w dowolnym edytorze tekstu. Były trzy wersje języka.

* `XSLT 1.0` — XSLT 1.0 został opublikowany jako rekomendacja W3C w listopadzie 1999 r.
* `XSLT 2.0` - Zawiera modyfikacje, takie jak manipulowanie łańcuchami przy użyciu wyrażeń regularnych, funkcji i operatorów do manipulowania datami, godzinami i czasem trwania, wiele dokumentów wyjściowych, grupowanie oraz bogatszy system typów i silne sprawdzanie typów.
* `XSLT 3.0` - stało się częścią rekomendacji W3C 8 czerwca 2017 r., a główne nowe funkcje obejmują transformację strumieniową, pakiety poprawiające modułowość dużych arkuszy stylów, ulepszoną obsługę błędów dynamicznych, na przykład za pomocą instrukcji xsl:try, oraz wsparcie dla map i tablic, umożliwiając XSLT obsługę zarówno JSON, jak i XML.

### Przykład XSLT

Poniższy przykład pochodzi z [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Bibliografia ##

* [XSLT – z Wikipedii](https://en.wikipedia.org/wiki/XSLT)
* [Elementy XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

