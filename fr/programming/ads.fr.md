
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier ADS - Format de fichier de spécification Ada",
  "description":"Découvrez ce qu'est le format de fichier ADS avec des exemples et des API qui peuvent créer et ouvrir des fichiers ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Qu'est-ce qu'un fichier ADS ?

Un fichier ADS est un fichier de spécification pour un projet de programmation Ada. Il est similaire à une classe pour Java, ou à la paire d'en-tête et d'implémentation dans le cas de C++. Les spécifications publiques et privées du package Ada sont stockées dans le fichier .ads. Le fichier .adb, en revanche, contient l'implémentation ou les corps Ada. Comme [C++](/fr/programming/cpp/), Ada offre une séparation entre les spécifications et les implémentations indépendantes de la POO.

Les fichiers ADS peuvent être ouverts dans n'importe quel éditeur de texte tel que Microsoft Notepad, Notepad ++ et Atom.

## Format de fichier ADS

Les fichiers ADS sont au format de fichier texte simple et peuvent être ouverts/modifiés avec n'importe quel éditeur de texte. Les packages Ada peuvent être organisés en hiérarchies. Une unité enfant peut être déclarée de la manière suivante :

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Références

* [Packages Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

