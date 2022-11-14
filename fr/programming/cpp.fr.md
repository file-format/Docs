{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "fichier", "extension", "format de fichier", "C++", "Langage de programmation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - Fichier de code source C++",
  "description":"En savoir plus sur le format de fichier CPP et les API qui peuvent créer et ouvrir des fichiers CPP.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier C++ ?

Les fichiers avec l'extension de fichier CPP sont des fichiers de code source pour les applications écrites en langage de programmation C++. Un seul projet C++ peut contenir plusieurs fichiers CPP en tant que code source de l'application. Un tel projet est constitué de différents types de fichiers, dont les fichiers CPP sont appelés fichiers d'implémentation car ils contiennent toutes les définitions des méthodes déclarées dans le fichier d'en-tête (.h). Le projet C++ dans son ensemble donne une application exécutable lorsqu'il est compilé dans son ensemble.

## Structure du dossier RPC

Une structure de fichier CPP est simple par rapport aux fichiers d'en-tête. L'objectif principal d'un tel fichier d'implémentation est de séparer l'interface de l'implémentation. Cela se traduit par des déclarations de toutes les fonctions membres dans un fichier d'en-tête et leurs détails dans le fichier CPP. Un fichier d'implémentation CPP peut être utilisé comme simple fichier pour écrire une application ou comme implémentation de classe.

### Implémentation indépendante

Un fichier CPP, lorsqu'il est utilisé en tant qu'application indépendante, peut contenir toutes les implémentations qu'il contient sans qu'il soit nécessaire de déclarer les méthodes dans le fichier d'en-tête. Une telle implémentation se compose de toutes les méthodes définies dans le fichier d'implémentation où l'entrée de l'application est régie par une méthode principale qui prend comme arguments une entrée utilisateur facultative. Il peut également inclure toutes les bibliothèques de la bibliothèque standard C++ à utiliser par toutes les méthodes déclarées dans le fichier.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Implémentation de classe

Dans la programmation orientée objet (POO), un fichier CPP est utilisé comme définition de classe. Dans ce cas, tous les membres de données de classe et les fonctions membres sont déclarés dans le fichier d'en-tête. Chaque fichier d'en-tête peut à son tour faire référence à des méthodes de bibliothèque standard. Le fichier CPP de définition de classe fait référence au fichier d'en-tête dans une instruction include au début du fichier. Généralement, les développeurs de logiciels incluent des commentaires au début d'un tel fichier d'implémentation de classe qui fournissent des informations sur le contenu réel du fichier, les détails de l'auteur et la date d'implémentation. Dans de tels cas, les fichiers d'implémentation d'en-tête doivent avoir les mêmes noms. Un exemple d'un tel fichier d'en-tête et d'implémentation est le suivant.

### En tête de fichier

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### Fichier de mise en œuvre du CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Références

* [Implémentation de classe - Par Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

