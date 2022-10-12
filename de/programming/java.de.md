---
date: 2019-10-11
keywords: "Java, .java, Java-Dateiformat, Java-Dateien öffnen, Java-Dateien ausführen, Java-Datei, Java-Beispielcode"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "Java-Dateiformat"
linktitle: "Java"
description: "Erfahren Sie mehr über das Java-Dateiformat und APIs, die Java-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Was ist eine Java-Datei? ##
Eine Datei, die Java-Quellcode enthält und mit der Dateierweiterung .java gespeichert wird, wird als Java-Datei bezeichnet. Java ist eine der am weitesten verbreiteten Technologien für die Entwicklung von Spielen, Mobil-, Web- und Desktop-Anwendungen. Da Java plattformunabhängig ist, funktioniert es einwandfrei unter Windows, Mac, Linux, Raspberry Pi usw. Java ist C# und C++ sehr ähnlich, sodass es einfacher ist, zwischen diesen Sprachen zu wechseln.

## Kurze Geschichte ##

Das Java-Projekt wurde im Juni 1991 von James Gosling, Mike Sheridan und Patrick Naughton initiiert. Java hieß ursprünglich Oak. Später wurde es in Green und schließlich in Java umbenannt. James Gosling hat Java mit einer C/C++ ähnlichen Syntax entworfen. Die erste öffentliche Version von Java wurde 1996 von Sun Microsystems veröffentlicht. Es konnte auf allen gängigen Systemen ausgeführt werden, was dazu führte, dass Java schnell populär wurde. Mit der Veröffentlichung von Java 2 im Dezember 1998 wurden mehrere Konfigurationen für verschiedene Plattformtypen erstellt. Die Versionen waren wie folgt

- J2EE (Java EE): Für Unternehmenslösungen
- J2ME (Java ME): Für mobile Anwendungen
- J2SE (Java SE): Für Desktop-Anwendungen

Am 19. November 2006 wurde Java Virtual Machine (JVM) von Sun als kostenlose Open-Source-Software veröffentlicht. Nach der Übernahme von Sun Microsystems durch die Oracle Corporation in den Jahren 2009–2010 trat James Gosling am 2. April 2010 von Oracle zurück.

## Wie man Java-Code ausführt/ausführt ##

Um den Java-Code auszuführen, muss dieser zunächst kompiliert werden. Dafür wird das Java SDK benötigt. Das Java SDK kompiliert den Java-Code in eine Bytecode-Klassendatei. Es gibt IDEs wie Eclipse und IntelliJ Idea, die die Arbeit mit Java-Dateien erleichtern, indem sie Codevervollständigung und eine benutzerfreundliche Schnittstelle zum Kompilieren und Ausführen des Java-Codes bereitstellen.

## Java-Dateiformat ##

Die Syntax von Java wurde stark von C und C++ beeinflusst, aber im Gegensatz zu C++ wurde Java fast ausschließlich als objektorientierte Sprache entwickelt. In Java wird der gesamte Code in Klassen geschrieben und jedes Datenelement ist ein Objekt. Im Gegensatz zu C++ unterstützt Java keine Operatorüberladung oder Mehrfachvererbung.

### Java-Beispielcode ###

Das Folgende ist ein Beispiel für die Java-Syntax.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
Im obigen Code bezeichnet das Schlüsselwort **public** den Zugriffsmodifikator. Es besagt, dass auf diese Klasse von den Klassen außerhalb der Klassenhierarchie zugegriffen werden kann. Der Zugriffsmodifikator kann auch **protected** (Zugriff im selben Paket möglich) oder **private** (auf die Methoden kann nur von derselben Klasse zugegriffen werden) sein. Das **statische** vor der Methode gibt an, dass die Methode ohne eine bestimmte Instanz der Klasse aufgerufen werden kann. **void** gibt an, dass die Methode nichts zurückgeben würde. Um die Zeichenfolge auf der Konsole auszugeben. Der Befehl System.out.println wird verwendet. In diesem Befehl hat die *System*-Klasse ein statisches Feld *out*, das eine Instanz der *PrintStream*-Klasse ist, die die *println*-Methode enthält.

Der Dateiname der Java-Dateien sollte mit dem Klassennamen übereinstimmen. Die Java-Datei für den Beispielcode würde also *ExampleApp.java* heißen.

## Verweise ##

- [Java (Programmiersprache) - Wikipedia](https://en.wikipedia.org/wiki/Java_(Programmiersprache))

