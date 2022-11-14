{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "fichier", "extension", "format de fichier", "Visual Basic", "Guide de programmation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Fichier de code Visual Basic",
  "description":"En savoir plus sur le format de fichier VB et les API qui peuvent créer et ouvrir des fichiers VB.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier VB ?

Un fichier VB est un fichier de code source créé en langage Visual Basic qui a été créé par Microsoft pour le développement d'applications .NET. Un autre langage similaire avec une syntaxe différente est C# dont les fichiers sont enregistrés avec l'extension de fichier [.CS](/fr/programming/cs/). Le format de fichier fournit le langage de programmation de bas niveau pour écrire du code qui est compilé pour générer le fichier de sortie final sous la forme d'un EXE ou d'une DLL. Ceux-ci peuvent être créés et compilés avec Microsoft Visual Studio. Microsoft Visual Studio Express peut également être utilisé pour créer et mettre à jour de tels fichiers qui est un IDE gratuit. Un projet Visual Studio simple [solution](/fr/programming/sln/) créé avec le langage VB peut comprendre un ou plusieurs de ces fichiers. Les fichiers marqués pour inclusion dans la compilation sont répertoriés dans le fichier [CSPROJ](/fr/programming/csproj/) qui fait partie du projet et indique au compilateur d'utiliser les fichiers marqués.

## Format de fichier VB - Plus d'informations

Les fichiers VB sont des formats de fichiers texte qui peuvent être ouverts dans n'importe quel éditeur de texte pour être modifiés. Cependant, lorsqu'il est ouvert dans un IDE pris en charge avec une coloration syntaxique appropriée, le code est facile à lire et à organiser. Un simple fichier VB contient :

* Déclaration des espaces de noms - Pour faire référence à une fonctionnalité particulière définie par cet espace de noms spécifique
* Déclaration de variables - Pour déclarer des variables au niveau de la classe pour l'implémentation particulière
* Déclaration des méthodes - Pour déclarer la déclaration des méthodes pour la fonctionnalité particulière

## Exemple de format de fichier VB

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



