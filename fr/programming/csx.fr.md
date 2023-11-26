{
"date": "2023-05-15",
  "keywords": [
"fichier csx",
"qu'est-ce qu'un fichier csx",
"que contient le fichier csx",
"quel est le format du fichier csx",
"déposer",
"extension de fichier CSX",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier CSX - Script Visual C#",
  "description":"Découvrez le format CSX et les API permettant de créer et d'ouvrir des fichiers CSX.",
"linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
"parent": "programmation"
}
},
"derniermod": "2023-05-15"
}

## Qu'est-ce qu'un fichier CSX ?

Visual C# Script (également connu sous le nom de CSX) est un format de fichier utilisé par le moteur de script Roslyn dans l'écosystème .NET de Microsoft. Les fichiers CSX contiennent du code C# qui peut être exécuté directement sans avoir besoin d'une étape de compilation distincte.

Le format CSX est spécifique à l'écosystème Microsoft et n'est pas un format de fichier largement utilisé en programmation générale. Les fichiers CSX sont souvent utilisés dans des scénarios où une fonctionnalité de prototypage ou de script rapide est requise. Ils vous permettent de créer et d'exécuter des programmes C# de manière plus légère que la création d'une application compilée à part entière.

Pour exécuter des fichiers CSX, vous pouvez utiliser des outils tels que .NET Interactive Notebooks, qui fournissent un environnement interactif pour exécuter du code C#. Visual Studio Code avec l'extension C# et le SDK .NET Core peut également être utilisé pour travailler avec des fichiers CSX.

## Que contient le fichier CSX ?

Un fichier CSX (C# Script) contient du code C# qui peut être exécuté directement. Il peut inclure n'importe quel code C# valide tel que des déclarations de variables, des fonctions, des classes et d'autres constructions de programmation.

Voici un exemple de ce que le fichier CSX peut contenir :

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

Les fichiers CSX peuvent également inclure des instructions d'importation, des références de bibliothèques externes et d'autres fonctionnalités du langage C# pour prendre en charge les fonctionnalités du code. Le code est interprété et exécuté à la volée sans nécessiter de compilation, ce qui le rend adapté aux tâches de script et de prototypage rapide.

## Quel est le format du fichier CSX ?

Le format CSX (C# Script) suit un format texte simple. Il porte généralement l'extension de fichier .csx pour le différencier des fichiers de code source C# classiques (.cs).

Les fichiers CSX peuvent être modifiés à l'aide de n'importe quel éditeur de texte ou environnement de développement intégré (IDE) prenant en charge la coloration syntaxique C#. Une fois le fichier CSX prêt, il peut être exécuté à l'aide d'outils tels que .NET Interactive Notebooks, l'interface de ligne de commande (CLI) .NET Core ou un IDE avec prise en charge des scripts C#.

## Les références
* [Programmation C# avec Visual Studio Code](https://code.visualstudio.com/docs/langages/csharp)

