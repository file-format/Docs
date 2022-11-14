---
date: 2019-10-11
keywords: dart, .dart, formato file dart, file dart, come eseguire file dart, estensione .dart
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file Dart
linktitle: Dart
description: "Scopri il formato di file Dart e le API che possono creare e aprire file Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Che cos'è un file Dart? ##

Un file Dart contiene il codice sorgente del linguaggio di programmazione Dart che è un linguaggio di programmazione ottimizzato per il client sviluppato da Google che viene utilizzato per creare app per dispositivi mobili, desktop, Web, Iot (Internet delle cose) ecc. Dart è un linguaggio orientato agli oggetti con una sintassi simile a C. Dart può essere compilato in codice JavaScript o nativo. Puoi eseguire i file Dart nel famoso browser web proprio come puoi eseguire un file javascript. Per compilare ed eseguire i file Dart viene utilizzato anche uno strumento da riga di comando noto come Dart virtual machine fornito con Dart SDK can.

## Breve storia ##

Il progetto Dart è stato fondato da Lars Bak e Kasper Lund e la prima versione è stata rilasciata il 14 novembre 2013. All'inizio il Dart è stato criticato per la frammentazione del web a causa dei piani per l'inclusione di una VM Dart in Google Chrome. Questi piani sono stati abbandonati e Dart si è concentrato sulla compilazione in JavaScript con il rilascio della versione 1.9 nel 2015.

Dart 2.0 è stato rilasciato nell'agosto 2018 in cui è stata introdotta l'estensione dart2native che compilava il codice Dart su piattaforme native Linux, Windows e macOS. Questa estensione ha abilitato eseguibili autonomi grazie ai quali l'SDK Dart non era necessario per eseguire app Dart su quelle piattaforme. Questa estensione si integrava anche con Flutter rendendo possibile la creazione di app multipiattaforma.

ECMA ha standardizzato Dart con la prima edizione a luglio 2014 e la seconda edizione a dicembre 2014.


## Come eseguire/eseguire il codice Dart ##

Il codice Dart può essere eseguito nei seguenti modi:

- **Compilato come JavaScript**:</br> Il codice Dart viene compilato in JavaScript utilizzando il compilatore dart2js. Il codice JavaScript compilato è compatibile con tutti i principali browser web.
- **Indipendente, autonomo**:</br> Il Dart Software Development Kit (SDK) viene fornito con una VM Dart autonoma che consente l'esecuzione del codice Dart nell'interfaccia della riga di comando. Dart viene fornito con una libreria standard completa che consente agli utenti di scrivere app completamente funzionali.
- **Compilazione anticipata (AOT)**:</br> Il codice Dart può essere compilato in AOT in codice macchina che consente di creare app mobili con Flutter.
- **Nativo**:</br> Con il compilatore dart2native, il codice Dart può essere compilato in eseguibili autonomi che possono essere eseguiti su Windows, Linux e macOS.

## Formato file Dart ##

Dart è un linguaggio orientato agli oggetti in stile C che supporta interfacce, mixin, classi astratte, generici reificati e interfaccia di tipo.

### Sintassi ###

Di seguito sono riportati alcuni esempi di sintassi di Dart.

#### Stampa su console ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Loop e array ####

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

#### Funzioni ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Classi ####

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

#### Mixin ####

I mixin sono classi normali da cui possiamo prendere in prestito metodi/variabili senza ereditarli. Questo viene fatto utilizzando la parola chiave *"with"*.

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

## Riferimenti ##

- [Dart (linguaggio di programmazione) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(linguaggio_di_programmazione))
- [Dardo](https://dart.dev/)

