{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Fichier MDE - Qu'est-ce qu'un fichier MDE et comment l'ouvrir?",
  "description":"Découvrez le format de fichier MDE et les API permettant de créer et d'ouvrir des fichiers MDE.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-fr-mde"
    }
  },
  "lastmod" : "2023-12-03"
}

## Qu'est-ce qu'un fichier MDE ?

Un fichier .MDE est une version compilée d'une base de données Access (.mdb ou .accdb). Lorsque vous compilez une base de données Access dans un fichier .MDE, elle n'est plus modifiable à l'aide des outils de conception Access standard. L'objectif principal de la création d'un fichier .MDE est de distribuer une application de base de données sans exposer le code source d'origine.

## Format de fichier MDE

Un fichier MDE est créé en compilant le code VBA, les formulaires, les rapports et autres objets. Cela aboutit à la création du format de fichier binaire MDE. Le fichier .MDE résultant peut être distribué aux utilisateurs qui peuvent exécuter l'application mais ne peuvent pas modifier la conception ni afficher le code d'origine. Le fichier MDE est en fait la version compilée d'un [fichier .MDA](/database/mda/). La distribution de fichiers .MDE peut contribuer à protéger la propriété intellectuelle en empêchant les utilisateurs d'accéder ou de modifier le code source. Cela peut également améliorer les performances à mesure que le code est compilé et optimisé.

## Les références

* [Spécifications d'accès](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
