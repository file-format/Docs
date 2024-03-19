{
  "date" : "2019-10-11",
  "keywords" :["xml", "Fichier", "Extension", "Format de fichier", "Extension de fichier", "langage de balisage extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier XML",
  "description":"En savoir plus sur le format de fichier XML et les API qui peuvent créer et ouvrir des fichiers XML.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier XML ?

XML signifie Extensible Markup Language qui est similaire à **[HTML](/fr/web/html/)** mais différent dans l'utilisation de balises pour définir des objets. L'idée derrière la création du format de fichier XML était de stocker et de transporter des données sans dépendre d'outils logiciels ou matériels. Sa popularité est due au fait qu'il est à la fois lisible par l'homme et par la machine. Cela lui permet de créer des protocoles de données communs sous la forme d'objets à stocker et à partager sur un réseau tel que le World Wide Web (WWW). Le "X" dans XML est pour extensible, ce qui implique que le langage peut être étendu à n'importe quel nombre de symboles selon les besoins de l'utilisateur. C'est pour ces fonctionnalités que de nombreux formats de fichiers standard l'utilisent tels que Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/fr/web/xhtml/)** et **[SVG](/fr/page-description-language/svg/)**.

## Format de fichier XML

Le format de fichier XML est basé sur le XML Document Object Model (DOM) qui est une API de programmation pour les documents HTML et XML. Le DOM XML définit une méthode standard pour accéder et manipuler les éléments du document XML. Il crée une vue arborescente d'un document XML qui peut être utilisée pour accéder à tous les éléments via l'arborescence DOM. Les éléments existants peuvent être modifiés/supprimés et de nouveaux éléments peuvent être créés dans l'arborescence XML. Chaque élément d'un document XML est appelé un nœud. Le DOM XML est comme indiqué dans l'image suivante.

{{< figure src="../XML DOM.png" alt="DOM XML" >}}

### Approche universelle de XML

La puissance de XML en fait un langage universel pour la communication de données sur le réseau en simplifiant le transport des données et les changements de plate-forme. Cela garantit également que l'échange de données entre des systèmes incompatibles est possible en stockant les données au format texte brut. HTML est pour la représentation de données sur le Web, tandis que XML est pour l'échange de données. Les paires de balises de balisage utilisées dans XML définissent les éléments clés de la structure à utiliser par les applications de lecture.

## Exemple XML

Voici un exemple simplifié d'un catalogue de CD où chaque enregistrement contient des informations sur les CD telles que l'artiste, le pays, la société, le prix et l'année de production.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Références

* [XML - Par Wikipédia](https://en.wikipedia.org/wiki/XML)

