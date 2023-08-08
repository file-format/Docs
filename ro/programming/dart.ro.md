---
date: 2019-10-11
keywords: dart, .dart, format de fișier dart, fișier dart, cum să rulați fișiere dart, extensia .dart
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier Dart
linktitle: Dart
description: "Aflați despre formatul de fișier Dart și despre API-urile care pot crea și deschide fișiere Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Ce este un fișier Dart? ##

Un fișier Dart conține codul sursă al limbajului de programare Dart, care este un limbaj de programare optimizat pentru client, dezvoltat de Google, care este utilizat pentru a crea aplicații pentru mobil, desktop, web, Iot (Internetul lucrurilor) etc. Dart este un limbaj orientat pe obiecte. cu o sintaxă similară cu C. Dart poate fi compilat fie în JavaScript, fie în cod nativ. Puteți rula fișierele Dart într-un browser web celebru, așa cum puteți rula un fișier javascript. Un instrument de linie de comandă cunoscut sub numele de mașină virtuală Dart, care vine cu Dart SDK can este, de asemenea, utilizat pentru a compila și rula fișierele Dart.

## Scurt istoric ##

Proiectul Dart a fost fondat de Lars Bak și Kasper Lund, iar prima versiune a fost lansată pe 14 noiembrie 2013. La început, Dart a fost criticat pentru fragmentarea web din cauza planurilor de includere a unui Dart VM în Google Chrome. Aceste planuri au fost abandonate și Dart s-a concentrat pe compilarea în JavaScript odată cu lansarea versiunii 1.9 în 2015.

Dart 2.0 a fost lansat în august 2018 în care a fost introdusă extensia dart2native care a compilat codul Dart pe platformele native Linux, Windows, macOS. Această extensie a activat executabile autonome, datorită cărora SDK-ul Dart nu era necesar pentru a rula aplicații Dart pe acele platforme. Această extensie a fost integrată și cu Flutter, făcând posibilă crearea de aplicații multiplatformă.

ECMA a standardizat Dart cu prima ediție în iulie 2014 și a doua ediție în decembrie 2014.


## Cum să rulezi/execuți codul Dart ##

Codul Dart poate rula în următoarele moduri:

- **Compilate ca JavaScript**:</br> Codul Dart este compilat în JavaScript utilizând compilatorul dart2js. Codul JavaScript compilat este compatibil cu toate browserele web majore.
- **De sine stătătoare**:</br> Kitul de dezvoltare software (SDK) Dart este livrat cu un VM Dart autonom care permite rularea codului Dart în interfața de linie de comandă. Dart este livrat cu o bibliotecă standard completă care permite utilizatorilor să scrie aplicații complet funcționale.
- **Ahead-of-time (AOT) compilat**:</br> Codul Dart poate fi compilat prin AOT în codul mașinii care permite crearea aplicațiilor mobile cu Flutter.
- **Nativ**:</br> Cu compilatorul dart2native, codul Dart poate fi compilat în executabile autonome care pot rula pe Windows, Linux și macOS.

## Format fișier Dart ##

Dart este un limbaj orientat pe obiecte în stil C care acceptă interfețe, mix-uri, clase abstracte, generice reificate și interfețe de tip.

### Sintaxă ###

Următoarele sunt câteva exemple de sintaxă Dart.

#### Print to Console ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Bucle și matrice ####

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

#### Funcții ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Clase ####

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

Mixin-urile sunt clase normale de la care putem împrumuta metode/variabile fără a le moșteni. Acest lucru se face folosind cuvântul cheie *"cu"*.

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

## Referințe ##

- [Dart (limbaj de programare) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

