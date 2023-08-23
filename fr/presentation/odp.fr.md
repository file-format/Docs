{
  "date" : "2019-10-11",
  "keywords" :[ "fichier odp", "format de fichier odp", "qu'est-ce qu'un fichier odp", "fichier", "exemple odp", "extension de fichier odp","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODP - Format de fichier de présentation OpenOffice",
  "description":"En savoir plus sur le format de fichier ODP et les API qui peuvent créer et ouvrir des fichiers ODP.",
  "linktitle" : "ODP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier ODP ?

Les fichiers avec l'extension .odp représentent le format de fichier de présentation utilisé par OpenOffice.org dans la norme OASISOpen. Un fichier de présentation est une collection de diapositives où chaque diapositive peut comprendre du texte, des images, une mise en forme, des animations et d'autres médias. Ces diapositives sont présentées au public sous la forme de diaporamas avec des paramètres de présentation personnalisés. Les fichiers ODP peuvent être ouverts par des applications conformes au format OpenDocument (comme OpenOffice ou StarOffice).

## Bref historique

Les spécifications du format de fichier ODP sont basées sur la norme développée en tant que spécifications ODF. Ces spécifications ont évolué au cours du passé sous la forme de trois versions développées et publiées par OASIS comme suit :

`2005` - La version 1.0 a été publiée en mai 2005
`2007` - La version 1.1 a été publiée en février 2007
`2011` - La version 1.2 a été publiée en septembre 2011

Il y a eu des changements assez mineurs lors de la transition des versions ODF 1.0 à 1.1. La [version ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) est la dernière version des spécifications ODF et doit être consultée par les développeurs pour le développement d'applications liées à la lecture/écriture ODS.

## Spécifications du format de fichier

Le format OpenDocument prend en charge la représentation du document sous la forme d'un document XML unique ainsi qu'une collection de plusieurs sous-documents dans un package sous forme d'archive [ZIP](https://docs.fileformat.com/compression/zip/). Chacun des fichiers de l'archive ZIP stocke une partie du document complet. Chaque sous-document stocke un aspect particulier du document. Par exemple, un sous-document contient les informations de style et un autre sous-document contient le contenu du document. Un document ODF typique comprend les composants suivants :

* `content.xml` - Contenu du document et styles automatiques utilisés dans le contenu.
* `styles.xml` - Styles utilisés dans le contenu du document et styles automatiques utilisés dans les styles eux-mêmes.
* `meta.xml` - Documentez les méta-informations, telles que l'auteur ou l'heure de la dernière action d'enregistrement.
* `settings.xml` - Paramètres spécifiques à l'application, tels que la taille de la fenêtre ou les informations sur l'imprimante.

Outre ceux-ci, le package peut contenir de nombreux autres sous-documents tels que des vignettes de document, des images, etc.

Les fichiers de document de feuille de calcul sont le sous-ensemble de fichiers ODF où le contenu (feuilles) est stocké dans le sous-document content.xml.

## Références

* [OpenDocument - Par Wikipédia](https://en.wikipedia.org/wiki/OpenDocument)

