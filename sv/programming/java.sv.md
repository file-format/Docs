---
date: 2019-10-11
keywords: java, .java, java filformat, hur man öppnar java-filer, hur man kör java-filer, java-fil, java exempelkod
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java filformat
linktitle: Java
description: "Lär dig mer om Java-filformat och API:er som kan skapa och öppna Java-filer." 
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Vad är en Java-fil? ##
En fil som innehåller Java-källkod och sparad med filtillägget .java kallas Java-fil. Java är en av de mest använda teknikerna för utveckling av spel, mobil, webb och stationära applikationer. Eftersom Java är plattformsoberoende fungerar det felfritt på Windows, Mac, Linux, Raspberry Pi, etc. Java är väldigt likt C# och C++ så det är lättare att växla mellan dessa språk.

## Kortfattad bakgrund ##

Java-projektet initierades i juni 1991 av James Gosling, Mike Sheridan och Patrick Naughton. Java fick ursprungligen namnet Ek. Det döptes senare om till Green och slutligen till Java. James Gosling designade Java med en syntax som liknar C/C++. Den första offentliga versionen av Java släpptes 1996 av Sun Microsystems. Det kunde köras på alla populära system vilket gjorde att Java snabbt blev populärt. Med lanseringen av Java 2 i december 1998 byggdes flera konfigurationer för olika typer av plattformar. Versionerna var följande

- J2EE (Java EE): För företagslösningar
- J2ME (Java ME): För mobilapplikationer
- J2SE (Java SE): För stationära applikationer

Den 19 november 2006 släpptes Java Virtual Machine (JVM) av Sun som gratis programvara med öppen källkod. Efter att Oracle Corporation förvärvade Sun Microsystems 2009–2010 sa James Gosling upp sig från Oracle den 2 april 2010.

## Hur man kör/kör Java-kod ##

För att köra Java-koden måste den kompileras först. För det krävs Java SDK. Java SDK kompilerar Java-koden till en bytecode-klassfil. Det finns IDE:s som Eclipse och IntelliJ Idea som gör det lättare att arbeta med Java-filer genom att tillhandahålla kodkomplettering och lättanvänt gränssnitt för att kompilera och exekvera Java-koden.

## Java-filformat ##

Syntaxen för Java var starkt influerad av C och C++ men till skillnad från C++ byggdes Java nästan uteslutande som ett objektorienterat språk. I Java skrivs all kod i klasser och varje dataobjekt är ett objekt. Till skillnad från C++ stöder Java inte operatörsöverbelastning eller multipelt arv.

### Java-exempelkod ###

Följande är ett exempel på Java-syntax.

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
I koden ovan anger nyckelordet **public** åtkomstmodifieraren. Den anger att denna klass kan nås av klasserna utanför klasshierarkin. Åtkomstmodifieraren kan också vara **skyddad** (kan nås i samma paket) eller **privat** (metoderna kan endast nås av samma klass). **statiska** framför metoden indikerar att metoden kan anropas utan en specifik instans av klassen. **void** indikerar att metoden inte skulle returnera något. För att skriva ut strängen till konsolen. Kommandot System.out.println används. I det här kommandot har klassen *System* ett statiskt fält *out* som är en instans av klassen *PrintStream* som innehåller metoden *println*.

Filnamnet på Java-filerna ska vara detsamma som klassnamnet. Så Java-filen för exempelkoden skulle heta *ExampleApp.java*.

## Referenser ##

- [Java (programmeringsspråk) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

