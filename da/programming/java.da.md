---
date: 2019-10-11
keywords: java, .java, java file format, how to open java files, how to run java files, java file, java sample code
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java filformularat
linktitle: Java
description: Ltjene om Java-filformat og API'er, der kan oprette og åbne Java-fils.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Hvad er en Java-fil? ##
En fil, der indeholder Java-kildekode og gemt med .java-filtypen, kaldes Java-fil. Java er en af de mest udbredte teknologier til udvikling af spil, mobil, web og desktop-applikationer. Da Java er platformsuafhængig, fungerer det fejlfrit på Windows, Mac, Linux, Raspberry Pi osv. Java ligner meget C# og C++, så det er nemmere at skifte mellem disse sprog.

## Kort historie ##

Java-projektet blev indledt i juni 1991 af James Gosling, Mike Sheridan og Patrick Naughton. Java blev oprindeligt navngivet Oak. Det blev senere omdøbt til Green og endelig til Java. James Gosling designede Java med en syntaks svarende til C/C++. Den første offentlige version af Java blev udgivet i 1996 af Sun Microsystems. Det kunne køre på alle de populære systemer, hvilket fik Java til at blive populært hurtigt. Med udgivelsen af Java 2 i december 1998 blev der bygget flere konfigurationer til forskellige typer platforme. Udgaverne var som følger

- J2EE (Java EE): Til virksomhedsløsninger
- J2ME (Java ME): Til mobilapplikationer
- J2SE (Java SE): Til desktop-applikationer

Den 19. november 2006 blev Java Virtual Machine (JVM) udgivet af Sun som gratis og open source-software. Efter at Oracle Corporation købte Sun Microsystems i 2009-2010, trak James Gosling sig fra Oracle den 2. april 2010.

## Sådan kører/udfører du Java-kode ##

For at udføre Java-koden skal den først kompileres. Til det kræves Java SDK. Java SDK kompilerer Java-koden til en bytekode-klassefil. Der er IDE'er som Eclipse og IntelliJ Idea, der gør det lettere at arbejde med Java-filer ved at levere kodefuldførelse og brugervenlig grænseflade til at kompilere og udføre Java-koden.

## Java filformat ##

Syntaksen i Java var stærkt påvirket af C og C++, men i modsætning til C++ blev Java næsten udelukkende bygget som et objektorienteret sprog. I Java er al koden skrevet inde i klasser, og hvert dataelement er et objekt. I modsætning til C++ understøtter Java ikke operatøroverbelastning eller multipel nedarvning.

### Java-eksempelkode ###

Det følgende er et eksempel på Java-syntaks.

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
I ovenstående kode angiver nøgleordet **offentlig** adgangsmodifikatoren. Den angiver, at denne klasse kan tilgås af klasserne uden for klassehierarkiet. Adgangsmodifikatoren kan også være **beskyttet** (kan tilgås i samme pakke) eller **privat** (metoderne kan kun tilgås af den samme klasse). Den **statiske** foran metoden indikerer, at metoden kan startes uden en specifik forekomst af klassen. **tomheden** indikerer, at metoden intet ville returnere. For at udskrive strengen til konsollen. Kommandoen System.out.println bruges. I denne kommando har *System*-klassen et statisk felt *out*, som er en forekomst af *PrintStream*-klassen, der indeholder *println*-metoden.

Filnavnet på Java-filerne skal være det samme som klassenavnet. Så Java-filen for eksempelkoden ville hedde *ExampleApp.java*.

## Referencer ##

- [Java (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

