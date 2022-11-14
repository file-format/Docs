{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier GDB - Fichier de géodatabase de fichier ESRI",
  "description":"En savoir plus sur le format de fichier GDB et les API qui peuvent créer et ouvrir des fichiers GDB.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Qu'est-ce qu'un fichier GDB ?

Le fichier ESRI Geodatabase (FileGDB) est une collection de fichiers dans un dossier sur disque qui contient des données géospatiales connexes telles que des jeux de données d'entités, des classes d'entités et des tables associées. Il nécessite que certains autres fichiers soient conservés à côté du fichier .gdb dans le même répertoire pour que cela fonctionne. Les requêtes peuvent être exécutées sur le fichier .gdb pour gérer les données spatiales et non spatiales.

## Format de fichier GDB - Plus d'informations

Les géodatabases fichier sont composées de sept tables système plus des données utilisateur. Les données utilisateur peuvent être stockées dans les types d'ensembles de données suivants :

* Classe d'entités
* Ensemble de données d'entités
* Ensemble de données mosaïque
* Catalogue raster
* Jeu de données raster
* Jeu de données schématique
* Tableau (non spatial)
* Boîtes à outils

Les jeux de classes d'entités peuvent contenir des classes d'entités ainsi que les types de jeux de données suivants :

* Pièces jointes
* Annotation liée aux fonctionnalités
* Réseaux géométriques
* Jeux de données réseau
* Tissus colis
* Classes relationnelles
* Terrains
* Topologies

La taille maximale par défaut des jeux de données dans les géodatabases fichier est de 1 To. La taille maximale peut être augmentée à 256 To pour les grands ensembles de données (généralement raster). Ceci est contrôlé par un mot-clé de configuration. Reportez-vous à la rubrique Mots-clés de configuration pour les géodatabases fichier pour plus d'informations.

Les géodatabases fichier peuvent également contenir des sous-types et des domaines et participer à la réplication d'extraction/d'archivage et aux répliques unidirectionnelles.

Une géodatabase fichier est accessible simultanément par plusieurs utilisateurs. Si les utilisateurs effectuent des modifications, ils doivent modifier différents ensembles de données.

## Spécifications du format de fichier GDB ##

Le fichier GDB est un format propriétaire d'ESRI et ses spécifications ne sont pas disponibles publiquement. Pour cette raison, les détails du format de fichier pour FIle GDB n'ont pas pu être documentés ailleurs que par certaines sources qui l'ont fait [partiellement](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) par rétro-ingénierie .

## Références ##

* [Spécifications FGDB](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

