---
date: 2019-10-11
keywords: dart, .dart, dart file format, dart file, how to run dart files, .dart extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dmeno failo formaat
linktitle: Dart
description: Luždirbti apie Dart failo formatą ir API, kurios gali sukurti ir atidaryti Dart failąs.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Kas yra Dart failas? ##

Dart faile yra Dart programavimo kalbos, kuri yra Google sukurta klientui optimizuota programavimo kalba, kuri naudojama programoms mobiliesiems, staliniams kompiuteriams, žiniatinkliui, Iot (daiktų internetui) ir kt. kurti. Dart yra į objektą orientuota kalba. su sintaksė, panašia į C. Dart gali būti sukompiliuota į JavaScript arba vietinį kodą. Dart failus galite paleisti garsiojoje žiniatinklio naršyklėje, kaip ir Javascript failą. Komandinės eilutės įrankis, žinomas kaip Dart virtualioji mašina, kuris pateikiamas kartu su Dart SDK, taip pat naudojamas Dart failams kompiliuoti ir paleisti.

## Trumpa istorija ##

The Dart project was founded by Lars Bak and Kasper Lund and the first version was released on 14th November 2013. Iš pradžių Dart buvo kritikuojamas dėl žiniatinklio susiskaidymo dėl planų įtraukti Dart VM į Google Chrome. Šie planai buvo atmesti ir Dart sutelkė dėmesį į JavaScript kompiliavimą, kai 2015 m. buvo išleista 1.9 versija.

2018 m. rugpjūčio mėn. buvo išleista Dart 2.0, kurioje buvo pristatytas dart2native plėtinys, kuris sukompiliavo Dart kodą vietinėms Linux, Windows ir MacOS platformoms. Šis plėtinys įgalino savarankiškus vykdomuosius failus, todėl Dart SDK neprivalėjo paleisti Dart programėlių tose platformose. Šis plėtinys taip pat integruotas su Flutter, kad būtų galima kurti kelių platformų programas.

ECMA standartizavo Dart pirmąjį leidimą 2014 m. liepos mėn., o antrąjį – 2014 m. gruodžio mėn.


## Kaip paleisti / vykdyti Dart kodą ##

Dart kodas gali būti paleistas šiais būdais:

- **Sudaryta kaip JavaScript**:</br> Dart kodas sukompiliuojamas į JavaScript naudojant dart2js kompiliatorių. Sudarytas JavaScript kodas yra suderinamas su visomis pagrindinėmis interneto naršyklėmis.
- **Atskiras**:</br> Dart programinės įrangos kūrimo rinkinys (SDK) pristatomas su atskiru Dart VM, leidžiančiu Dart kodui paleisti komandinės eilutės sąsajoje. Dart pristatoma su visa standartine biblioteka, kuri leidžia vartotojams rašyti visiškai veikiančias programas.
- **Sudaryta prieš laiką (AOT)**:</br> Dart kodas gali būti AOT sukompiliuotas į mašininį kodą, kuris leidžia kurti programas mobiliesiems naudojant Flutter.
- **Gimtoji**:</br> Naudojant dart2native kompiliatorių, Dart kodas gali būti sukompiliuotas į savarankiškus vykdomuosius failus, kurie gali veikti Windows, Linux ir MacOS.

## Dart failo formatas ##

Dart yra C stiliaus į objektus orientuota kalba, palaikanti sąsajas, mišinius, abstrakčias klases, pakeistus bendruosius žodžius ir tipo sąsają.

### Sintaksė ###

Toliau pateikiami keli Dart sintaksės pavyzdžiai.

#### Spausdinti į konsolę ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Kilpos ir masyvai ####

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

#### Funkcijos ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Klasės ####

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

#### Mišiniai ####

Mixins yra normalios klasės, iš kurių galime pasiskolinti metodus/kintamuosius jų nepaveldėdami. Tai atliekama naudojant raktinį žodį *su*.

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

## Nuorodos Nr.

- [Dart (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

