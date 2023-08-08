---
date: 2019-10-11
keywords: dart, .dart, format pliku dart, plik dart, jak uruchamiać pliki dart, rozszerzenie .dart
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format pliku rzutki
linktitle: Dart
description: "Dowiedz się więcej o formacie plików Dart i interfejsach API, które umożliwiają tworzenie i otwieranie plików Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Co to jest plik Dart? ##

Plik Dart zawiera kod źródłowy języka programowania Dart, który jest zoptymalizowanym pod kątem klienta językiem programowania opracowanym przez Google, który jest używany do tworzenia aplikacji na urządzenia mobilne, komputery stacjonarne, Internet, Internet rzeczy itp. Dart to język zorientowany obiektowo ze składnią podobną do C. Dart można skompilować do kodu JavaScript lub natywnego. Możesz uruchomić pliki Dart w słynnej przeglądarce internetowej, tak jak możesz uruchomić plik javascript. Narzędzie wiersza poleceń znane jako maszyna wirtualna Dart, które jest dostarczane z pakietem Dart SDK, jest również używane do kompilowania i uruchamiania plików Dart.

## Krótka historia ##

Projekt Dart został założony przez Larsa Baka i Kaspera Lunda, a pierwsza wersja została wydana 14 listopada 2013 roku. Na początku Dart był krytykowany za fragmentację sieci w związku z planami włączenia Dart VM do Google Chrome. Plany te zostały odrzucone, a Dart skupił się na kompilacji do JavaScript wraz z wydaniem wersji 1.9 w 2015 roku.

Dart 2.0 został wydany w sierpniu 2018 roku, w którym wprowadzono rozszerzenie dart2native, które kompilowało kod Dart na natywne platformy Linux, Windows, macOS. To rozszerzenie umożliwiło samodzielne tworzenie plików wykonywalnych, dzięki czemu Dart SDK nie był wymagany do uruchamiania aplikacji Dart na tych platformach. To rozszerzenie jest również zintegrowane z Flutterem, umożliwiając tworzenie aplikacji międzyplatformowych.

ECMA ustandaryzowała Darta pierwszą edycją w lipcu 2014 r., A drugą edycją w grudniu 2014 r.


## Jak uruchomić/wykonać kod Dart ##

Dart code może działać w następujący sposób:

- **Skompilowany jako JavaScript**:</br> Kod Dart jest kompilowany do JavaScript przy użyciu kompilatora dart2js. Skompilowany kod JavaScript jest kompatybilny ze wszystkimi głównymi przeglądarkami internetowymi.
- **Samodzielny**:</br> Dart Software Development Kit (SDK) jest dostarczany z samodzielną maszyną wirtualną Dart, która umożliwia uruchamianie kodu Dart w interfejsie wiersza poleceń. Dart jest dostarczany z kompletną standardową biblioteką, która pozwala użytkownikom pisać w pełni funkcjonalne aplikacje.
- **Skompilowane z wyprzedzeniem (AOT)**:</br> Kod Dart może zostać skompilowany przez AOT do kodu maszynowego, który umożliwia tworzenie aplikacji mobilnych za pomocą Flutter.
- **Rodzinny**:</br> Dzięki kompilatorowi dart2native kod Dart można skompilować do samodzielnych plików wykonywalnych, które mogą działać w systemach Windows, Linux i macOS.

## Format pliku rzutki ##

Dart to zorientowany obiektowo język w stylu C, który obsługuje interfejsy, domieszki, klasy abstrakcyjne, zreifikowane generyczne i interfejsy typu.

### Składnia ###

Poniżej przedstawiono kilka przykładów składni Darta.

#### Drukuj do konsoli ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Pętle i tablice ####

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

#### Funkcje ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Zajęcia ####

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

#### Mieszanki ####

Domieszki to zwykłe klasy, z których możemy pożyczać metody/zmienne bez ich dziedziczenia. Odbywa się to za pomocą słowa kluczowego *"with"*.

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

## Bibliografia ##

- [Dart (język programowania) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

