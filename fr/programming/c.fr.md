{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c","qu'est-ce qu'un fichier ac","comment ouvrir un fichier c", "extension", "fichier", "fichier c","format de fichier c", "extension de fichier c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier de programmation en langage C - C",
  "description":"En savoir plus sur le format de fichier C et les API qui peuvent créer et ouvrir des fichiers C.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Qu'est-ce qu'un fichier C ?

Un fichier enregistré avec l'extension de fichier c est un fichier de code source écrit en langage de programmation C. Le **fichier C** inclut toute la mise en œuvre des fonctionnalités de l'application sous la forme de code source. La déclaration du code source est écrite dans les fichiers d'en-tête qui sont enregistrés avec l'extension [.h](/fr/programming/h/). C++ est la forme moderne du langage C et est utilisé pour développer la plupart des logiciels de nos jours.

## Bref historique

Le langage C est né de la création de différents utilitaires pour le système d'exploitation UNIX. Denis Ritchie, l'homme derrière la création de ce langage de programmation, le travail a commencé à l'origine dans les années 1960 et au début des années 1970.

## Format de fichier C

Les fichiers C sont écrits au format de fichier texte brut en suivant la syntaxe du langage de programmation. Un fichier C typique aura :

* déclaration d'importation en haut du fichier pour importer tous les fichiers d'en-tête
* une ou plusieurs méthodes pour implémenter la fonctionnalité souhaitée

### Importation des en-têtes

Les fichiers d'en-tête, avec l'extension .h, contiennent les instructions d'inclusion nécessaires pour inclure d'autres fichiers de fonctionnalité dans le projet. De plus, ceux-ci contiennent les déclarations des méthodes définies dans le fichier d'implémentation. Les fichiers d'en-tête sont inclus à l'aide de l'instruction include, comme indiqué ci-dessous.

```
#include <filename.h>
```

### Implémentation du code source

La mise en œuvre réelle des exigences fonctionnelles est codée sous forme de méthodes dans le fichier C. Chaque méthode dans un fichier C a un type de retour, un nom de méthode et peut avoir des paramètres d'entrée. Si le type de retour n'est pas vide, la méthode peut renvoyer une valeur.

### Exemple de code C
Voici un exemple de programme :

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Références** ##

* [Implémentation de classe - Par Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

