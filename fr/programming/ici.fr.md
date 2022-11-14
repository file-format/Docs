{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "fichier", "extension", "format de fichier", "implémentation ICI", "Guide de programmation", "exemple ici", "langage de programmation ICI", "modules d'ICI", "modèle de données d'ICI ", "documentation d'ICI", "langage ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Fichier de langage de programmation",
  "description":"En savoir plus sur le format de fichier ICI et les API qui peuvent créer et ouvrir des fichiers ICI.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Qu'est-ce qu'un fichier ICI ?

Un langage de programmation à usage général qui est interprété et contient plusieurs fonctionnalités telles que le typage dynamique ainsi que les types de données flexibles est connu sous le nom de langage de programmation ICI (pas un acronyme). Il est considéré comme similaire au langage [Perl](/fr/programming/pl/). Ce langage ICI comprend des constructions de contrôle de flux et contient également certains opérateurs du langage C. Ce n'est pas un langage orienté objet, mais certaines des fonctionnalités de la POO peuvent être atteintes par une méthode d'héritage spécifique connue sous le nom de superstructures. Semblable à [C](/fr/programming/c), ce langage de programmation ICI a la même interface système et une bibliothèque standard pour les fonctions intégrées.


## Bref historique ##

À la fin des années 1980, il a été développé par Tim Long en tant que langage de programmation interprété à usage général. La plupart des fonctionnalités de ce langage sont similaires à C et il peut également réaliser certaines fonctionnalités en appliquant certaines méthodes spéciales. Ce langage appartient au domaine public et est disponible en tant que langage revendable et personne n'est tenu de mentionner d'où il a obtenu le code source. La documentation d'ICI est sous copyright de Canon Information System Research Australia.

## Spécification technique ##

Deux types de données différents sont utilisés dans ce langage. Ces deux types de données sont primitifs et agrégés. Les deux incluent des expressions différentes en fonction de leur composition prédéfinie dans la langue. Différents modules tels que imbriqués et sous-programmes sont pris en charge par ce langage. Comme certaines de ses propriétés sont similaires à Perl, il a une intégration stricte avec les expressions régulières.

Les ensembles sont confinés pour être hétérogènes et imbriqués. Ces ensembles prennent en charge les opérations d'ensemble couramment utilisées telles que Union et Intersection, etc. Il est principalement utilisé comme langage pour la mise en œuvre de base des applications détenues par des organisations multinationales.

Presque tous les types de programmes peuvent être écrits dans ce langage et la plupart des programmes spécifiques qui impliquent des structures de données complexes sont écrits dans le langage de programmation ICI. Les applications peuvent impliquer la mise en œuvre de l'ICI d'une manière telle qu'elles devraient y être écrites. Des parties fonctionnelles de l'application peuvent être implémentées par les modules d'ICI. Le langage d'ICI ressemble quelque peu au langage C, mais le modèle de données d'ICI est de niveau assez supérieur et différent avec des types tels que des dictionnaires (struct), des ensembles, des tableaux dynamiques, des expressions régulières et des chaînes (réelles).


## Exemple de format de fichier ICI ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Référence ##

* [Langage de programmation ICI] (http://atrn.org/ici/doc/ici.html)



