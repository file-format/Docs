{
  "date" : "2021-01-20",
  "keywords" :["xslt", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "Limbă extensibilă a foii de stil"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier XSLT",
  "description":"Aflați despre formatul de fișier XSLT și despre API-urile care pot crea și deschide fișiere XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Ce este un fișier XSLT?

Un fișier cu o extensie .xslt este un fișier Extensible Stylesheet Language Transformation care este utilizat pentru a transforma și a stila un fișier XML folosind instrucțiuni XSL. Formatul este folosit pentru a transforma documente XML în formate standard de ieșire, cum ar fi un document text sau o pagină web .html. Această transformare creează un nou document bazat pe conținutul documentului XML existent. XSLT îl face teoretic capabil de calcule arbitrare.

## Format de fișier XSLT

Formatul de fișier XLST conține instrucțiuni de transformare în format text simplu care pot fi vizualizate în orice editor de text. Au existat trei revizuiri ale limbii.

* `XSLT 1.0` - XSLT 1.0 a fost publicat ca recomandare W3C în noiembrie 1999.
* `XSLT 2.0` - Include modificări precum manipularea șirurilor folosind expresii regulate, funcții și operatori pentru manipularea datelor, orelor și duratelor, documente de ieșire multiple, grupare și un sistem de tip mai bogat și verificare puternică a tipului.
* `XSLT 3.0` - A devenit parte a Recomandării W3C la 8 iunie 2017, iar principalele caracteristici noi includ transformarea în flux, pachete pentru îmbunătățirea modularității foilor de stil mari, gestionarea îmbunătățită a erorilor dinamice cu, de exemplu, o instrucțiune xsl:try, și suport pentru hărți și matrice, permițând XSLT să gestioneze JSON și XML.

### Exemplu XSLT

Următorul exemplu este preluat de la [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Referințe ##

* [XSLT - După Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [Elemente XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

