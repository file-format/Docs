{
  "date" : "2019-10-11",
  "keywords" :[ "fichier fodg", "format de fichier fodg", "qu'est-ce qu'un fichier fodg", "fichier", "exemple fodg", "extension de fichier fodg","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - Format de fichier de dessin OpenDocument",
  "description":"En savoir plus sur le format de fichier FODG et les API qui peuvent créer et ouvrir des fichiers FODG.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier FODG ?

Un fichier avec l'extension .fodg est un format de fichier Apache OpenOffice Drawing permettant de stocker des éléments de dessin. Il est basé sur les spécifications de format de fichier décrites par Advancement of Structural Information Standards (OASIS). Un autre format de fichier similaire pour les graphiques OpenOffice est [ODG](/fr/image/odg/) qui stocke les éléments de dessin sous forme d'image vectorielle. Les fichiers FODG peuvent être ouverts avec OpenOffice ainsi que LibreOffice. Les autres formats de fichiers pris en charge par OpenOffice, par exemple, incluent [ODT](/fr/word-processing/odt/), ODF, [ODP](/fr/presentation/odp/) et [ODS](/fr/spreadsheet/ods/).

## Format de fichier FODG

FODG est basé sur le format de fichier XML d'OpenDocument qui est conforme au format OASIS OpenDocument ISO/IEC 26300. Il a le type de média Internet application/vnd.oasis.opendocument.graphics et est également conforme à org.oasis-open.opendocument public.composite-content . La structure XML est commune à tous les types de documents tels que les feuilles de calcul, les fichiers de dessin et les documents texte. Les documents OpenOffice tirent parti de la séparation des préoccupations en séparant le contenu, les styles, les métadonnées et les paramètres d'application dans quatre fichiers XML distincts.

`<office:document-content> ` - Contenu du document et styles automatiques utilisés dans le contenu.
`<office:document-styles> ` - Styles utilisés dans le contenu du document et styles automatiques utilisés dans les styles eux-mêmes.
`<office:document-meta> ` - Documenter les méta-informations, telles que l'auteur ou l'heure de la dernière action d'enregistrement.
`<office:document-settings> ` - Paramètres spécifiques à l'application, tels que la taille de la fenêtre ou les informations sur l'imprimante.

## Références ##
* [Future Specifications for v 1.3 Standardization ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [Format de document ouvert OASIS pour les applications Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Format OpenDocument - Wikipédia](https://en.wikipedia.org/wiki/OpenDocument)

