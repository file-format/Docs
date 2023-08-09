---
date: 2019-10-11
keywords: "kt, .kt, Kotlin-Dateiformat, Öffnen von Kotlin-Dateien, Ausführen von Kotlin-Dateien, .kt-Dateiformat, kt-Datei, Kotlin-Dateierweiterung, .kt-Erweiterung, Kotlin vs. Java"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "KT-Dateiformat"
linktitle: "KT"
description: "Erfahren Sie mehr über das KT-Dateiformat und APIs, die KT-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Was ist eine KT-Datei? ##

Ein in Kotlin geschriebener Quellcode wird mit der Erweiterung .kt gespeichert, die allgemein als **Kotlin-Dateierweiterung** bekannt ist. Kotlin ist eine plattformübergreifende Allzweck-Programmiersprache, die von JetBrains für die vollständige Interoperabilität mit [Java](/de/programming/java/) entwickelt wurde. Die Marke Kotlin ist durch die Kotlin Foundation geschützt.

Kotlin wurde am 7. Mai 2019 von Google als bevorzugte Programmiersprache für die Entwicklung von Android-Apps angekündigt. Android Studio 3.0 begann im Oktober 2017 mit der Unterstützung von Kotlin als Alternative für die Entwicklung von Android-Apps.

## Kurze Geschichte des Kotlin KT-Dateiformats##

Kotlin wurde von JetBrains im Juli 2011 als neue Programmiersprache für JVM vorgestellt. Der Leiter von JetBrains, Dmitry Jemerov, sagte, dass den meisten Sprachen die gesuchten Funktionen fehlten, mit Ausnahme von Scala, aber die langsame Kompilierung von Scala sei ein Nachteil. Eines der Hauptziele von Kotlin war es, so schnell wie Java zu kompilieren. Das Kotlin-Projekt wurde im Februar 2012 unter der Apache 2-Lizenz als Open Source veröffentlicht.

Version 1.0 von Kotlin wurde am 15. Februar 2015 veröffentlicht. Android kündigte auf der Google I/O 2017 erstklassige Unterstützung für Kotlin auf Android an. Kotlin 1.2 wurde am 28. November 2017 veröffentlicht und bietet die Möglichkeit, Code zwischen JVM- und JavaScript-Plattformen auszutauschen. Kotlin 1.3 wurde am 29. Oktober 2018 mit der Unterstützung für asynchrone Programmierung veröffentlicht. Google hat Kotlin am 7. Mai 2019 als bevorzugte Programmiersprache für die Entwicklung von Android-Apps angekündigt. Kotlin 1.4 wurde im August 2020 mit einigen geringfügigen Änderungen veröffentlicht, um die Interoperabilität mit Swift/Objective-C zu unterstützen.

## Kotlin-Syntax ##

Kotlin wurde entwickelt, um besser als Java zu sein, aber dennoch mit Java-Code interoperabel zu sein, um eine schrittweise Migration von Java zu Kotlin zu ermöglichen.

* Semikolons sind in Kotlin optional. Eine neue Zeile reicht aus, um das Ende der Anweisung anzuzeigen.
* Kotlin unterstützt zwei Arten von Variablen, schreibgeschützt, definiert durch das Schlüsselwort *val*, und änderbar, definiert durch das Schlüsselwort *var*.
* Klassen sind standardmäßig privat und endgültig. Um von einer Klasse abzuleiten, muss die Basisklasse mit dem Schlüsselwort *open* deklariert werden.
* Kotlin unterstützt auch prozedurale Programmierung.
* Der Einstiegspunkt zum Kotlin-Programm ist die „main“-Funktion ähnlich wie bei Java, C# usw.

### Syntaxbeispiel ###

Das Folgende ist ein Beispiel für die Kotlin-Syntax.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Im obigen Code definiert das Schlüsselwort **fun** die Funktion mit dem Namen main. Innerhalb der Funktion wird eine schreibgeschützte Variable „audience“ mit dem Schlüsselwort **val** deklariert. Durch die Verwendung der Methode **println** wird „Hello World from Kotlin“ auf der Konsole ausgegeben. Der Wert der Variablen Audience wird mit dem Zeichen **$** in die Zeichenfolge eingefügt.

## Kotlin gegen Java
Kotlin ist eine offizielle Sprache zum Schreiben von Android-Apps mit vielen erweiterten Funktionen, aber viele erfahrene Java-Entwickler zeigen immer noch kein Interesse, zu Kotlin zu wechseln. Sie denken, dass sie alles nur mit Java machen können. Im Folgenden also der Vergleich zwischen zwei Technologien, die die Java-Entwickler davon überzeugen könnten, umzusteigen:

| Parameter | Java | Kotlin |
|--------------------|-----------|----------- -|
| Singletons-Objekte | √ | √ |
| Wildcard-Typen | √ | Χ |
| Zusammenstellung | Bytecodes | Virtuelle Maschine |
| Lambda-Ausdruck | Χ | √ |
| Invariantes Array | Χ | √ |
| Nicht private Felder | √ | Χ |
| Intelligente Besetzungen | Χ | √ |
| Nullsicherheit | Χ | √ |
| Statische Elemente | √ | Χ |

## Verweise ##

- [Kotlin (Programmiersprache) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

