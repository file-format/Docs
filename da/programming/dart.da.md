---
date: 2019-10-11
keywords: dart, .dart, dart file format, dart file, how to run dart files, .dart extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dart filformularat
linktitle: Dart
description: Ltjene om Dart-filformat og API'er, der kan oprette og åbne Dart-fils.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Hvad er en Dart-fil? ##

En Dart-fil indeholder kildekoden til Dart-programmeringssproget, som er et klientoptimeret programmeringssprog udviklet af Google, der bruges til at bygge apps til mobil, desktop, web, Iot (Internet of things) osv. Dart er et objektorienteret sprog med en syntaks svarende til C. Dart kan kompileres til enten JavaScript eller native kode. Du kan køre Dart-filerne i den berømte webbrowser, ligesom du kan køre en javascript-fil. Et kommandolinjeværktøj kendt som Dart virtuel maskine, som leveres med Dart SDK can, bruges også til at kompilere og køre Dart-filerne.

## Kort historie ##

The Dart project was founded by Lars Bak and Kasper Lund and the first version was released on 14th November 2013. I begyndelsen blev Dart kritiseret for webfragmenteringen på grund af planerne om at inkludere en Dart VM i Google Chrome. Disse planer blev droppet, og Dart fokuserede på at kompilere til JavaScript med udgivelsen af version 1.9 i 2015.

Dart 2.0 blev udgivet i august 2018, hvor dart2native-udvidelsen blev introduceret, der kompilerede Dart-kode til native Linux, Windows, macOS-platforme. Denne udvidelse aktiverede selvstændige eksekverbare filer, hvorfor Dart SDK ikke var påkrævet for at køre Dart-apps på disse platforme. Denne udvidelse er også integreret med Flutter, hvilket gør det muligt at skabe apps på tværs af platforme.

ECMA standardiserede Dart med den første udgave i juli 2014 og den anden udgave i december 2014.


## Sådan kører/udfører du Dart-kode ##

Dart-kode kan køre på følgende måder:

- **Kompileret som JavaScript**:</br> Dart-koden kompileres til JavaScript ved at bruge dart2js-kompileren. Den kompilerede JavaScript-kode er kompatibel med alle større webbrowsere.
- **Stand-alone**:</br> Dart Software Development Kit (SDK) leveres med en selvstændig Dart VM, der tillader Dart-kode at køre i kommandolinjegrænsefladen. Dart leveres med et komplet standardbibliotek, der giver brugerne mulighed for at skrive fuldt funktionelle apps.
- **Ahead-of-time (AOT) kompileret**:</br> Dartkode kan AOT-kompileres til maskinkode, der gør det muligt at bygge mobilapps med Flutter.
- **Native**:</br> Med dart2native-kompileren kan Dart-kode kompileres til selvstændige eksekverbare filer, der kan køre på Windows, Linux og macOS.

## Dart-filformat ##

Dart er et C-stil objektorienteret sprog, der understøtter grænseflader, mixins, abstrakte klasser, reificerede generiske og typegrænseflader.

### Syntaks ###

Følgende er nogle eksempler på Dart-syntaks.

#### Udskriv til konsol ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Sløjfer og arrays ####

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

#### Funktioner ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Klasser ####

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

Mixins er normale klasser, hvorfra vi kan låne metoder/variabler uden at arve dem. Dette gøres ved at bruge nøgleordet *with*.

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

## Referencer ##

- [Dart (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

