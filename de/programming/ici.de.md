{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "Datei", "Erweiterung", "Dateiformat", "ICI-Implementierung", "Programmierleitfaden", "ici-Beispiel", "ICI-Programmiersprache", "Module von ICI", "Datenmodell von ICI ", "Dokumentation von ICI", "ICI-Sprache" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Programmiersprachendatei",
  "description":"Erfahren Sie mehr über das ICI-Dateiformat und APIs, die ICI-Dateien erstellen und öffnen können.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Was ist eine ICI-Datei?

Eine Allzweck-Programmiersprache, die interpretiert wird und mehrere Funktionen wie dynamische Typisierung zusammen mit den flexiblen Datentypen enthält, ist als ICI-Programmiersprache (kein Akronym) bekannt. Es wird als der Sprache [Perl](/de/programming/pl/) ähnlich angesehen. Diese ICI-Sprache umfasst Flusssteuerungskonstrukte und enthält auch einige Operatoren der C-Sprache. Es ist keine objektorientierte Sprache, aber einige der Merkmale von OOP können durch eine spezielle Vererbungsmethode erreicht werden, die als Überstrukturen bekannt ist. Ähnlich wie [C](/de/programming/c) hat diese ICI-Programmiersprache die gleiche Systemschnittstelle und eine Standardbibliothek für eingebaute Funktionen.


## Kurze Geschichte ##

In den späten 1980er Jahren wurde es von Tim Long als universelle interpretierte Programmiersprache entwickelt. Die meisten Merkmale dieser Sprache ähneln denen von C, und einige der Merkmale können auch durch Anwendung einiger spezieller Methoden erreicht werden. Diese Sprache ist gemeinfrei und steht als wiederverkaufbare Sprache zur Verfügung, und niemand ist verpflichtet zu erwähnen, woher er den Quellcode hat. Die Dokumentation von ICI unterliegt dem Copyright von Canon Information System Research Australia.

## Technische Spezifikation ##

In dieser Sprache werden zwei verschiedene Datentypen verwendet. Diese beiden sind primitive und aggregierte Datentypen. Beide enthalten unterschiedliche Ausdrücke gemäß ihrer vordefinierten Zusammensetzung in der Sprache. Verschiedene Module wie verschachtelte und Subroutinen werden von dieser Sprache unterstützt. Da einige seiner Eigenschaften denen von Perl ähneln, hat es eine strikte Integration mit den regulären Ausdrücken.

Mengen sind darauf beschränkt, heterogen und verschachtelt zu sein. Diese Sets bieten Unterstützung für häufig verwendete Set-Operationen wie Union und Intersection usw. Es wird hauptsächlich als Sprache für die Kernimplementierung von Anwendungen verwendet, die multinationalen Organisationen gehören.

Nahezu alle Arten von Programmen können in dieser Sprache geschrieben werden, und die meisten spezifischen Programme, die komplexe Datenstrukturen beinhalten, werden in der ICI-Programmiersprache geschrieben. Anwendungen können die ICI-Implementierung so einbeziehen, dass sie darin geschrieben werden sollten. Funktionale Teile der Anwendung können durch die Module von ICI implementiert werden. Die Sprache von ICI ähnelt ein wenig der C-Sprache, aber das Datenmodell von ICI ist ein ziemlich höheres Niveau und unterscheidet sich mit Typen wie Wörterbüchern (Struct), Sätzen, dynamischen Arrays, regulären Ausdrücken und (echten) Zeichenfolgen.


## Beispiel für ICI-Dateiformat ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Bezug ##

* [ICI-Programmiersprache](http://atrn.org/ici/doc/ici.html)



