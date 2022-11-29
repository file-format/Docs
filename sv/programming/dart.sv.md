---
date: 2019-10-11
keywords: dart, .dart, dart-filformat, dart-fil, hur man kör dart-filer, .dart-tillägget
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dart filformat
linktitle: Dart
description: "Lär dig om Dart-filformat och API:er som kan skapa och öppna Dart-filer." 
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Vad är en Dart-fil? ##

En Dart-fil innehåller källkoden till Dart-programmeringsspråket som är ett klientoptimerat programmeringsspråk utvecklat av Google som används för att bygga appar för mobil, desktop, webb, Iot (Internet of things) etc. Dart är ett objektorienterat språk med en syntax som liknar C. Dart kan kompileras till antingen JavaScript eller inbyggd kod. Du kan köra Dart-filerna i en berömd webbläsare precis som du kan köra en javascript-fil. Ett kommandoradsverktyg känt som Dart virtuell maskin som kommer med Dart SDK can används också för att kompilera och köra Dart-filerna.

## Kortfattad bakgrund ##

Dart-projektet grundades av Lars Bak och Kasper Lund och den första versionen släpptes den 14 november 2013. I början kritiserades Dart för webbfragmenteringen på grund av planerna på att inkludera en Dart VM i Google Chrome. De planerna lades ner och Dart fokuserade på att kompilera till JavaScript när version 1.9 släpptes 2015.

Dart 2.0 släpptes i augusti 2018 där dart2native-tillägget introducerades som kompilerade Dart-kod till inbyggda Linux-, Windows- och macOS-plattformar. Det här tillägget aktiverade fristående körbara filer på grund av att Dart SDK inte krävdes för att köra Dart-appar på dessa plattformar. Denna tillägg är också integrerad med Flutter vilket gör det möjligt att skapa plattformsoberoende appar.

ECMA standardiserade Dart med den första upplagan i juli 2014 och den andra upplagan i december 2014.


## Hur man kör/kör Dart-kod ##

Dartkod kan köras på följande sätt:

- **Kompilerad som JavaScript**:</br> Dart-koden kompileras till JavaScript med hjälp av kompilatorn dart2js. Den kompilerade JavaScript-koden är kompatibel med alla större webbläsare.
- **Fristående**:</br> Dart Software Development Kit (SDK) levereras med en fristående Dart VM som gör att Dart-kod kan köras i kommandoradsgränssnittet. Dart levereras med ett komplett standardbibliotek som tillåter användare att skriva fullt fungerande appar.
- **Ahead-of-time (AOT) sammanställd**:</br> Dartkod kan AOT-kompileras till maskinkod som gör att mobilappar kan byggas med Flutter.
- **Native**:</br> Med dart2native-kompilatorn kan Dart-kod kompileras till fristående körbara filer som kan köras på Windows, Linux och macOS.

## Dart-filformat ##

Dart är ett objektorienterat språk i C-stil som stöder gränssnitt, mixins, abstrakta klasser, reified generics och typgränssnitt.

### Syntax ###

Följande är några exempel på Dart-syntax.

#### Skriv ut till konsol ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Slingor och matriser ####

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

Mixiner är normala klasser som vi kan låna metoder/variabler från utan att ärva dem. Detta görs genom att använda nyckelordet *"with"*.

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

## Referenser ##

- [Dart (programmeringsspråk) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

