---
date: 2019-10-11
keywords: kt, .kt, kotlin-filformat, hur man öppnar kotlin-filer, hur man kör kotlin-filer, .kt-filformat, kt-fil, kotlin-filtillägg, .kt extension, kotlin vs java
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT filformat
linktitle: KT
description: "Lär dig om KT-filformat och API:er som kan skapa och öppna KT-filer." 
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Vad är KT fil? ##

En källkod skriven i Kotlin sparas med tillägget .kt som är allmänt känt som **Kotlin filtillägg**. Kotlin är ett allmänt plattformsoberoende programmeringsspråk utvecklat av JetBrains för att vara fullt interoperabelt med [Java](/sv/programmering/java/). Kotlins varumärke är skyddat av Kotlin Foundation.

Kotlin tillkännagavs som det föredragna programmeringsspråket för Android-apputveckling av Google den 7 maj 2019. Android Studio 3.0 började stödja Kotlin som ett alternativ för Android-apputveckling i oktober 2017.

## Kort historik om Kotlin KT-filformat##

Kotlin presenterades av JetBrains i juli 2011 som ett nytt programmeringsspråk för JVM. Ledaren av JetBrains Dmitry Jemerov sa att de flesta av språken saknade funktioner som de letade efter förutom Scala men den långsamma sammanställningen av Scala var en nackdel. Ett av huvudmålen för Kotlin var att kompilera lika snabbt som Java. Kotlin-projektet var öppen källkod under Apache 2-licens i februari 2012.

Version 1.0 av Kotlin släpptes den 15 februari 2015. Android tillkännagav förstklassigt stöd för Kotlin på Android vid Google I/O 2017. Kotlin 1.2 släpptes den 28 november 2017 med möjligheten att dela kod mellan JVM- och JavaScript-plattformar. Kotlin 1.3 släpptes den 29 oktober 2018 med stöd för asynkron programmering. Google tillkännagav Kotlin som det föredragna programmeringsspråket för Android-apputveckling den 7 maj 2019. Kotlin 1.4 släpptes i augusti 2020 med några små ändringar för att stödja interoperabilitet med Swift/Objective-C.

## Kotlin-syntax ##

Kotlin designades för att vara bättre än Java men ändå vara interoperabel med Java-kod för att möjliggöra gradvis migrering från Java till Kotlin.

* Semikolon är valfria i Kotlin. En ny rad räcker för att indikera slutet på påståendet.
* Kotlin stöder två typer av variabler, skrivskyddade, definierade av nyckelordet *val*, och föränderliga, definierade av nyckelordet *var*.
* Klasserna är privata och slutliga som standard. För att härleda från en klass måste basklassen deklareras med nyckelordet *open*.
* Kotlin stöder även procedurprogrammering.
* Ingångspunkten till Kotlin-programmet är "huvudfunktionen" som liknar Java, C#, etc.

### Syntaxexempel ###

Följande är ett exempel på Kotlin-syntax.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

I koden ovan definierar nyckelordet **fun** funktionen som heter main. Inuti funktionen deklareras en skrivskyddad variabel 'publik' med nyckelordet **val**. Genom att använda **println**-metoden skrivs "Hello World from Kotlin" ut på konsolen. Värdet för den variabla målgruppen injiceras i strängen med tecknet **$**.

## Kotlin vs Java
Kotlin är ett officiellt språk för att skriva Android-appar med många avancerade funktioner, men många expertutvecklare av Java visar fortfarande inte sitt intresse för att byta till Kotlin. De tror att de bara kan göra allt med Java. Så följande är jämförelsen mellan två tekniker som kan övertyga java-utvecklarna att byta:

| Parameter | Java | Kotlin |
|--------------------|----------------|---------------- -|
| Singletons Objekt | √ | √ |
| Jokerteckentyper | √ | Χ |
| Sammanställning | Bytekoder | Virtuell maskin |
| Lambdauttryck | Χ | √ |
| Invariant Array | Χ | √ |
| Icke-privata fält | √ | Χ |
| Smarta kastar | Χ | √ |
| Noll säkerhet | Χ | √ |
| Statiska medlemmar | √ | Χ |

## Referenser ##

- [Kotlin (programmeringsspråk) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

