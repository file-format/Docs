---
date: 2019-10-11
keywords: kt, .kt, kotlin fájlformátum, kotlin fájlok megnyitása, kotlin fájlok futtatása, .kt fájlformátum, kt fájl , kotlin fájlkiterjesztés, .kt kiterjesztés, kotlin vs java
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT fájlformátum
linktitle: KT
description: "Ismerje meg a KT fájlformátumot és az API-kat, amelyekkel KT fájlokat hozhat létre és nyithat meg."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Mi az a KT fájl? ##

A Kotlin nyelven írt forráskód .kt kiterjesztéssel kerül mentésre, amely általában **Kotlin fájlkiterjesztés** néven ismert. A Kotlin egy általános célú, többplatformos programozási nyelv, amelyet a JetBrains fejlesztett ki, hogy teljes mértékben együttműködjön a [Java]-val (/hu/programming/java/). A Kotlin védjegyet a Kotlin Alapítvány védi.

A Google 2019. május 7-én jelentette be a Kotlint az Android-alkalmazások fejlesztésének preferált programozási nyelveként. Az Android Studio 3.0 2017 októberében kezdte meg a Kotlin támogatását az Android-alkalmazások fejlesztésének alternatívájaként.

## A Kotlin KT fájlformátum rövid története ##

A Kotlint a JetBrains 2011 júliusában mutatta be a JVM új programozási nyelveként. A JetBrains vezetője, Dmitrij Jemerov elmondta, hogy a legtöbb nyelvből hiányoztak azok a funkciók, amelyeket kerestek, kivéve a Scalát, de a Scala lassú összeállítása hátrányt jelent. A Kotlin egyik fő célja az volt, hogy olyan gyorsan fordítson, mint a Java. A Kotlin projekt nyílt forráskódú Apache 2 licenc alatt 2012 februárjában.

A Kotlin 1.0-s verziója 2015. február 15-én jelent meg. Az Android a Google I/O 2017 rendezvényen bejelentette a Kotlin első osztályú támogatását Androidon. A Kotlin 1.2-t 2017. november 28-án adták ki, amely képes megosztani a kódot JVM és JavaScript platformok között. A Kotlin 1.3 2018. október 29-én jelent meg az aszinkron programozás támogatásával. A Google 2019. május 7-én bejelentette, hogy a Kotlin lesz az előnyben részesített programozási nyelv az Android-alkalmazások fejlesztéséhez. A Kotlin 1.4 2020 augusztusában jelent meg, néhány apró változtatással a Swift/Objective-C-vel való együttműködés támogatása érdekében.

## Kotlin szintaxis ##

A Kotlint úgy tervezték, hogy jobb legyen, mint a Java, de továbbra is együttműködjön a Java kóddal, hogy lehetővé tegye a Javáról a Kotlinra való fokozatos migrációt.

* A pontosvessző nem kötelező a Kotlin nyelvben. Egy új sor elegendő az állítás végének jelzésére.
* A Kotlin kétféle változót támogat: csak olvasható, amelyet a *val* kulcsszó definiál, és változó, amelyet a *var* kulcsszó határoz meg.
* A kurzusok alapértelmezés szerint zártkörűek és véglegesek. Az osztályból való származtatáshoz az alaposztályt az *open* kulcsszóval kell deklarálni.
* A Kotlin támogatja a procedurális programozást is.
* A Kotlin program belépési pontja a "fő" függvény, hasonlóan a Java-hoz, C#-hoz stb.

### Szintaxis példa ###

A következő példa a Kotlin szintaxisra.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

A fenti kódban a **fun** kulcsszó határozza meg a main nevű függvényt. A függvényen belül egy csak olvasható „közönség” változó van deklarálva a **val** kulcsszóval. A **println** módszerrel a „Hello World from Kotlin” felirat kerül a konzolra. A változó közönség értéke a **$** jellel kerül a karakterláncba.

## Kotlin vs Java
A Kotlin egy hivatalos nyelv az Android-alkalmazások írásához, számos fejlett funkcióval, de sok szakértő Java-fejlesztő még mindig nem mutat érdeklődést a Kotlinra való váltás iránt. Azt hiszik, hogy mindent csak Java-val tudnak megtenni. Tehát a következő két technológia összehasonlítása, amely meggyőzheti a java fejlesztőket a váltásról:

| Paraméter | Java | Kotlin |
|--------------------|------------|----------------- -|
| Singletons objektumok | √ | √ |
| Helyettesítő karakter típusok | √ | Χ |
| Összeállítás | Bájtkódok | Virtuális gép |
| Lambda kifejezés | Χ | √ |
| Invariáns tömb | Χ | √ |
| Nem magánterületek | √ | Χ |
| Smart Casts | Χ | √ |
| Null Safety | Χ | √ |
| Statikus tagok | √ | Χ |

## Referenciák ##

- [Kotlin (programozási nyelv) - Wikipédia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

