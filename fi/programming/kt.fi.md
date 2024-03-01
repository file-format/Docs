---
date: 2019-10-11
keywords: kt, .kt, kotlin file format, how to open kotlin files, how to run kotlin files, .kt file format, kt file , kotlin file extension, .kt extention, kotlin vs java
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT Tiedostolomakeat
linktitle: KT
description: Lansaitse KT-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata KT-tiedostons.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Mikä on KT-tiedosto? ##

Kotlinilla kirjoitettu lähdekoodi tallennetaan .kt-tunnisteella, joka tunnetaan yleisesti nimellä **Kotlin-tiedostotunniste**. Kotlin on yleiskäyttöinen monikäyttöinen ohjelmointikieli, jonka JetBrains on kehittänyt olemaan täysin yhteentoimiva [Java](/programming/java/):n kanssa. Kotlin-tavaramerkki on Kotlin-säätiön suojaama.

Kotlin was announced as the preferred programming language for Android App development by Google on 7th May 2019. Android Studio 3.0 aloitti Kotlinin tukemisen vaihtoehtona Android-sovelluskehityksessä lokakuussa 2017.

## Kotlin KT -tiedostomuodon ## lyhyt historia

JetBrains paljasti Kotlinin heinäkuussa 2011 uutena ohjelmointikielenä JVM:lle. JetBrainsin johtaja Dmitri Jemerov sanoi, että useimmista kielistä puuttui Scalaa lukuun ottamatta etsimiä ominaisuuksia, mutta Scalan hidas käännös oli haittapuoli. Yksi Kotlinin päätavoitteista oli kääntää yhtä nopeasti kuin Java. Kotlin-projekti oli avoimen lähdekoodin alla Apache 2 -lisenssillä helmikuussa 2012.

Version 1.0 of Kotlin was released on 15 February 2015. Android julkisti ensiluokkaisen tuen Kotlinille Androidissa Google I/O 2017 -tapahtumassa. Kotlin 1.2 julkaistiin 28. marraskuuta 2017, ja se pystyi jakamaan koodia JVM- ja JavaScript-alustojen välillä. Kotlin 1.3 julkaistiin 29.10.2018 asynkronisen ohjelmoinnin tuella. Google ilmoitti Kotlinin ensisijaiseksi ohjelmointikieleksi Android-sovelluskehityksessä 7. toukokuuta 2019. Kotlin 1.4 julkaistiin elokuussa 2020 pienin muutoksin tukemaan yhteentoimivuutta Swift/Objective-C:n kanssa.

## Kotlinin syntaksi ##

Kotlin suunniteltiin Javaa paremmaksi, mutta silti yhteentoimivaksi Java-koodin kanssa mahdollistaakseen asteittaisen siirtymisen Javasta Kotliniin.

 * Puolipisteet ovat valinnaisia Kotlinissa. Uusi rivi riittää osoittamaan lauseen lopun.
 * Kotlin tukee kahdenlaisia muuttujia, vain luku -muotoisia, jotka määritellään *val*-avainsanalla, ja muuttuvia, jotka määritellään avainsanalla *var*.
 * Luokat ovat oletuksena yksityisiä ja lopullisia. Luokasta johtamiseksi perusluokka on ilmoitettava avainsanalla *open*.
 * Kotlin tukee myös prosessiohjelmointia.
 * Kotlin-ohjelman sisääntulopiste on pää-toiminto, joka on samanlainen kuin Java, C# jne.

### Syntaksiesimerkki ###

Seuraava on esimerkki Kotlin-syntaksista.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Yllä olevassa koodissa avainsana **fun** määrittää toiminnon nimeltä main. Funktion sisällä vain luku -muotoinen muuttuja yleisö ilmoitetaan avainsanalla **val**. **println**-menetelmää käyttämällä Hello World from Kotlin tulostetaan konsoliin. Muuttujan yleisön arvo syötetään merkkijonoon **$**-merkillä.

## Kotlin vs Java
Kotlin on virallinen kieli Android-sovellusten kirjoittamiseen ja tarjoaa monia edistyneitä ominaisuuksia, mutta monet kokeneet Java-kehittäjät eivät silti osoita kiinnostuksensa vaihtaa Kotliniin. He ajattelevat voivansa tehdä kaiken vain Javalla. Joten seuraava on vertailu kahden tekniikan välillä, jotka voivat vakuuttaa java-kehittäjät vaihtamaan:

| Parametri | Java | Kotlin |
|--------------------|------------|----------------- -|
| Singletons Objects | √ | √ |
| Jokerimerkkityypit | √ | Χ |
| Kokoelma | Tavukoodit | Virtuaalikone |
| Lambda Expression | Χ | √ |
| Invarianttitaulukko | Χ | √ |
| Ei-yksityiset kentät | √ | Χ |
| Smart Casts | Χ | √ |
| Nollaturvallisuus | Χ | √ |
| Staattiset jäsenet | √ | Χ |

## Viitteet ##

- {{HYPERLINKKI}})

