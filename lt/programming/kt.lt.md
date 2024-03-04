---
date: 2019-10-11
keywords: kt, .kt, kotlin file format, how to open kotlin files, how to run kotlin files, .kt file format, kt file , kotlin file extension, .kt extention, kotlin vs java
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT Failo formaat
linktitle: KT
description: Luždirbkite apie KT failo formatą ir API, kurios gali sukurti ir atidaryti KT failąs.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Kas yra KT failas? ##

Kotlin parašytas šaltinio kodas išsaugomas su plėtiniu .kt, kuris paprastai žinomas kaip **Kotlin failo plėtinys**. Kotlin yra bendros paskirties kelių platformų programavimo kalba, kurią sukūrė JetBrains, kad ji būtų visiškai suderinama su [Java](/programming/java/). Kotlin prekės ženklą saugo Kotlin fondas.

Kotlin was announced as the preferred programming language for Android App development by Google on 7th May 2019. Android Studio 3.0 pradėjo palaikyti Kotlin kaip alternatyvą Android programų kūrimui 2017 m. spalio mėn.

## Trumpa Kotlin KT failo formato ## istorija

2011 m. liepos mėn. JetBrains pristatė Kotliną kaip naują JVM programavimo kalbą. JetBrains vadovas Dmitrijus Jemerovas teigė, kad daugumoje kalbų trūksta funkcijų, kurių jie ieškojo, išskyrus Scala, tačiau lėtas Scala kompiliavimas buvo trūkumas. Vienas iš pagrindinių Kotlin tikslų buvo kompiliuoti taip pat greitai, kaip ir Java. 2012 m. vasario mėn. Kotlin projektas buvo sukurtas pagal Apache 2 licenciją.

Version 1.0 of Kotlin was released on 15 February 2015. Android paskelbė apie aukščiausios klasės Kotlin palaikymą Android sistemoje Google I/O 2017. 2017 m. lapkričio 28 d. buvo išleista Kotlin 1.2 versija su galimybe dalytis kodu tarp JVM ir JavaScript platformų. Kotlin 1.3 buvo išleistas 2018 m. spalio 29 d. su asinchroninio programavimo palaikymu. 2019 m. gegužės 7 d. Google paskelbė, kad Kotlin bus pageidaujama programavimo kalba kuriant Android programas. Kotlin 1.4 versija buvo išleista 2020 m. rugpjūčio mėn. su nedideliais pakeitimais, kad būtų palaikoma sąveika su Swift / Objective-C.

## Kotlino sintaksė ##

Kotlin buvo sukurtas taip, kad būtų geresnis nei Java, bet vis tiek būtų suderinamas su Java kodu, kad būtų galima laipsniškai pereiti iš Java į Kotlin.

 * Kabliataškiai yra neprivalomi Kotlin. Teiginio pabaigai nurodyti pakanka naujos eilutės.
 * Kotlin palaiko dviejų tipų kintamuosius: tik skaitomus, apibrėžtus *val* raktiniu žodžiu, ir kintamuosius, apibrėžtus *var* raktiniu žodžiu.
 * Pagal numatytuosius nustatymus užsiėmimai yra privatūs ir galutiniai. Norint gauti iš klasės, pagrindinė klasė turi būti deklaruota naudojant raktinį žodį *open*.
 * Kotlin taip pat palaiko procedūrinį programavimą.
 * Kotlin programos įėjimo taškas yra pagrindinė funkcija, panaši į Java, C# ir kt.

### Sintaksės pavyzdys ###

Toliau pateikiamas Kotlino sintaksės pavyzdys.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Aukščiau pateiktame kode raktinis žodis **fun** apibrėžia funkciją, pavadintą main. Funkcijos viduje tik skaitomas kintamasis auditorija deklaruojamas naudojant raktinį žodį **val**. Naudojant **println** metodą, ant konsolės atspausdinamas Hello World from Kotlin. Kintamosios auditorijos reikšmė įvedama į eilutę su **$** ženklu.

## Kotlin prieš Java
Kotlin yra oficiali kalba, skirta rašyti Android programėles, siūlančias daug pažangių funkcijų, tačiau daugelis patyrusių Java kūrėjų vis tiek nerodo savo susidomėjimo pereiti prie Kotlin. Jie mano, kad viską gali padaryti tik su Java. Taigi toliau pateikiamas dviejų technologijų, kurios gali įtikinti java kūrėjus pereiti, palyginimas:

| Parametras | Java | Kotlin |
|--------------------|------------|----------------- -|
| Singletons objektai | √ | √ |
| Pakaitos simbolių tipai | √ | Χ |
| Kompiliacija | Baitų kodai | Virtuali mašina |
| Lambda išraiška | Χ | √ |
| Nekintamasis masyvas | Χ | √ |
| Neprivatūs laukai | √ | Χ |
| Smart Casts | Χ | √ |
| Nulinė sauga | Χ | √ |
| Statiški nariai | √ | Χ |

## Nuorodos Nr.

- [Kotlin (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

