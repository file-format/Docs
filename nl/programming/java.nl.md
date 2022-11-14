---
date: 2019-10-11
keywords: java, .java, java-bestandsindeling, hoe java-bestanden te openen, hoe java-bestanden uit te voeren, java-bestand, java-voorbeeldcode
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java-bestandsindeling
linktitle: Java
description: "Meer informatie over Java-bestandsindelingen en API's die Java-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Wat is een Java-bestand? ##
Een bestand dat de Java-broncode bevat en is opgeslagen met de .java-bestandsextensie staat bekend als Java-bestand. Java is een van de meest gebruikte technologie voor de ontwikkeling van games, mobiele, web- en desktopapplicaties. Omdat Java platformonafhankelijk is, werkt het feilloos op Windows, Mac, Linux, Raspberry Pi, enz. Java lijkt erg op C# en C++, dus het is gemakkelijker om tussen deze talen te schakelen.

## Korte geschiedenis ##

Het Java-project werd in juni 1991 geïnitieerd door James Gosling, Mike Sheridan en Patrick Naughton. Java heette aanvankelijk Oak. Het werd later omgedoopt tot Groen en uiteindelijk tot Java. James Gosling ontwierp Java met een syntaxis vergelijkbaar met C/C++. De eerste openbare versie van Java werd in 1996 uitgebracht door Sun Microsystems. Het zou op alle populaire systemen kunnen draaien waardoor Java snel populair werd. Met de release van Java 2 in december 1998 werden meerdere configuraties voor verschillende soorten platforms gebouwd. De versies waren als volgt:

- J2EE (Java EE): voor bedrijfsoplossingen
- J2ME (Java ME): voor mobiele toepassingen
- J2SE (Java SE): voor desktoptoepassingen

Op 19 november 2006 werd Java Virtual Machine (JVM) door Sun uitgebracht als gratis en open-source software. Nadat Oracle Corporation Sun Microsystems in 2009-2010 had overgenomen, nam James Gosling op 2 april 2010 ontslag bij Oracle.

## Java-code uitvoeren/uitvoeren ##

Om de Java-code uit te voeren, moet deze eerst worden gecompileerd. Daarvoor is de Java SDK vereist. De Java SDK compileert de Java-code naar een bytecode-klassebestand. Er zijn IDE's zoals Eclipse en IntelliJ Idea die het gemakkelijker maken om met Java-bestanden te werken door code-aanvulling te bieden en een gebruiksvriendelijke interface om de Java-code te compileren en uit te voeren.

## Java-bestandsindeling ##

De syntaxis van Java werd sterk beïnvloed door C en C++, maar in tegenstelling tot C++ werd Java bijna uitsluitend gebouwd als een objectgeoriënteerde taal. In Java wordt alle code in klassen geschreven en is elk gegevensitem een object. In tegenstelling tot C++ ondersteunt Java geen overbelasting van operators of meervoudige overerving.

### Java-voorbeeldcode ###

Het volgende is een voorbeeld van Java-syntaxis.

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
In de bovenstaande code geeft het trefwoord **public** de toegangsmodifier aan. Er staat dat deze klasse toegankelijk is voor de klassen buiten de klassenhiërarchie. De toegangsmodifier kan ook **beveiligd** zijn (kan in hetzelfde pakket worden geopend) of **privé** (de methoden zijn alleen toegankelijk voor dezelfde klasse). De **static** voor de methode geeft aan dat de methode kan worden aangeroepen zonder een specifieke instantie van de klasse. De **void** geeft aan dat de methode niets zou opleveren. Om de string naar de console af te drukken. De opdracht System.out.println wordt gebruikt. In deze opdracht heeft de klasse *System* een statisch veld *out* dat een instantie is van de klasse *PrintStream* die de methode *println* bevat.

De bestandsnaam van de Java-bestanden moet hetzelfde zijn als de klassenaam. Het Java-bestand voor de voorbeeldcode zou dus *ExampleApp.java* heten.

## Referenties ##

- [Java (programmeertaal) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programmeertaal))

