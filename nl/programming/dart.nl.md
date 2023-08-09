---
date: 2019-10-11
keywords: dart, .dart, dart-bestandsindeling, dart-bestand, hoe dart-bestanden worden uitgevoerd, .dart-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dart-bestandsindeling
linktitle: Dart
description: "Meer informatie over de Dart-bestandsindeling en API's die Dart-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Wat is een Dart-bestand? ##

Een Dart-bestand bevat de broncode van de Dart-programmeertaal, een voor de klant geoptimaliseerde programmeertaal die is ontwikkeld door Google en die wordt gebruikt om apps te bouwen voor mobiel, desktop, web, Iot (Internet of things) enz. Dart is een objectgeoriënteerde taal met een syntaxis vergelijkbaar met C. Dart kan worden gecompileerd naar JavaScript of native code. U kunt de Dart-bestanden in de beroemde webbrowser uitvoeren, net zoals u een javascript-bestand kunt uitvoeren. Een opdrachtregelprogramma dat bekend staat als de virtuele Dart-machine en die bij de Dart SDK-can wordt geleverd, wordt ook gebruikt om de Dart-bestanden te compileren en uit te voeren.

## Korte geschiedenis ##

Het Dart-project is opgericht door Lars Bak en Kasper Lund en de eerste versie werd uitgebracht op 14 november 2013. In het begin werd de Dart bekritiseerd vanwege de webfragmentatie vanwege de plannen om een Dart-VM in Google Chrome op te nemen. Die plannen werden geschrapt en Dart concentreerde zich op het compileren naar JavaScript met de release van versie 1.9 in 2015.

Dart 2.0 werd uitgebracht in augustus 2018, waarin de extensie dart2native werd geïntroduceerd die Dart-code compileerde naar native Linux-, Windows- en macOS-platforms. Deze extensie maakte zelfstandige uitvoerbare bestanden mogelijk waardoor de Dart SDK niet nodig was om Dart-apps op die platforms uit te voeren. Deze extensie is ook geïntegreerd met Flutter, waardoor het mogelijk is om platformonafhankelijke apps te maken.

ECMA heeft Dart gestandaardiseerd met de eerste editie in juli 2014 en de tweede editie in december 2014.


## Dart-code uitvoeren/uitvoeren ##

Dartcode kan op de volgende manieren worden uitgevoerd:

- **Gecompileerd als JavaScript**:</br> De Dart-code wordt gecompileerd naar JavaScript met behulp van de dart2js-compiler. De gecompileerde JavaScript-code is compatibel met alle belangrijke webbrowsers.
- **Zelfstandig**:</br> De Dart Software Development Kit (SDK) wordt geleverd met een stand-alone Dart VM waarmee Dart-code kan worden uitgevoerd in de opdrachtregelinterface. Dart wordt geleverd met een complete standaardbibliotheek waarmee gebruikers volledig functionele apps kunnen schrijven.
- **Ahead-of-time (AOT) samengesteld**:</br> Dartcode kan AOT-gecompileerd worden tot machinecode waarmee mobiele apps met Flutter kunnen worden gebouwd.
- **Oorspronkelijk**:</br> Met de dart2native-compiler kan Dart-code worden gecompileerd tot zelfstandige uitvoerbare bestanden die op Windows, Linux en macOS kunnen worden uitgevoerd.

## Dart-bestandsindeling ##

Dart is een objectgeoriënteerde taal in C-stijl die interfaces, mixins, abstracte klassen, gereïficeerde generieke termen en type-interface ondersteunt.

### Syntaxis ###

Hieronder volgen enkele voorbeelden van de Dart-syntaxis.

#### Afdrukken naar console ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Loops en arrays ####

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

#### Functies ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Klassen ####

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

Mixins zijn normale klassen waaruit we methoden/variabelen kunnen lenen zonder ze te erven. Dit wordt gedaan door het sleutelwoord *"with"* te gebruiken.

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

## Referenties ##

- [Dart (programmeertaal) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

