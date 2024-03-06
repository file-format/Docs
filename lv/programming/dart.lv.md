---
date: 2019-10-11
keywords: dart, .dart, dart file format, dart file, how to run dart files, .dart extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dmākslas faila formaat
linktitle: Dart
description: Lnopelniet par Dart faila formātu un API, kas var izveidot un atvērt Dart failus.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Kas ir Dart fails? ##

Dart failā ir iekļauts Dart programmēšanas valodas pirmkods, kas ir klientam optimizēta programmēšanas valoda, ko izstrādājis Google un ko izmanto, lai izveidotu lietotnes mobilajām ierīcēm, galddatoriem, tīmeklim, Iot (lietu internetam) utt. Dart ir objektorientēta valoda. ar sintaksi, kas līdzīga C. Dart var kompilēt vai nu JavaScript, vai vietējā kodā. Jūs varat palaist Dart failus slavenajā tīmekļa pārlūkprogrammā tāpat kā javascript failu. Dart failu apkopošanai un palaišanai tiek izmantots arī komandrindas rīks, kas pazīstams kā Dart virtuālā mašīna, kas tiek piegādāts kopā ar Dart SDK.

## Īsa vēsture ##

The Dart project was founded by Lars Bak and Kasper Lund and the first version was released on 14th November 2013. Sākumā Dart tika kritizēts par tīmekļa sadrumstalotību saistībā ar plāniem iekļaut Dart VM pārlūkprogrammā Google Chrome. Šie plāni tika atcelti, un Dart koncentrējās uz JavaScript kompilēšanu, izlaižot versiju 1.9 2015. gadā.

Dart 2.0 tika izlaists 2018. gada augustā, kurā tika ieviests paplašinājums dart2native, kas apkopoja Dart kodu vietējām Linux, Windows un macOS platformām. Šis paplašinājums iespējoja autonomus izpildāmos failus, kuru dēļ Dart SDK nebija nepieciešams, lai šajās platformās palaistu Dart lietotnes. Šis paplašinājums ir integrēts arī ar Flutter, kas ļauj izveidot vairāku platformu lietotnes.

ECMA standartizēja Dart ar pirmo izdevumu 2014. gada jūlijā un otro izdevumu 2014. gada decembrī.


## Kā palaist/izpildīt Dart kodu ##

Dart kodu var palaist šādos veidos:

- **Sastādīts kā JavaScript**:</br> Dart kods tiek kompilēts JavaScript, izmantojot dart2js kompilatoru. Apkopotais JavaScript kods ir saderīgs ar visām lielākajām tīmekļa pārlūkprogrammām.
- **Atsevišķi**:</br> Dart programmatūras izstrādes komplekts (SDK) tiek piegādāts ar atsevišķu Dart VM, kas ļauj Dart kodam darboties komandrindas saskarnē. Dart tiek piegādāts ar pilnīgu standarta bibliotēku, kas lietotājiem ļauj rakstīt pilnībā funkcionējošas lietotnes.
- **Apkopots pirms laika (AOT)**:</br> Šautriņu kodu var AOT kompilēt mašīnas kodā, kas ļauj veidot mobilās lietotnes, izmantojot Flutter.
- **Dzimtā**:</br> Izmantojot dart2native kompilatoru, Dart kodu var kompilēt pašpietiekamiem izpildāmiem failiem, kas var darboties operētājsistēmās Windows, Linux un macOS.

## Dart faila formāts ##

Dart ir C stila objektorientēta valoda, kas atbalsta interfeisus, mixins, abstraktās klases, reified sugas un tipa interfeisu.

### Sintakse ###

Tālāk ir sniegti daži Dart sintakses piemēri.

#### Drukāt uz konsoli ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Cilpas un masīvi ####

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

#### Funkcijas ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Klases ####

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

Mixins ir normālas klases, no kurām mēs varam aizņemties metodes/mainīgos, tos nepārmantojot. Tas tiek darīts, izmantojot atslēgvārdu *ar*.

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

## Atsauces Nr.

- [Dart (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

