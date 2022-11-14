---
date: 2019-10-11
keywords: dart, .dart, format de fichier dart, fichier dart, comment exécuter des fichiers dart, extension .dart
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier fléchette
linktitle: Dart
description: "Découvrez le format de fichier Dart et les API qui peuvent créer et ouvrir des fichiers Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Qu'est-ce qu'un fichier Dart ? ##

Un fichier Dart contient le code source du langage de programmation Dart qui est un langage de programmation optimisé pour le client développé par Google et utilisé pour créer des applications pour mobile, ordinateur de bureau, Web, Iot (Internet des objets), etc. Dart est un langage orienté objet avec une syntaxe similaire à C. Dart peut être compilé en JavaScript ou en code natif. Vous pouvez exécuter les fichiers Dart dans un navigateur Web célèbre, tout comme vous pouvez exécuter un fichier javascript. Un outil de ligne de commande connu sous le nom de machine virtuelle Dart fourni avec Dart SDK peut également être utilisé pour compiler et exécuter les fichiers Dart.

## Bref historique ##

Le projet Dart a été fondé par Lars Bak et Kasper Lund et la première version a été publiée le 14 novembre 2013. Au début, le Dart a été critiqué pour la fragmentation du Web en raison des projets d'inclusion d'une machine virtuelle Dart dans Google Chrome. Ces plans ont été abandonnés et Dart s'est concentré sur la compilation en JavaScript avec la sortie de la version 1.9 en 2015.

Dart 2.0 a été publié en août 2018 dans lequel l'extension dart2native a été introduite qui compilait le code Dart sur les plates-formes Linux, Windows et macOS natives. Cette extension activait des exécutables autonomes grâce auxquels le SDK Dart n'était pas nécessaire pour exécuter des applications Dart sur ces plates-formes. Cette extension est également intégrée à Flutter permettant de créer des applications multiplateformes.

L'ECMA a normalisé Dart avec la première édition en juillet 2014 et la deuxième édition en décembre 2014.


## Comment lancer/exécuter le code Dart ##

Le code Dart peut s'exécuter de la manière suivante :

- **Compilé en JavaScript** :</br> Le code Dart est compilé en JavaScript à l'aide du compilateur dart2js. Le code JavaScript compilé est compatible avec tous les principaux navigateurs Web.
- **Autonome** :</br> Le kit de développement logiciel Dart (SDK) est livré avec une machine virtuelle Dart autonome qui permet au code Dart de s'exécuter dans l'interface de ligne de commande. Dart est livré avec une bibliothèque standard complète qui permet aux utilisateurs d'écrire des applications entièrement fonctionnelles.
- **Compilation anticipée (AOT)** :</br> Le code Dart peut être compilé par AOT en code machine qui permet de créer des applications mobiles avec Flutter.
- **Originaire de**:</br> Avec le compilateur dart2native, le code Dart peut être compilé en exécutables autonomes pouvant s'exécuter sous Windows, Linux et macOS.

## Format de fichier fléchette ##

Dart est un langage orienté objet de style C qui prend en charge les interfaces, les mixins, les classes abstraites, les génériques réifiés et l'interface de type.

### Syntaxe ###

Voici quelques exemples de syntaxe Dart.

#### Imprimer sur la console ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Boucles et tableaux ####

```dart
// loops and arrays
var names = {
  'John',
  'James',
  'Rose',
};
main() {
  for (var name in names) {
    print(name);
  }
}
```

#### Les fonctions ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Des classes ####

```dart
// classes
abstract class Person {
  detail();
}

class Student implements Person {
  String firstName = "Jack";
  String lastName = "Wick";
  detail() => print("Student: $firstName $lastName");
}

main() {
  // The 'new' keyword is optional.
  Student student = Student();
  student.detail();
}
```

#### Mixins ####

Les mixins sont des classes normales auxquelles on peut emprunter des méthodes/variables sans en hériter. Ceci est fait en utilisant le mot-clé *"with"*.

```dart
class B {  
  method(){
     ....
  }
}

class A with B {
  ....
     ......
}
void main() {
  A a = A();
  a.method();  //We are able to access the method of B class without inheriting from it.
}
```

## Références ##

- [Dart (langage de programmation) - Wikipédia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Fléchette](https://dart.dev/)

