{
  "date" : "2019-10-11",
  "keywords" :[ "fichier vssm", "format de fichier vssm", "qu'est-ce qu'un fichier vssm", "fichier", "exemple vssm", "extension de fichier vssm","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSM - Format de fichier compatible avec les macros Microsoft Visio",
  "description":"En savoir plus sur le format de fichier VSSM et les API qui peuvent créer et ouvrir des fichiers VSSM.",
  "linktitle" : "VSSM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier VSSM ?

Les fichiers avec l'extension .vssm sont des fichiers Microsoft Visio Stencil qui prennent en charge les macros. Un fichier VSSM lorsqu'il est ouvert permet d'exécuter les macros pour obtenir le formatage et le placement souhaités des formes dans un diagramme. En général, Microsoft Visio est un logiciel de dessin qui permet de créer des fichiers pouvant contenir et représenter des informations définies par l'utilisateur sous différentes formes. Les plus courants d'entre eux incluent, mais sans s'y limiter, les diagrammes UML, les organigrammes, les objets visuels, le flux d'informations, les organigrammes, les diagrammes de logiciels, la disposition du réseau, les modèles de base de données, le mappage d'objets et d'autres informations similaires. Les fichiers générés à l'aide de Visio peuvent également être convertis en différents formats de fichiers tels que [PNG](/fr/image/png/), [BMP](/fr/image/bmp/), [PDF](/fr/pdf/) et autres.

## Format de fichier VSSM

Le format de fichier VSSM a été introduit avec Microsoft Visio 2013 qui est basé sur les spécifications OpenOffice XML. Certains autres types de fichiers qui composent le format de fichier Visio 2013 incluent :

* .vsdm (dessin compatible avec les macros Visio)
* .vssx (gabarit Visio)
* .vssm (gabarit prenant en charge les macros Visio)
* .vstx (modèle Visio)
* .vstm (modèle compatible avec les macros Visio)

Sous le capot, le format de fichier Visio 2013 utilise un moyen structuré pour stocker les données d'application avec les ressources associées dans une archive telle que [ZIP](/fr/compression/zip/). Le fichier ZIP peut être extrait à l'aide de n'importe quel utilitaire d'extraction standard où il contient également d'autres types de fichiers.

Chaque fichier Visio est appelé package contenant d'autres fichiers ou parties. Une partie de package peut être un fichier XML, une image ou même une solution VBA. Les parties du package peuvent être divisées en parties "document" et "relation".

## Références ##

* [Introduction au format de fichier Visio](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

