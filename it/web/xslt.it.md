{
  "date" : "2021-01-20",
  "keywords" :["xslt", "File", "Estensione", "Formato file", "Estensione file", "Linguaggio del foglio di stile estensibile"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file XSLT",
  "description":"Scopri il formato di file XSLT e le API che possono creare e aprire file XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Che cos'è un file XSLT?

Un file con estensione .xslt è un file Extensible Stylesheet Language Transformation che viene utilizzato per trasformare e applicare uno stile a un file XML utilizzando le istruzioni XSL. Il formato viene utilizzato per trasformare i documenti XML in formati di output standard come un documento di testo o una pagina Web .html. Questa trasformazione crea un nuovo documento basato sul contenuto del documento XML esistente. XSLT lo sta rendendo teoricamente capace di calcoli arbitrari.

## Formato file XSLT

Il formato file XLST contiene istruzioni di trasformazione in formato testo normale che possono essere visualizzate in qualsiasi editor di testo. Ci sono state tre revisioni alla lingua.

* `XSLT 1.0` - XSLT 1.0 è stato pubblicato come raccomandazione del W3C nel novembre 1999.
* `XSLT 2.0` - Include modifiche come la manipolazione di stringhe utilizzando espressioni regolari, funzioni e operatori per manipolare date, orari e durate, documenti di output multipli, raggruppamenti e un sistema di tipi più ricco e un controllo di tipo avanzato.
* `XSLT 3.0` - È diventato parte della raccomandazione del W3C l'8 giugno 2017 e le principali novità includono la trasformazione dello streaming, i pacchetti per migliorare la modularità di fogli di stile di grandi dimensioni, una migliore gestione degli errori dinamici con, ad esempio, un'istruzione xsl:try, e supporto per mappe e array, consentendo a XSLT di gestire JSON e XML.

### Esempio XSLT

L'esempio seguente è tratto da [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Riferimenti ##

* [XSLT - Di Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [Elementi XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

