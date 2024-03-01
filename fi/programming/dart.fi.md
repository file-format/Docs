---
date: 2019-10-11
keywords: dart, .dart, dart file format, dart file, how to run dart files, .dart extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Dart tiedostolomakeat
linktitle: Dart
description: Lansaita Dart-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata Dart-tiedostons.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Mikä on Dart-tiedosto? ##

Dart-tiedosto sisältää Dart-ohjelmointikielen lähdekoodin, joka on Googlen kehittämä asiakasoptimoitu ohjelmointikieli, jota käytetään sovellusten luomiseen mobiili-, työpöytä-, verkko-, Iot- (esineiden internet) jne. käyttöön. Dart on oliokieli. jolla on samanlainen syntaksi kuin C. Dart voidaan kääntää joko JavaScriptiksi tai alkuperäiseen koodiin. Voit ajaa Dart-tiedostoja kuuluisalla verkkoselaimella aivan kuten javascript-tiedoston. Dart-tiedostojen kääntämiseen ja suorittamiseen käytetään myös komentorivityökalua, joka tunnetaan nimellä Dart-virtuaalikone, joka tulee Dart SDK:n mukana.

## Lyhyt historia ##

The Dart project was founded by Lars Bak and Kasper Lund and the first version was released on 14th November 2013. Aluksi Dartia kritisoitiin verkon pirstoutumisesta johtuen suunnitelmista sisällyttää Dart VM Google Chromeen. Nämä suunnitelmat hylättiin, ja Dart keskittyi kääntämiseen JavaScriptiin julkaisemalla version 1.9 vuonna 2015.

Dart 2.0 julkaistiin elokuussa 2018, jossa esiteltiin dart2native-laajennus, joka käänsi Dart-koodin alkuperäisille Linux-, Windows- ja macOS-alustoille. Tämä laajennus mahdollisti itsenäiset suoritettavat tiedostot, minkä vuoksi Dart SDK:ta ei vaadittu ajamaan Dart-sovelluksia näillä alustoilla. Tämä laajennus on myös integroitu Flutteriin, mikä mahdollistaa useiden alustojen välisten sovellusten luomisen.

ECMA standardoi Dartin ensimmäisellä painoksella heinäkuussa 2014 ja toisella painoksella joulukuussa 2014.


## Kuinka ajaa/suorittaa Dart-koodin ##

Dart-koodi voi ajaa seuraavilla tavoilla:

- **Koottu JavaScriptiksi**:</br> Dart-koodi käännetään JavaScriptiksi dart2js-kääntäjän avulla. Käytetty JavaScript-koodi on yhteensopiva kaikkien tärkeimpien verkkoselaimien kanssa.
-**Erillinen**:</br> Dart Software Development Kit (SDK) toimitetaan erillisen Dart VM:n kanssa, joka mahdollistaa Dart-koodin suorittamisen komentoriviliittymässä. Dart toimitetaan täydellisen vakiokirjaston kanssa, jonka avulla käyttäjät voivat kirjoittaa täysin toimivia sovelluksia.
- **Ennakkoaika (AOT) koottu**:</br> Dart-koodi voidaan AOT-kääntää konekoodiksi, joka mahdollistaa mobiilisovellusten rakentamisen Flutterilla.
- **Alkuperäinen**:</br> Dart2native-kääntäjällä Dart-koodi voidaan kääntää itsenäisiksi suoritettaviksi tiedostoiksi, jotka voivat toimia Windowsissa, Linuxissa ja macOS:ssä.

## Dart-tiedostomuoto ##

Dart on C-tyylinen oliokieli, joka tukee käyttöliittymiä, mixinejä, abstrakteja luokkia, uudelleen muotoiltuja geneerejä ja tyyppirajapintaa.

### Syntaksi ###

Seuraavassa on esimerkkejä Dart-syntaksista.

#### Tulosta konsoliin ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Silmukat ja taulukot ####

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

#### Toiminnot ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Luokat ####

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

Mixiinit ovat normaaleja luokkia, joista voimme lainata menetelmiä/muuttujia perimättä niitä. Tämä tehdään käyttämällä avainsanaa *with*.

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

## Viitteet ##

- {{HYPERLINKKI}})
- {{HYPERLINKKI1}}

