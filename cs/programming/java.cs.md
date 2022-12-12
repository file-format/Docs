---
date: 2019-10-11
keywords: java, .java, formát souboru java, jak otevřít soubory java, jak spouštět soubory java, soubor java, ukázkový kód java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru Java
linktitle: Java
description: "Přečtěte si o formátu souborů Java a rozhraních API, která mohou vytvářet a otevírat soubory Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Co je to Java soubor? ##
Soubor obsahující zdrojový kód Java a uložený s příponou .java se nazývá soubor Java. Java je jednou z nejpoužívanějších technologií pro vývoj her, mobilních, webových a desktopových aplikací. Protože je Java nezávislá na platformě, funguje bezchybně na Windows, Mac, Linux, Raspberry Pi atd. Java je velmi podobná C# a C++, takže je snazší mezi těmito jazyky přepínat.

## Stručná historie ##

Projekt Java iniciovali v červnu 1991 James Gosling, Mike Sheridan a Patrick Naughton. Java se zpočátku jmenovala Oak. Později byla přejmenována na Green a nakonec na Java. James Gosling navrhl Javu se syntaxí podobnou C/C++. První veřejná verze Javy byla vydána v roce 1996 společností Sun Microsystems. Mohlo to běžet na všech populárních systémech, které způsobily, že se Java rychle stala populární. S vydáním Java 2 v prosinci 1998 bylo vytvořeno několik konfigurací pro různé typy platforem. Verze byly následující

- J2EE (Java EE): Pro podniková řešení
- J2ME (Java ME): Pro mobilní aplikace
- J2SE (Java SE): Pro desktopové aplikace

19. listopadu 2006 vydala společnost Sun Java Virtual Machine (JVM) jako bezplatný software s otevřeným zdrojovým kódem. Poté, co Oracle Corporation získala Sun Microsystems v letech 2009–2010, James Gosling odstoupil z Oracle dne 2. dubna 2010.

## Jak spustit/spustit Java kód ##

Aby bylo možné spustit kód Java, musí být nejprve zkompilován. K tomu je zapotřebí Java SDK. Java SDK zkompiluje kód Java do souboru třídy bytecode. Existují IDE jako Eclipse a IntelliJ Idea, které usnadňují práci se soubory Java tím, že poskytují dokončování kódu a snadno použitelné rozhraní pro kompilaci a spouštění kódu Java.

## Formát souboru Java ##

Syntaxe Javy byla silně ovlivněna C a C++, ale na rozdíl od C++ byla Java vytvořena téměř výhradně jako objektově orientovaný jazyk. V Javě je veškerý kód zapsán uvnitř tříd a každá datová položka je objekt. Na rozdíl od C++ Java nepodporuje přetěžování operátorů ani vícenásobnou dědičnost.

### Ukázkový kód Java ###

Následuje příklad syntaxe Java.

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
Ve výše uvedeném kódu klíčové slovo **public** označuje modifikátor přístupu. Uvádí, že k této třídě mohou přistupovat třídy mimo hierarchii tříd. Modifikátor přístupu může být také **chráněný** (lze přistupovat ve stejném balíčku) nebo **soukromý** (k metodám má přístup pouze stejná třída). **statický** před metodou označuje, že metodu lze vyvolat bez konkrétní instance třídy. **void** znamená, že metoda nevrací nic. Chcete-li vytisknout řetězec do konzoly. Je použit příkaz System.out.println. V tomto příkazu má třída *System* statické pole *out*, které je instancí třídy *PrintStream* obsahující metodu *println*.

Název souboru Java souborů by měl být stejný jako název třídy. Soubor Java pro ukázkový kód by se tedy jmenoval *ExampleApp.java*.

## Reference ##

- [Java (programovací jazyk) - Wikipedie](https://en.wikipedia.org/wiki/Java_(programming_language))

