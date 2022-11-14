{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "extension", "fichier", "format", "système", "fichier TMP", "documents TMP", "fichiers TMP", "fichier temporaire", "application", "programmes" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Format de fichier temporaire",
  "description":"En savoir plus sur le format de fichier TMP et les API qui peuvent créer et ouvrir des fichiers TMP.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Qu'est-ce qu'un fichier TMP ? ##

Un fichier TMP fait référence à une sauvegarde, un stockage ou un autre système de fichiers transitoire généré par un logiciel. Il est parfois créé en tant que fichier invisible et est fréquemment détruit lors de la fermeture du programme. Les fichiers TMP peuvent également être utilisés pour stocker temporairement des informations pendant la construction d'un nouveau fichier.

## Format de fichier TMP ##

Un fichier TMP est généralement composé de données brutes qui sont utilisées comme une phase dans le processus de conversion du matériau d'un style à un autre. Microsoft Word et Apple Safari sont deux applications capables de produire et d'utiliser le format de fichier TMP.

Les documents TMP générés devraient, en théorie, être automatiquement supprimés lorsque le programme est fermé ou que la machine est éteinte. En pratique, ce n'est pas toujours le cas. Par conséquent, lors de la navigation dans les documents de votre programme, vous pouvez rencontrer des fichiers transitoires qui ne sont pas activement utilisés par le système ou tout autre logiciel.

### Mémoire auxiliaire ###

La mémoire virtuelle est utilisée dans les systèmes d'exploitation, cependant, les programmes qui utilisent d'énormes volumes d'informations peuvent avoir besoin de créer des documents temporaires.

### Communication interprocessus ###

La plupart des systèmes d'exploitation fournissent des primitives pour transmettre des données entre des programmes, tels que des canaux, des sockets ou la mémoire principale, mais la méthode la plus simple consiste à transférer des fichiers vers un fichier temporaire et à informer l'application réceptrice de l'emplacement du fichier temporaire.


## Spécification technique ##

L'obtention de noms de documents temporaires distinctifs est généralement fournie par les systèmes d'exploitation et les logiciels.
Les fichiers temporaires peuvent être générés en toute sécurité sur les systèmes POSIX à l'aide des fonctions de bibliothèque mkstemp ou tmpfile. Certains systèmes incluent l'application mktemp POSIX précédente (disparue depuis). Ces fichiers se trouvent généralement dans le répertoire temporaire habituel sur les plates-formes Unix dans /TMP, ou %TEMP% (il est spécifique à la connexion) sur les machines Windows.

Lorsque le programme s'arrête ou que le document est fermé, le fichier transitoire généré avec le fichier tmp est automatiquement supprimé. GetTempFileName (Windows) ou tmpnam (POSIX) peut être utilisé pour créer un nom de fichier temporaire qui durera plus longtemps que le programme qui l'a créé.

## Référence ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
