---
date: 2019-10-11
keywords: kt, .kt, kotlin file format, how to open kotlin files, how to run kotlin files, .kt file format, kt file , kotlin file extension, .kt extention, kotlin vs java
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT fil formularat
linktitle: KT
description: Ltjen om KT filformat og API'er, der kan oprette og åbne KT fils.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Hvad er en KT fil? ##

En kildekode skrevet i Kotlin gemmes med filtypenavnet .kt, som er almindeligt kendt som **Kotlin filtypenavn**. Kotlin er et generel programmeringssprog på tværs af platforme udviklet af JetBrains til at være fuldt interoperabelt med [Java](/programming/java/). Kotlin-varemærket er beskyttet af Kotlin Foundation.

Kotlin was announced as the preferred programming language for Android App development by Google on 7th May 2019. Android Studio 3.0 begyndte at understøtte Kotlin som et alternativ til Android App-udvikling i oktober 2017.

## Kort historie om Kotlin KT-filformat##

Kotlin blev afsløret af JetBrains i juli 2011 som et nyt programmeringssprog til JVM. Lederen af JetBrains Dmitry Jemerov sagde, at de fleste af sprogene manglede funktioner, som de ledte efter undtagen Scala, men den langsomme kompilering af Scala var en ulempe. Et af Kotlins hovedmål var at kompilere lige så hurtigt som Java. Kotlin-projektet blev åbnet under Apache 2-licens i februar 2012.

Version 1.0 of Kotlin was released on 15 February 2015. Android annoncerede førsteklasses support til Kotlin på Android ved Google I/O 2017. Kotlin 1.2 blev udgivet den 28. november 2017 med mulighed for at dele kode mellem JVM- og JavaScript-platforme. Kotlin 1.3 blev udgivet den 29. oktober 2018 med understøttelse af asynkron programmering. Google annoncerede Kotlin som det foretrukne programmeringssprog til Android App-udvikling den 7. maj 2019. Kotlin 1.4 blev frigivet i august 2020 med nogle små ændringer for at understøtte interoperabilitet med Swift/Objective-C.

## Kotlin-syntaks ##

Kotlin blev designet til at være bedre end Java, men stadig være interoperabel med Java-kode for at tillade gradvis migrering fra Java til Kotlin.

 * Semikoloner er valgfrie i Kotlin. En ny linje er nok til at angive slutningen af udsagnet.
 * Kotlin understøtter to typer variabler, skrivebeskyttet, defineret af *val* nøgleordet, og mutable, defineret af *var* nøgleordet.
 * Klasser er private og endelige som standard. For at udlede fra en klasse, skal basisklassen erklæres med nøgleordet *open*.
 * Kotlin understøtter også proceduremæssig programmering.
 * Indgangspunktet til Kotlin-programmet er hoved-funktionen svarende til Java, C# osv.

### Syntakseksempel ###

Det følgende er et eksempel på Kotlin-syntaks.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

I ovenstående kode definerer nøgleordet **sjov** funktionen med navnet main. Inde i funktionen er en skrivebeskyttet variabel 'audience' erklæret med nøgleordet **val**. Ved at bruge **println**-metoden udskrives Hello World from Kotlin på konsollen. Værdien af den variable målgruppe injiceres i strengen med tegnet **$**.

## Kotlin vs Java
Kotlin er et officielt sprog til at skrive Android-apps med, der tilbyder mange avancerede funktioner, men mange ekspert Java-udviklere viser stadig ikke deres interesse for at skifte til Kotlin. De tror, at de kun kan gøre alt med Java. Så følgende er sammenligningen mellem to teknologier, der kan overbevise java-udviklerne til at skifte:

| Parameter | Java | Kotlin |
|--------------------|--------|---------------- -|
| Singletons Objekter | √ | √ |
| Jokertegntyper | √ | Χ |
| Kompilering | Bytekoder | Virtuel maskine |
| Lambda-udtryk | Χ | √ |
| Invariant Array | Χ | √ |
| Ikke-private felter | √ | Χ |
| Smart Casts | Χ | √ |
| Nul sikkerhed | Χ | √ |
| Statiske medlemmer | √ | Χ |

## Referencer ##

- [Kotlin (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

