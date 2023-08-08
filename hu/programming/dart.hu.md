---
date: 2019-10-11
keywords: dart, .dart, dart fájlformátum, dart fájl, dart fájlok futtatása, .dart kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dart fájlformátum
linktitle: Dart
description: "Ismerje meg a Dart fájlformátumot és az API-kat, amelyekkel Dart fájlokat hozhat létre és nyithat meg."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Mi az a Dart fájl? ##

A Dart fájl tartalmazza a Dart programozási nyelv forráskódját, amely egy kliensre optimalizált, a Google által kifejlesztett programozási nyelv, amelyet mobil, asztali, web, Iot (tárgyak internete) stb. alkalmazások készítésére használnak. A Dart egy objektumorientált nyelv. a C-hez hasonló szintaxissal. A Dart akár JavaScriptre, akár natív kódra fordítható. A Dart fájlokat ugyanúgy futtathatja a híres webböngészőben, mint a javascript fájlokat. A Dart SDK-val együtt szállított Dart virtuális gép néven ismert parancssori eszköz szintén használható a Dart fájlok fordítására és futtatására.

## Rövid története ##

A Dart projektet Lars Bak és Kasper Lund alapította, és az első verziót 2013. november 14-én adták ki. Kezdetben a Dart-ot kritizálták a web töredezettsége miatt, mivel a tervek szerint egy Dart virtuális gépet szeretnének beépíteni a Google Chrome-ba. Ezeket a terveket elvetették, és a Dart a JavaScriptre való fordításra összpontosított az 1.9-es verzió 2015-ös kiadásával.

A Dart 2.0 2018 augusztusában jelent meg, amelyben bemutatták a dart2native kiterjesztést, amely Dart kódot fordított natív Linux, Windows és macOS platformokra. Ez a bővítmény lehetővé tette az önálló végrehajtható fájlokat, amelyek miatt a Dart SDK-nak nem volt szüksége a Dart-alkalmazások futtatásához ezeken a platformokon. Ez a bővítmény a Flutter-rel is integrálva lehetővé teszi többplatformos alkalmazások létrehozását.

Az ECMA szabványosította a Dartot az első kiadással 2014 júliusában és a második kiadással 2014 decemberében.


## A ## Dart kód futtatása/végrehajtása

A dart kód a következő módokon futhat:

- **JavaScriptként összeállítva**:</br> A Dart kódot a dart2js fordító segítségével JavaScriptre fordítják. A lefordított JavaScript kód az összes főbb webböngészővel kompatibilis.
- **Önálló**:</br> A Dart Software Development Kit (SDK) egy önálló Dart virtuális géppel érkezik, amely lehetővé teszi a Dart kód futtatását a parancssori felületen. A Dart egy komplett szabványos könyvtárral rendelkezik, amely lehetővé teszi a felhasználók számára, hogy teljesen működőképes alkalmazásokat írjanak.
- **Idő előtti (AOT) összeállítás**:</br> A dart kód AOT-val lefordítható gépi kódra, amely lehetővé teszi a mobilalkalmazások Flutter segítségével történő építését.
- **Anyanyelvi**:</br> A dart2native fordítóval a Dart kód önálló futtatható fájlokká fordítható, amelyek Windows, Linux és macOS rendszeren futhatnak.

## Dart fájlformátum ##

A Dart egy C-stílusú objektum-orientált nyelv, amely támogatja az interfészeket, a mixineket, az absztrakt osztályokat, az újraértelmezett általánosságokat és a típusinterfészt.

### Szintaxis ###

Az alábbiakban néhány példa látható a Dart szintaxisra.

#### Nyomtatás a konzolra ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Hurok és tömbök ####

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

#### Funkciók ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Osztályok ####

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

A mixinek normál osztályok, amelyekből metódusokat/változókat kölcsönözhetünk anélkül, hogy örökölnénk őket. Ez a *"with"* kulcsszó használatával történik.

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

## Hivatkozások ##

- [Dart (programozási nyelv) - Wikipédia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

