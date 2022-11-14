{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "fichier", "extension", "format de fichier", "CSharp", "Langage de programmation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - Fichier de code CSharp",
  "description":"En savoir plus sur le format de fichier CS et les API qui peuvent créer et ouvrir des fichiers CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier CS ?

Les fichiers avec l'extension .cs sont des fichiers de code source pour le langage de programmation C#. Introduit par Microsoft pour une utilisation avec le .NET Framework, le format de fichier fournit le langage de programmation de bas niveau pour écrire du code qui est compilé pour générer le fichier de sortie final sous la forme d'un EXE ou d'une DLL. Ceux-ci peuvent être créés et compilés avec Microsoft Visual Studio. Microsoft Visual Studio Express peut également être utilisé pour créer et mettre à jour de tels fichiers qui est un IDE gratuit. Les fichiers CS sont utilisés pour le développement d'applications qui peuvent aller de simples applications de bureau à des programmes plus complexes. Un projet Visual Studio simple [solution](/fr/programming/sln/) créé avec le langage C# peut comprendre un ou plusieurs de ces fichiers. Les fichiers marqués pour inclusion dans la compilation sont répertoriés dans le fichier [CSPROJ](/fr/programming/csproj/) qui fait partie du projet et indique au compilateur d'utiliser les fichiers marqués.

## Format de fichier CS ##

Les fichiers CS sont des formats de fichiers texte qui peuvent être ouverts dans n'importe quel éditeur de texte pour être modifiés. Cependant, lorsqu'il est ouvert dans un IDE pris en charge avec une coloration syntaxique appropriée, le code est facile à lire et à organiser. Un simple fichier CS contient :

* Déclaration des espaces de noms - Pour faire référence à une fonctionnalité particulière définie par cet espace de noms spécifique
* Déclaration de variables - Pour déclarer des variables au niveau de la classe pour l'implémentation particulière
* Déclaration des méthodes - Pour déclarer la déclaration des méthodes pour la fonctionnalité particulière

### Syntaxe ###

* Les points-virgules sont utilisés pour indiquer la fin d'une instruction.
* Les accolades sont utilisées pour regrouper les déclarations. Les instructions sont généralement regroupées en méthodes (fonctions), les méthodes en classes et les classes en espaces de noms.
* Les variables sont attribuées à l'aide d'un signe égal, mais comparées à l'aide de deux signes égal consécutifs.
* Les crochets sont utilisés avec les tableaux, à la fois pour les déclarer et pour obtenir une valeur à un index donné dans l'un d'entre eux.

### Exemple ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

