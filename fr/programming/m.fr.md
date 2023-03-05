{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Fichier de code source Matlab",
  "description":"En savoir plus sur le fichier de code source Matlab .m et les API qui peuvent créer et ouvrir des fichiers MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Fichiers de code source Matlab

## Qu'est-ce qu'un fichier M (Matlab) ?

Un fichier avec l'extension .m est un fichier de code source utilisé par Matlab, une plate-forme de programmation et de calcul numérique utilisée pour l'analyse, le développement d'algorithmes et la modélisation de simulation. Comme d'autres formats de fichiers de programmation, un fichier M contient du code source qui exécute des commandes Matlab pour tracer des graphiques, exécuter des simulations et d'autres opérations mathématiques. Une seule simulation Matlab peut s'étendre sur plusieurs fichiers .m de ce type qui peuvent classer l'application en scripts, classes, fonctions ou déclarations. Les fichiers Matlab M peuvent être ouverts avec n'importe quel éditeur de texte.

## Format de fichier Matlab M - Plus d'informations

Les fichiers Matlab .m sont des fichiers texte contenant du code de programmation dans le langage de programmation Matlab. Ceux-ci peuvent être ouverts et modifiés dans n'importe quel éditeur de texte, et sauvegardés pour être exécutés dans le logiciel Matlab. Matlab lui-même contient un éditeur en direct qui est utilisé pour créer des scripts qui sont une combinaison de code, de sortie et de texte formaté.

### Fichiers de fonctions Matlab

Comme d'autres langages de programmation, vous pouvez créer un fichier .m qui contient uniquement la définition d'une fonction qui exécute une tâche spécifique uniquement. Ces fichiers sont également enregistrés avec l'extension .m et implémentent les fonctionnalités liées à cette fonction uniquement.

### Exemple de fichier .M

Voici un exemple de fichier de fonction Matlab qui calcule le temps nécessaire pour qu'un objet tombe de la hauteur h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Pour appeler cette fonction depuis l'éditeur Matlab ou depuis un autre fichier .m, le code suivant peut être utilisé.
```C++
TimeToGround(100)
```

## Références

* [Matlab - Formats de fichiers pris en charge](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Utilisation de Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Fichier d'implémentation d'Objective-C

## Qu'est-ce qu'un fichier M (Objective-C) ?

Un fichier M est également appelé fichier d'implémentation qui contient le code source d'une classe écrite en langage Objective-C, un langage de programmation utilisé pour écrire des applications logicielles pour OS X et iOS. Objective-C est le principal langage de programmation utilisé par les principales API d'Apple, Cocoa et Cocoa Touch, pour ces plates-formes. Une seule application logicielle développée dans ce langage peut contenir plusieurs fichiers .m, contenant l'implémentation des classes du programme. Ceux-ci peuvent être ouverts à l'aide d'Apple XCode, jEdit et d'autres éditeurs de texte courants.

## Format de fichier Objective-C M - Plus d'informations

Les fichiers M sont écrits au format texte brut en utilisant la syntaxe de programmation d'Objective-C. Chaque méthode d'une classe doit être définie avec tout son code nécessaire dans ces fichiers d'implémentation. Ces fichiers M d'implémentation peuvent importer un ou plusieurs fichiers d'en-tête .h selon les besoins. L'instruction import indique au compilateur où trouver le fichier d'en-tête qui appartient à ce fichier d'implémentation. L'instruction d'importation est écrite comme suit.

```C++
#import "network.h"
```

Chaque implémentation de fichier M commence alors par la directive `@implementation`, suivie du nom du fichier de classe d'implémentation. Ceci est ensuite suivi par toutes les implémentations de méthodes qui sont déclarées dans le fichier d'en-tête.

### Exemple de format de fichier M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Références
* [À propos d'Objective C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Guide d'Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

