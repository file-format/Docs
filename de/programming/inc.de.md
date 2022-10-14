{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INC-Dateierweiterung - Was ist eine INC-Datei?",
  "description":"Erfahren Sie mehr über das INC Include-Dateiformat und APIs, die INC-Dateien erstellen und öffnen können.",
  "linktitle" :"INK",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Was ist eine INC-Datei?

Eine INC-Datei ist eine Include-Datei, die vom Quellcode eines Softwareprogramms verwendet wird, um Header-Informationen zu referenzieren. Es ähnelt dem [.h-Dateiformat](/de/programming/h/) und enthält Deklarationen, Funktionen, Header oder Makros, die von Quellcodedateien wie C++ wiederverwendet werden können. INC-Dateien werden von einer Vielzahl von Programmiersprachen wie C, [C++](/de/programming/cpp/), Pascal, [PHP](/de/programming/php/) und [Java](/de/programming/java/) verwendet. Texteditoren wie Microsoft Notepad, Notepad++ und TextEdit können zum Öffnen von INC-Dateien verwendet werden.

## INC-Dateiformat - Weitere Informationen

Eine INC-Datei wird als reine Textdatei mit allen enthaltenen Deklarationen gemäß der Deklarationssyntax gespeichert. Eine INC-Datei kann auch auf andere INC-Dateien verweisen. Nach der Erstellung wird die INC-Datei Teil des Projekts und kann von Quelldateien wie C++ referenziert werden. Es kann von mehreren Quelldateien referenziert werden, um Duplikate zu vermeiden.

## Inhalt der INC-Datei

INC-Dateien können die folgenden Informationen enthalten.

**`Variablen`** - Im Fall von objektorientierter Programmierung (OOP) enthält eine Klassenheaderdatei Definitionen aller Variablen auf Klassenebene, auf die über die Quellcodedateien der Implementierung zugegriffen werden kann

**`Methods Declaration`** – Alle Methodendeklarationen sind in den .h-Header-Dateien enthalten, um über mehrere Implementierungsdateien hinweg zugänglich zu sein.

**`Nicht-Inline-Funktionsdefinitionen`** - Header-Dateien können auch Definitionen von Nicht-Inline-Methoden enthalten.

## Nachteil der Verwendung von INC-Dateien in PHP

PHP sind serverseitige Skripte, die auf dem Server ausgeführt werden und die Ergebnisse an die aufrufenden Webseiten zurückgeben. Wenn eine PHP-Datei auf eine INC-Datei verweist und der Server nicht zum Parsen von .inc-Dateien konfiguriert ist (was sehr häufig vorkommt), kann ein Benutzer den PHP-Quellcode in der .inc-Datei anzeigen, indem er das URL-Verzeichnis besucht. Man muss also vorsichtig sein, wenn man INC-Dateien als Include-Dateien in PHP verwendet.

## Verweise

* [Verwendung von INC in PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

