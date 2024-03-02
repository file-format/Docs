---
date: 2019-10-11
keywords: dart, .dart, dart file format, dart file, how to run dart files, .dart extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: DArt Form Comhadat
linktitle: Dart
description: Ltuilleamh faoi fhormáid comhaid Dart agus APIs ar féidir leo comhad Dart a chruthú agus a oscailts.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## Cad is comhad Dart ann? ##

Tá cód foinse na teanga ríomhchlárúcháin Dart i gcomhad Dart ar teanga ríomhchlárúcháin optamaithe í a d'fhorbair Google a úsáidtear chun aipeanna a chruthú le haghaidh soghluaiste, deisce, gréasán, Iot (Idirlíon rudaí) srl. le comhréir cosúil le C. Is féidir Dart a chur le chéile de réir JavaScript nó cód dúchais. Is féidir leat na comhaid Dart a rith sa bhrabhsálaí gréasáin cáiliúil díreach mar is féidir leat comhad javascript a rith. Úsáidtear uirlis líne ordaithe ar a dtugtar meaisín fíorúil Dart a thagann le Dart SDK can freisin chun na comhaid Dart a thiomsú agus a rith.

## Stair Ghearr ##

The Dart project was founded by Lars Bak and Kasper Lund and the first version was released on 14th November 2013. I dtús, cáineadh an Dart as ilroinnt an ghréasáin mar gheall ar na pleananna chun Dart VM a áireamh in Google Chrome. Cuireadh deireadh leis na pleananna sin agus dhírigh Dart ar JavaScript a thiomsú le scaoileadh leagan 1.9 in 2015.

Scaoileadh Dart 2.0 i mí Lúnasa 2018 inar tugadh isteach an síneadh dart2native a thiomsaigh cód Dart chuig ardáin dhúchasacha Linux, Windows, macOS. Chuir an síneadh seo ar chumas earraí inrite féinchuimsitheacha de bharr nach raibh an Dart SDK ag teastáil chun apps Dart a rith ó na hardáin sin. Comhtháthaíodh an síneadh seo le Flutter freisin, rud a fhágann gur féidir aipeanna tras-ardáin a chruthú.

Rinne ECMA caighdeánaithe ar Dart leis an gcéad eagrán i mí Iúil 2014 agus an dara heagrán i mí na Nollag 2014.


## Conas cód Dart a rith / a fhorghníomhú ##

Is féidir cód dart a rith ar na bealaí seo a leanas:

- **Tiomsaithe mar JavaScript**:</br> Tiomsaítear an cód Dart go JavaScript trí úsáid a bhaint as tiomsaitheoir dart2js. Tá an cód JavaScript tiomsaithe ag luí leis na mórbhrabhsálaithe gréasáin go léir.
- **Seasamh**:</br> Seoltar an Kit Forbartha Bogearraí Dart (SDK) le Dart VM neamhspleách a ligeann do chód Dart rith sa chomhéadan ordú-líne. Longa Dart le leabharlann chaighdeánach iomlán a ligeann d’úsáideoirí apps lánfheidhmiúla a scríobh.
- **Roimh-am (AOT) tiomsaithe**:</br> Is féidir cód dart a thiomsú AOT do chód meaisín a cheadaíonn apps soghluaiste a thógáil le Flutter.
- **Dúchasach**:</br> Leis an tiomsaitheoir dart2native, is féidir cód Dart a thiomsú d'earraí inrite féinchuimsitheach is féidir a reáchtáil ar Windows, Linux, agus macOS.

## Formáid Chomhaid Dart ##

Is teanga C-stíl oibiachtaí-dhírithe é Dart a thacaíonn le comhéadain, meascáin, aicmí teibí, generics athneartaithe, agus cineál comhéadan.

### Comhréir ###

Seo a leanas roinnt samplaí de chomhréir Dart.

#### Priontáil chuig Consól ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### Lúb agus Eagar ####

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

#### Feidhmeanna ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### Ranganna ####

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

#### Meascáin ####

Is gnáth-aicmí iad meascáin ónar féidir linn modhanna/athróga a fháil ar iasacht gan iad a fháil le hoidhreacht. Déantar é seo tríd an eochairfhocal *le* a úsáid.

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

## Tagairtí ##

- [Dart (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [Dart](https://dart.dev/)

