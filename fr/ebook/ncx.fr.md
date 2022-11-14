{
  "date" : "2021-03-23",
  "keywords" :["NCX", "EPUB Navigation Control XML File", "extension", "format", "E-Book", "TOC", "DAISY Consortium"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier EPUB Navigation Control XML File (NCX) et les API qui peuvent créer et ouvrir des fichiers NCX.",
  "title" :"NCX - Fichier XML de contrôle de navigation EPUB",
  "linktitle" : "NCX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Qu'est-ce qu'un fichier NCX ? ##

Le fichier NCX abrégé en fichier de contrôle de navigation pour XML, généralement nommé toc.ncx. Ce fichier se compose de la table des matières hiérarchique d'un fichier EPUB. La spécification pour NCX a été développée pour Digital Talking Book (DTB) et ce format de fichier est maintenu par le **DAISY Consortium** et ne fait pas partie de la spécification EPUB. Le fichier NCX inclut un type mime **application/x-dtbncx+xml**.

## Spécification NCX ##

Le fichier NCX contient différents types de balises XML. Les balises méta telles que `meta name="dtb:uid"` sont utilisées pour mentionner l'ID. L'élément `meta name="dtb:depth"` est égal à la profondeur de l'élément de balise `navMap`. Les éléments `navPoint` peuvent être imbriqués pour créer une table des matières hiérarchique. Le contenu de `navLabel` est le texte qui apparaît dans la table des matières générée par les systèmes de lecture qui utilisent le .ncx. Le contenu de l'élément `navPoint` pointe vers un document de contenu répertorié dans le manifeste et peut également inclure un identifiant d'élément

Une description de certaines exceptions à la spécification NCX telle qu'utilisée dans EPUB. Vous pouvez voir ici l'exemple d'un fichier NCX :

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ncx PUBLIC "-//NISO//DTD ncx 2005-1//EN"
"http://www.daisy.org/z3986/2005/ncx-2005-1.dtd">

<ncx version="2005-1" xml:lang="en" xmlns="http://www.daisy.org/z3986/2005/ncx/">

  <head>
<!-- The following four metadata items are required for all NCX documents,
including those that conform to the relaxed constraints of OPS 2.0 -->

    <meta name="dtb:uid" content="123456789X"/> <!-- same as in .opf -->
    <meta name="dtb:depth" content="1"/> <!-- 1 or higher -->
    <meta name="dtb:totalPageCount" content="0"/> <!-- must be 0 -->
    <meta name="dtb:maxPageNumber" content="0"/> <!-- must be 0 -->
  </head>

  <docTitle>
    <text>Pride and Prejudice</text>
  </docTitle>

  <docAuthor>
    <text>Austen, Jane</text>
  </docAuthor>

  <navMap>
    <navPoint class="chapter" id="chapter1" playOrder="1">
      <navLabel><text>Chapter 1</text></navLabel>
      <content src="chapter1.xhtml"/>
    </navPoint>
  </navMap>

</ncx>
```

## Références ##

* [EPUB de Wikipédia] (https://en.wikipedia.org/wiki/EPUB)
* [Quels fichiers inclure dans le toc.ncx](https://ebooks.stackexchange.com/questions/2332/what-files-to-include-in-the-toc-ncx)

