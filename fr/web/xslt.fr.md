{
  "date" : "2021-01-20",
  "keywords" :["xslt", "Fichier", "Extension", "Format de fichier", "Extension de fichier", "Langage de feuille de style extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier XSLT",
  "description":"En savoir plus sur le format de fichier XSLT et les API qui peuvent créer et ouvrir des fichiers XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Qu'est-ce qu'un fichier XSLT ?

Un fichier avec une extension .xslt est un fichier de transformation de langage de feuille de style extensible qui est utilisé pour transformer et styliser un fichier XML à l'aide d'instructions XSL. Le format est utilisé pour transformer des documents XML en formats de sortie standard tels qu'un document texte ou une page Web .html. Cette transformation crée un nouveau document basé sur le contenu du document XML existant. XSLT le rend théoriquement capable de calculs arbitraires.

## Format de fichier XSLT

Le format de fichier XLST contient des instructions de transformation au format texte brut qui peuvent être visualisées dans n'importe quel éditeur de texte. Il y a eu trois révisions de la langue.

* `XSLT 1.0` - XSLT 1.0 a été publié en tant que recommandation du W3C en novembre 1999.
* `XSLT 2.0` - Il inclut des modifications telles que la manipulation de chaînes à l'aide d'expressions régulières, de fonctions et d'opérateurs pour manipuler les dates, les heures et les durées, plusieurs documents de sortie, le regroupement, ainsi qu'un système de type plus riche et une vérification de type renforcée.
* `XSLT 3.0` - Il est devenu une partie de la recommandation du W3C le 8 juin 2017 et les principales nouvelles fonctionnalités incluent la transformation en continu, des packages pour améliorer la modularité des grandes feuilles de style, une meilleure gestion des erreurs dynamiques avec, par exemple, une instruction xsl:try, et la prise en charge des cartes et des tableaux, permettant à XSLT de gérer JSON ainsi que XML.

### Exemple XSLT

L'exemple suivant est tiré de [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
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
## Références ##

* [XSLT - Par Wikipédia](https://en.wikipedia.org/wiki/XSLT)
* [Éléments XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

