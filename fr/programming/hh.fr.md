{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh","qu'est-ce qu'un fichier .hh","comment ouvrir un fichier .hh", "extension", "fichier", "fichier .hh","format de fichier .hh", " extension de fichier .hh","Exemple de fichier .HH"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - Format de fichier d'en-tête C++",
  "description":"En savoir plus sur le format de fichier HH et les API qui peuvent créer et ouvrir un fichier HH.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Qu'est-ce qu'un fichier HH ?

Un fichier avec l'extension .hh est un fichier d'en-tête C++ qui inclut la déclaration des variables, des constantes et des fonctions. Ces déclarations sont utilisées par les fichiers d'implémentation C++ correspondants, généralement enregistrés en tant que fichiers [.cpp](/fr/programming/cpp/) qui contiennent l'implémentation réelle de la logique utilisateur. Les fichiers d'en-tête .hh sont référencés dans les fichiers CPP d'implémentation à l'aide de la directive `#include`. Vous pouvez ajouter autant de fichiers d'en-tête que possible à votre projet C++ pour inclure des déclarations au niveau du projet.

## Format de fichier .HH

Un fichier .hh est un fichier texte brut qui est créé en gardant à l'esprit les règles de définition du fichier d'en-tête. Les informations les plus courantes déclarées dans un fichier .hh sont les suivantes.

**`Variables`** - Dans le cas de la programmation orientée objet (POO), un fichier d'en-tête de classe contient les définitions de toutes les variables de niveau de classe accessibles dans les fichiers de code source d'implémentation
**`Déclaration de méthodes`** - Toutes les déclarations de méthodes sont incluses dans les fichiers d'en-tête .h pour être accessibles dans plusieurs fichiers d'implémentation.
**`Définitions de fonctions non en ligne`** - Les fichiers d'en-tête peuvent également contenir des définitions de méthodes non en ligne.
**`Message Maps`** - Un fichier d'en-tête peut également contenir des cartes de messages dans le cas d'une implémentation de code source MFC. Dans ce cas, les cartes de message sont liées à l'implémentation de la fonctionnalité qui est liée aux éléments de l'interface utilisateur tels que le bouton, la case à cocher, les boutons radio, etc.

## Différence entre les fichiers .H et .HH

Apparemment, il n'y a pas de telle différence entre les fichiers d'en-tête .h et .hh autre que la manière recommandée de les utiliser pour les langages respectifs, c'est-à-dire [C](/fr/programming/c/) ou C++. Nommer vos fichiers d'en-tête en fonction de ces langages vous aide à les distinguer dans un grand projet qui peut être un mélange d'implémentations C et C++.

De plus, si les en-têtes sont séparés par extension, votre éditeur peut appliquer automatiquement la mise en forme appropriée pour respectivement.

Dans l'ensemble, la différenciation de ces deux formats de fichiers ne fera aucun mal, mais sera avantageuse, et est encouragée à suivre pour la distinction C et C++.

### Gardes d'en-tête

Les fichiers d'en-tête peuvent générer des erreurs complexes lorsque plusieurs déclarations sont incluses dans le même fichier à la suite de l'ajout d'autres fichiers d'en-tête. Ces définitions en double génèrent des erreurs de compilation. Cette situation problématique peut être évitée via un mécanisme appelé garde d'en-tête qui sont des directives de compilation conditionnelle comme indiqué ci-dessous.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Avec cet en-tête, le préprocesseur vérifie si le `ANY_UNIQUE_NAME_HERE_HPP` a déjà été défini. Si l'en-tête est inclus à plusieurs reprises dans le même fichier, le contenu de l'en-tête sera ignoré.

## Références

* [Fichiers d'en-tête - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Différence entre les formats de fichiers .h et .hh](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

