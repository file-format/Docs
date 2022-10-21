---
date: 2019-10-11
keywords: "Dart, .dart, Dart-Dateiformat, Dart-Datei, Ausführen von Dart-Dateien, Erweiterung .dart"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "Dart-Dateiformat"
linktitle: "Pfeil"
description: "Erfahren Sie mehr über das Dart-Dateiformat und APIs, die Dart-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Was ist eine Dart-Datei? ##

Eine Dart-Datei enthält den Quellcode der Programmiersprache Dart, einer von Google entwickelten Client-optimierten Programmiersprache, die zum Erstellen von Apps für Mobilgeräte, Desktop, Web, IoT (Internet der Dinge) usw. verwendet wird. Dart ist eine objektorientierte Sprache mit einer ähnlichen Syntax wie C. Dart kann entweder in JavaScript oder nativen Code kompiliert werden. Sie können die Dart-Dateien in einem bekannten Webbrowser ausführen, genauso wie Sie eine Javascript-Datei ausführen können. Ein Befehlszeilentool namens Dart Virtual Machine, das mit Dart SDK geliefert wird, wird auch zum Kompilieren und Ausführen der Dart-Dateien verwendet.

## Kurze Geschichte ##

Das Dart-Projekt wurde von Lars Bak und Kasper Lund gegründet und die erste Version wurde am 14. November 2013 veröffentlicht. Anfangs wurde Dart für die Webfragmentierung aufgrund der Pläne zur Einbindung einer Dart-VM in Google Chrome kritisiert. Diese Pläne wurden verworfen und Dart konzentrierte sich mit der Veröffentlichung von Version 1.9 im Jahr 2015 auf die Kompilierung zu JavaScript.

Dart 2.0 wurde im August 2018 veröffentlicht, in dem die Erweiterung dart2native eingeführt wurde, die Dart-Code für native Linux-, Windows- und macOS-Plattformen kompilierte. Diese Erweiterung ermöglichte eigenständige ausführbare Dateien, aufgrund derer das Dart SDK nicht erforderlich war, um Dart-Apps auf diesen Plattformen auszuführen. Diese Erweiterung ist auch in Flutter integriert, sodass plattformübergreifende Apps erstellt werden können.

ECMA standardisierte Dart mit der ersten Ausgabe im Juli 2014 und der zweiten Ausgabe im Dezember 2014.


## Wie man Dart-Code ausführt/ausführt ##

Dart-Code kann auf folgende Weise ausgeführt werden:

- **Als JavaScript kompiliert**:</br> Der Dart-Code wird mithilfe des dart2js-Compilers in JavaScript kompiliert. Der kompilierte JavaScript-Code ist mit allen gängigen Webbrowsern kompatibel.
- **Eigenständige**:</br> Das Dart Software Development Kit (SDK) wird mit einer eigenständigen Dart-VM geliefert, mit der Dart-Code in der Befehlszeilenschnittstelle ausgeführt werden kann. Dart wird mit einer vollständigen Standardbibliothek geliefert, die es Benutzern ermöglicht, voll funktionsfähige Apps zu schreiben.
- **Ahead-of-Time (AOT) zusammengestellt**:</br> Dart-Code kann AOT-kompiliert werden, um Maschinencode zu erstellen, mit dem mobile Apps mit Flutter erstellt werden können.
- **Einheimisch**:</br> Mit dem dart2native-Compiler kann Dart-Code in eigenständige ausführbare Dateien kompiliert werden, die unter Windows, Linux und macOS ausgeführt werden können.

## Dart-Dateiformat ##

Dart ist eine objektorientierte Sprache im C-Stil, die Schnittstellen, Mixins, abstrakte Klassen, verdinglichte Generika und Typschnittstellen unterstützt.

### Syntax ###

Im Folgenden finden Sie einige Beispiele für die Dart-Syntax.

#### Auf Konsole drucken ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Schleifen und Arrays ####

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

#### Funktionen ####

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

Mixins sind normale Klassen, von denen wir Methoden/Variablen ausleihen können, ohne sie zu erben. Verwenden Sie dazu das Schlüsselwort *"with"*.

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

## Verweise ##

- [Dart (Programmiersprache) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(Programmiersprache))
- [Dart](https://dart.dev/)

