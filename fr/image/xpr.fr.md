{
  "date" : "2022-03-21",
  "keywords" :[ "fichier xpr", "format de fichier xpr", "qu'est-ce qu'un fichier xpr", "fichier", "exemple xpr", "extension de fichier xpr","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier XPR - Fichier graphique Microsoft Expression Design",
  "description":"En savoir plus sur le format de fichier XPR et les API qui peuvent créer et ouvrir des fichiers XPR.",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## Qu'est-ce qu'un fichier XPR ?

Un fichier XPR est un fichier d'image vectorielle créé avec le logiciel Microsoft Expression Graphics (EGD) désormais abandonné. Il contient des informations graphiques pouvant être utilisées comme maquette d'interface utilisateur. Les fichiers XPR ont ensuite été remplacés par des fichiers .design dans Microsoft Expression Design. Les fichiers XPR peuvent être ouverts avec Microsoft Expression Studio qui a été abandonné depuis un certain temps maintenant.

## Vulnérabilité du format de fichier XPR

Les fichiers XPR ont été identifiés comme bénéficiant d'une vulnérabilité dans Microsoft Expression Design, permettant l'exécution de code à distance. Dans le problème signalé, si un utilisateur ouvrait un fichier .xpr légitime placé dans le répertoire réseau avec le fichier de bibliothèque de liens dynamiques (DLL), Microsoft Expression Design pouvait tenter de charger le fichier DLL et d'exécuter le code qu'il contenait. Cela a ensuite été corrigé par Microsoft dans une mise à jour de sécurité.

## Références

* [Une vulnérabilité dans la conception d'expression pourrait permettre l'exécution de code à distance (2651018)](https://docs.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

