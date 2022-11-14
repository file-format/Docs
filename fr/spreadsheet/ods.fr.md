{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "fichier", "extension", "format de fichier", "Feuille de calcul OpenDocument" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Votre guide de format de fichier pour savoir ce qu'est un fichier ODS et les API qui peuvent les créer et les ouvrir.",
  "title" :"Qu'est-ce qu'un fichier ODS ?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Qu'est-ce qu'un fichier ODS ?

Les fichiers avec l'extension .ods représentent le format de document de feuille de calcul OpenDocument modifiable par l'utilisateur. Les données sont stockées dans le fichier ODF en lignes et en colonnes. Il s'agit d'un format basé sur XML et l'un des nombreux sous-types de la famille Open Document Formats (ODF). Le format est spécifié dans le cadre des spécifications ODF 1.2 publiées et maintenues par OASIS. Un certain nombre d'applications sous Windows ainsi que d'autres systèmes d'exploitation peuvent ouvrir des fichiers ODS pour l'édition et la manipulation, notamment Microsoft Excel, NeoOffice et LibreOffice. Les fichiers ODS peuvent également être convertis dans d'autres formats de feuille de calcul, tels que [XLS](/fr/spreadsheet/xls/), [XLSX](/fr/spreadsheet/xlsx/) et d'autres par différentes applications.

## Bref historique ##

Les spécifications de format de fichier ODS sont basées sur la norme développée en tant que spécifications ODF. Ces spécifications ont évolué au cours du passé sous la forme de trois versions développées et publiées par OASIS comme suit :

`2005` - La version 1.0 a été publiée en mai 2005

`2007` - La version 1.1 a été publiée en février 2007

`2011` - La version 1.2 a été publiée en septembre 2011

Il y a eu des changements assez mineurs lors de la transition des versions ODF 1.0 à 1.1. La [version ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) est la dernière version des spécifications ODF et doit être consultée par les développeurs pour le développement d'applications liées à la lecture/écriture ODS.

## Format de fichier ODS ##

Le format OpenDocument prend en charge la représentation du document sous la forme d'un document XML unique ainsi qu'une collection de plusieurs sous-documents dans un package sous forme d'archive [ZIP](/fr/compression/zip/). Chacun des fichiers de l'archive ZIP stocke une partie du document complet. Chaque sous-document stocke un aspect particulier du document. Par exemple, un sous-document contient les informations de style et un autre sous-document contient le contenu du document. Un document ODF typique comprend les composants suivants :

* `content.xml` - Contenu du document et styles automatiques utilisés dans le contenu.
* `styles.xml` - Styles utilisés dans le contenu du document et styles automatiques utilisés dans les styles eux-mêmes.
* `meta.xml` - Documentez les méta-informations, telles que l'auteur ou l'heure de la dernière action d'enregistrement.
* `settings.xml` - Paramètres spécifiques à l'application, tels que la taille de la fenêtre ou les informations sur l'imprimante.

Outre ceux-ci, le package peut contenir de nombreux autres sous-documents tels que des vignettes de document, des images, etc.

Les fichiers de document de feuille de calcul sont le sous-ensemble de fichiers ODF où le contenu (feuilles) est stocké dans le sous-document content.xml.

## Références ##

* [OpenDocument - Par Wikipédia](https://en.wikipedia.org/wiki/OpenDocument)

