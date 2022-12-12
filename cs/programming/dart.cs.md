---
date: 2019-10-11
keywords: dart, .dart, formát souboru dart, soubor dart, jak spouštět soubory dart, přípona .dart
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru Dart
linktitle: Dart
description: "Přečtěte si o formátu souboru Dart a rozhraních API, která mohou vytvářet a otevírat soubory Dart."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Co je soubor Dart? ##

Soubor Dart obsahuje zdrojový kód programovacího jazyka Dart, což je klientsky optimalizovaný programovací jazyk vyvinutý společností Google, který se používá k vytváření aplikací pro mobily, počítače, web, Iot (internet věcí) atd. Dart je objektově orientovaný jazyk se syntaxí podobnou C. Dart lze zkompilovat buď do JavaScriptu, nebo do nativního kódu. Soubory Dart můžete spouštět ve známém webovém prohlížeči, stejně jako můžete spouštět soubor javascript. Ke kompilaci a spouštění souborů Dart se také používá nástroj příkazového řádku známý jako Dart virtual machine, který je dodáván s Dart SDK plechovkou.

## Stručná historie ##

Projekt Dart založili Lars Bak a Kasper Lund a první verze byla vydána 14. listopadu 2013. Na začátku byl Dart kritizován za fragmentaci webu kvůli plánům na zahrnutí Dart VM do Google Chrome. Tyto plány byly zrušeny a Dart se zaměřil na kompilaci do JavaScriptu s vydáním verze 1.9 v roce 2015.

Dart 2.0 byl vydán v srpnu 2018, ve kterém bylo představeno rozšíření dart2native, které zkompilovalo kód Dart pro nativní platformy Linux, Windows a macOS. Toto rozšíření umožňovalo samostatné spustitelné soubory, díky kterým nebylo nutné Dart SDK spouštět aplikace Dart na těchto platformách. Toto rozšíření je také integrováno s Flutter, což umožňuje vytvářet aplikace pro různé platformy.

ECMA standardizoval Dart s prvním vydáním v červenci 2014 a druhým vydáním v prosinci 2014.


## Jak spustit/spustit Dart kód ##

Šipkový kód může běžet následujícími způsoby:

- **Zkompilováno jako JavaScript**:</br> Kód Dart je zkompilován do JavaScriptu pomocí kompilátoru dart2js. Kompilovaný JavaScript kód je kompatibilní se všemi hlavními webovými prohlížeči.
- **Samostatný**:</br> Sada Dart Software Development Kit (SDK) se dodává se samostatným virtuálním počítačem Dart, který umožňuje spouštění kódu Dart v rozhraní příkazového řádku. Dart se dodává s kompletní standardní knihovnou, která uživatelům umožňuje psát plně funkční aplikace.
- **Předběžně zkompilováno (AOT)**:</br> Šipkový kód lze AOT zkompilovat do strojového kódu, který umožňuje vytvářet mobilní aplikace pomocí Flutter.
- **Nativní**:</br> Pomocí kompilátoru dart2native lze kód Dart zkompilovat do samostatných spustitelných souborů, které lze spustit na Windows, Linux a macOS.

## Formát souboru Dart ##

Dart je objektově orientovaný jazyk ve stylu C, který podporuje rozhraní, mixiny, abstraktní třídy, reifikovaná generika a typové rozhraní.

### Syntaxe ###

Následuje několik příkladů syntaxe Dart.

#### Tisk do konzole ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Smyčky a pole ####

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

#### Funkce ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Třídy ####

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

#### Mixy ####

Mixiny jsou normální třídy, ze kterých si můžeme vypůjčit metody/proměnné, aniž bychom je zdědili. To se provádí pomocí klíčového slova *"with"*.

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

## Reference ##

- [Dart (programovací jazyk) - Wikipedie](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

