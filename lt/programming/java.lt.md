---
date: 2019-10-11
keywords: java, .java, java file format, how to open java files, how to run java files, java file, java sample code
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java failo formaat
linktitle: Java
description: Luždirbti apie Java failo formatą ir API, kurios gali sukurti ir atidaryti Java failąs.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Kas yra Java failas? ##
Failas su Java šaltinio kodu ir išsaugotas .java failo plėtiniu yra žinomas kaip Java failas. Java yra viena iš plačiausiai naudojamų žaidimų, mobiliųjų, žiniatinklio ir darbalaukio programų kūrimo technologijų. Kadangi Java yra nepriklausoma nuo platformos, ji nepriekaištingai veikia Windows, Mac, Linux, Raspberry Pi ir kt. Java yra labai panaši į C# ir C++, todėl lengviau perjungti šias kalbas.

## Trumpa istorija ##

Java projektą 1991 m. birželį inicijavo Jamesas Goslingas, Mike'as Sheridanas ir Patrickas Naughtonas. Java iš pradžių buvo pavadintas Ąžuolu. Vėliau jis buvo pervadintas į Green ir galiausiai į Java. Jamesas Goslingas sukūrė Java su sintaksė, panašia į C/C++. Pirmąją viešą Java versiją 1996 m. išleido Sun Microsystems. Jis galėjo veikti visose populiariose sistemose, dėl kurių Java greitai išpopuliarėjo. 1998 m. gruodį išleidus Java 2, buvo sukurtos kelios skirtingų tipų platformų konfigūracijos. Versijos buvo tokios

- J2EE (Java EE): įmonės sprendimams
- J2ME (Java ME): mobiliosioms programoms
- J2SE (Java SE): staliniams kompiuteriams skirtoms programoms

2006 m. lapkričio 19 d. Sun išleido Java Virtual Machine (JVM) kaip nemokamą atvirojo kodo programinę įrangą. 2009–2010 m. Oracle Corporation įsigijus Sun Microsystems, 2010 m. balandžio 2 d. Jamesas Goslingas atsistatydino iš Oracle.

## Kaip paleisti / vykdyti Java kodą ##

Norint vykdyti Java kodą, pirmiausia jį reikia sukompiliuoti. Tam reikalingas Java SDK. Java SDK sukompiliuoja Java kodą į baitinio kodo klasės failą. Yra tokių IDE kaip Eclipse ir IntelliJ Idea, kurios palengvina darbą su Java failais, nes suteikia kodo užbaigimą ir paprastą naudoti sąsają Java kodui kompiliuoti ir vykdyti.

## Java failo formatas ##

Java sintaksę labai paveikė C ir C++, tačiau skirtingai nei C++, Java buvo sukurta beveik vien kaip į objektą orientuota kalba. Java programoje visas kodas parašytas klasėse, o kiekvienas duomenų elementas yra objektas. Priešingai nei C++, Java nepalaiko operatoriaus perkrovos ar daugybinio paveldėjimo.

### Java pavyzdinis kodas ###

Toliau pateikiamas Java sintaksės pavyzdys.

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
Aukščiau pateiktame kode **viešasis** raktinis žodis reiškia prieigos modifikatorių. Jame teigiama, kad šią klasę gali pasiekti klasės už klasių hierarchijos ribų. Prieigos modifikatorius taip pat gali būti **apsaugotas** (gali būti pasiekiamas tame pačiame pakete) arba **privatus** (metodus gali pasiekti tik ta pati klasė). **static** prieš metodą rodo, kad metodas gali būti iškviestas be konkretaus klasės egzemplioriaus. **tuščia** rodo, kad metodas nieko negrąžins. Norėdami atspausdinti eilutę į konsolę. Naudojama komanda System.out.println. Šioje komandoje *System* klasė turi statinį lauką *out*, kuris yra *PrintStream* klasės, kurioje yra *println* metodas, pavyzdys.

Java failų failo pavadinimas turi būti toks pat kaip klasės pavadinimas. Taigi pavyzdinio kodo Java failas būtų pavadintas *ExampleApp.java*.

## Nuorodos Nr.

- [Java (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

