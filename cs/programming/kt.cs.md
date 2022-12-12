---
date: 2019-10-11
keywords: kt, .kt, formát souboru kotlin, jak otevřít soubory kotlin, jak spustit soubory kotlin, formát souboru .kt, soubor kt , přípona souboru kotlin, rozšíření .kt, kotlin vs java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru KT
linktitle: KT
description: "Přečtěte si o formátu souboru KT a rozhraních API, která mohou vytvářet a otevírat soubory KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Co je soubor KT? ##

Zdrojový kód napsaný v Kotlinu je uložen s příponou .kt, která je běžně známá jako **přípona souboru Kotlin**. Kotlin je univerzální multiplatformní programovací jazyk vyvinutý společností JetBrains, aby byl plně interoperabilní s [Java](/cs/programming/java/). Ochranná známka Kotlin je chráněna Kotlin Foundation.

Kotlin byl oznámen jako preferovaný programovací jazyk pro vývoj aplikací pro Android společností Google dne 7. května 2019. Android Studio 3.0 začalo podporovat Kotlin jako alternativu pro vývoj aplikací pro Android v říjnu 2017.

## Stručná historie formátu souboru Kotlin KT##

Kotlin byl představen JetBrains v červenci 2011 jako nový programovací jazyk pro JVM. Vedoucí JetBrains Dmitrij Jemerov řekl, že většině jazyků chyběly funkce, které hledali, kromě Scaly, ale pomalá kompilace Scaly byla nevýhodou. Jedním z hlavních cílů Kotlinu bylo zkompilovat stejně rychle jako Java. Projekt Kotlin byl otevřen pod licencí Apache 2 v únoru 2012.

Verze 1.0 Kotlinu byla vydána 15. února 2015. Android oznámil prvotřídní podporu pro Kotlin na Androidu na Google I/O 2017. Kotlin 1.2 byl vydán 28. listopadu 2017 s možností sdílet kód mezi platformami JVM a JavaScript. Kotlin 1.3 byl vydán 29. října 2018 s podporou asynchronního programování. Google oznámil Kotlin jako preferovaný programovací jazyk pro vývoj aplikací pro Android dne 7. května 2019. Kotlin 1.4 byl vydán v srpnu 2020 s několika drobnými změnami na podporu interoperability s Swift/Objective-C.

## Kotlin syntaxe ##

Kotlin byl navržen tak, aby byl lepší než Java, ale stále byl interoperabilní s kódem Java, aby umožnil postupnou migraci z Java na Kotlin.

* Středníky jsou v Kotlinu volitelné. Pro označení konce výpisu stačí nový řádek.
* Kotlin podporuje dva typy proměnných, pouze pro čtení, definované klíčovým slovem *val*, a proměnlivé, definované klíčovým slovem *var*.
* Třídy jsou ve výchozím nastavení soukromé a konečné. Pro odvození od třídy musí být základní třída deklarována pomocí klíčového slova *open*.
* Kotlin také podporuje procedurální programování.
* Vstupním bodem do programu Kotlin je „hlavní“ funkce podobná Javě, C# atd.

### Příklad syntaxe ###

Následuje příklad syntaxe Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Ve výše uvedeném kódu klíčové slovo **fun** definuje funkci s názvem main. Uvnitř funkce je deklarována proměnná pouze pro čtení 'audience' s klíčovým slovem **val**. Pomocí metody **println** se na konzoli vytiskne „Hello World from Kotlin“. Hodnota proměnné publikum se vloží do řetězce se znakem **$**.

## Kotlin vs Java
Kotlin je oficiální jazyk pro psaní aplikací pro Android s nabídkou mnoha pokročilých funkcí, ale mnoho zkušených vývojářů Java stále neprojevuje zájem přejít na Kotlin. Myslí si, že vše dokážou pouze s Javou. Následuje tedy srovnání dvou technologií, které mohou vývojáře Java přesvědčit, aby přešli:

| Parametr | Java | Kotlin |
|--------------------|-----------|----------------- -|
| Singletonové objekty | √ | √ |
| Typy zástupných znaků | √ | Χ |
| Kompilace | Bytekódy | Virtuální stroj |
| Lambda Expression | Χ | √ |
| Invariantní pole | Χ | √ |
| Nesoukromá pole | √ | Χ |
| Chytré obsazení | Χ | √ |
| Null Safety | Χ | √ |
| Statické členy | √ | Χ |

## Reference ##

- [Kotlin (programovací jazyk) - Wikipedie](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

