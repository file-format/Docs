{
  "date" : "2019-10-11",
  "keywords" :[ "fichier wmf", "format de fichier wmf", "qu'est-ce qu'un fichier wmf", "fichier", "exemple wmf", "extension de fichier wmf","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Format de métafichier Microsoft Windows",
  "description":"En savoir plus sur le format de fichier WMF et les API qui peuvent créer et ouvrir des fichiers WMF.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier WMF ?

Les fichiers avec l'extension WMF représentent le métafichier Microsoft Windows (WMF) pour stocker des données vectorielles et des images au format bitmap. Pour être plus précis, WMF appartient à la catégorie des formats de fichiers vectoriels des formats de fichiers graphiques indépendants de l'appareil. L'interface de périphérique graphique Windows (GDI) utilise les fonctions stockées dans un fichier WMF pour afficher une image à l'écran. Une version plus améliorée de WMF, connue sous le nom de Enhanced Meta Files (EMF), a été publiée plus tard, ce qui rend le format plus riche en fonctionnalités. Pratiquement, WMF est similaire à SVG.

## Spécifications du format de fichier WMF ##

Un fichier WMF faisait référence au format de fichier 16 bits au moment de son lancement avec Windows 3.0. Le format de fichier consiste en une série d'enregistrements de longueur variable qui contiennent des commandes de dessin graphique, des définitions d'objets et des propriétés. Étant donné que les fichiers WMF sont basés sur des commandes rendues au GDI pour dessiner l'image, il est également connu comme un enregistrement numérique de l'image qui peut être lu pour reproduire cette image. Les spécifications complètes du format de fichier de WMF sont disponibles en ligne et doivent être consultées pour le développement d'applications permettant de travailler avec des fichiers WMF. Un fichier WMF est organisé en :

* Enregistrement d'en-tête WMF
* Enregistrement(s) WMF
* Enregistrement de fin de fichier WMF

### Enregistrement d'en-tête WMF ###

L'enregistrement **META_HEADER** contient des informations qui définissent les caractéristiques du métafichier, notamment :

* Le type du métafichier
* La version du métafichier
* La taille du métafichier
* Le nombre d'objets définis dans le métafichier
* La taille du plus grand enregistrement unique dans le métafichier

### Enregistrement d'en-tête placable WMF ###

L'enregistrement **META_PLACEABLE** contient des informations détaillées concernant l'image, notamment :

* Un rectangle englobant
* Taille d'unité logique, pour la mise à l'échelle
* Une somme de contrôle, pour validation

### Enregistrement WMF ###

Les enregistrements WMF ont un format générique, qui est spécifié dans le document de spécifications. Chaque enregistrement WMF contient les informations suivantes :

* La taille de l'enregistrement
* La fonction d'enregistrement
* Paramètres, le cas échéant, pour la fonction d'enregistrement

## Références ##

* [[MS-WMF] : format de métafichier Windows](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Métafichier Windows - Wikipédia](https://en.wikipedia.org/wiki/Windows_Metafile)

