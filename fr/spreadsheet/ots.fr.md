{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "fichier", "extension", "format de fichier", "Excel", "Feuille de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier OTS et les API qui peuvent créer et ouvrir des fichiers OTS.",
  "title" :"OTS - Format de fichier de modèle de feuille de calcul OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Qu'est-ce qu'un fichier OTS ?

Un fichier avec l'extension .ots est un fichier de modèle de feuille de calcul OpenDocument créé avec le logiciel d'application Calc inclus dans Apache OpenOffice. Le logiciel d'application Calc est similaire à Excel disponible dans Microsoft Office. Le format de fichier OTS est utilisé pour créer des modèles contenant des paramètres prédéfinis liés aux styles, à la police, aux données, à la mise en page de la feuille de calcul et au formatage. Les fichiers OTF ont `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Ces fichiers modèles peuvent être utilisés comme point de départ pour générer et enregistrer des fichiers de données réels qui sont enregistrés au [format de fichier ODS](/fr/spreadsheet/ods/). Les fichiers OTS peuvent être utilisés avec des applications telles que OpenOffice et LibreOffice.

## Format de fichier OTS

Les fichiers OTS sont enregistrés au format de fichier OpenDocument XML d'OASIS qui comprend une collection de plusieurs sous-documents avec un package sous forme d'archive [ZIP](/fr/compression/zip/). Chaque archive zip stocke une partie du document complet et chaque sous-document stocke un aspect particulier du document. Par exemple, un sous-document contient les informations de style et un autre sous-document contient le contenu du document. Un document ODF typique comprend les composants suivants :

### Contenu OTS.xml

Le fichier content.xml contient le contenu réel du document. Cependant, cela n'inclut pas les données binaires telles que les images.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml du format de fichier OTS

Le fichier styles.xml contient des informations de style et est largement utilisé pour le formatage et la mise en page. Les types de styles incluent :

* Styles de paragraphe
* Styles de page
* Styles de caractères
* Styles de cadre
* Styles de liste

### Méta.xml

Le fichier meta.xml contient des informations sur les métadonnées du fichier telles que l'auteur, la date de la dernière modification, etc.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Paramètres.xml

Le fichier `settings.xml` comprend des paramètres au niveau du document tels que le facteur de zoom et la position du curseur.

## Références ##

* [Spécification OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Par Wikipédia](https://en.wikipedia.org/wiki/OpenDocument)

