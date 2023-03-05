{
  "date" : "2021-04-08",
  "keywords" :[ "fichier pkg", "format de fichier pkg", "qu'est-ce qu'un fichier pkg", "fichier", "exemple de pkg", "extension de fichier pkg","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Format de fichier d'archive extensible",
  "description":"En savoir plus sur le format de fichier PKG et les API qui peuvent créer et ouvrir des fichiers PKG.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Qu'est-ce qu'un fichier PKG ?

Un fichier avec l'extension .pkg est un fichier de package d'installation utilisé pour installer un logiciel sur macOS. En plus des ordinateurs Macintosh, il est également utilisé sur l'iPhone. L'application d'installation Apple intégrée peut être utilisée pour installer le contenu d'un fichier PKG. Un fichier PKG est similaire à un fichier MSI utilisé sur le système d'exploitation Windows pour l'installation de logiciels. Lors de l'installation, ces fichiers de package peuvent enregistrer des messages qui vous donnent une idée des éléments supplémentaires installés par ce package.

## Format de fichier PKG

Les PKR sont des fichiers binaires qui sont compressés pour réduire la taille globale du fichier. Depuis OSX 10.5, des packages plats avec des fichiers d'installation uniques ont été introduits par Apple. Ceux-ci sont différents des formats d'emballage précédents qui se présentaient sous forme de bundles plutôt que de fichiers uniques. Ces packages groupés contenaient une hiérarchie de répertoires structurée qui stockait les fichiers de manière à faciliter leur récupération via un fichier d'index. Le format de fichier plat PKG est en fait une archive [XAR](/fr/compression/xar/) qui a :

* En-tête - Définit la taille, la somme de contrôle et les informations de version
* Table des matières - Un document XML qui est (et doit) être encodé en UTF-8 et est stocké au début du fichier, ce qui facilite la numérisation de l'archive pour extraire un fichier individuel
* Heap - tas non structuré de données référencées par la table des matières

## Références

* [Format de fichier de package plat](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipédia](https://en.wikipedia.org/wiki/.pkg)

