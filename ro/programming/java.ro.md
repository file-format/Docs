---
date: 2019-10-11
keywords: java, .java, format de fișier java, cum să deschideți fișiere java, cum să rulați fișiere java, fișier java, exemplu de cod java
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier Java
linktitle: Java
description: "Aflați despre formatul de fișier Java și despre API-urile care pot crea și deschide fișiere Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Ce este un fișier Java? ##
Un fișier care conține cod sursă Java și salvat cu extensia de fișier .java este cunoscut ca fișier Java. Java este una dintre cele mai utilizate tehnologii pentru dezvoltarea de jocuri, aplicații mobile, web și desktop. Deoarece Java este independent de platformă, funcționează perfect pe Windows, Mac, Linux, Raspberry Pi etc. Java este foarte asemănător cu C# și C++, așa că este mai ușor să comutați între aceste limbi.

## Scurt istoric ##

Proiectul Java a fost inițiat în iunie 1991 de James Gosling, Mike Sheridan și Patrick Naughton. Java a fost inițial numit Oak. Mai târziu a fost redenumit Green și în cele din urmă în Java. James Gosling a proiectat Java cu o sintaxă similară cu C/C++. Prima versiune publică de Java a fost lansată în 1996 de Sun Microsystems. Ar putea rula pe toate sistemele populare care au făcut ca Java să devină popular rapid. Odată cu lansarea Java 2 în decembrie 1998, au fost construite mai multe configurații pentru diferite tipuri de platforme. Versiunile au fost după cum urmează

- J2EE (Java EE): Pentru soluții de întreprindere
- J2ME (Java ME): Pentru aplicații mobile
- J2SE (Java SE): Pentru aplicații desktop

Pe 19 noiembrie 2006, Java Virtual Machine (JVM) a fost lansat de Sun ca software gratuit și open-source. După ce Oracle Corporation a achiziționat Sun Microsystems în 2009–2010, James Gosling a demisionat din Oracle pe 2 aprilie 2010.

## Cum să rulezi/execuți codul Java ##

Pentru a executa codul Java, acesta trebuie mai întâi compilat. Pentru aceasta, este necesar Java SDK. Java SDK compilează codul Java într-un fișier de clasă bytecode. Există IDE-uri precum Eclipse și IntelliJ Idea care facilitează lucrul cu fișierele Java, oferind completarea codului și o interfață ușor de utilizat pentru compilarea și executarea codului Java.

## Format de fișier Java ##

Sintaxa Java a fost foarte influențată de C și C++, dar spre deosebire de C++, Java a fost construit aproape exclusiv ca un limbaj orientat pe obiecte. În Java, tot codul este scris în clase și fiecare element de date este un obiect. Spre deosebire de C++, Java nu acceptă supraîncărcarea operatorului sau moștenirea multiplă.

### Exemplu de cod Java ###

Următorul este un exemplu de sintaxă Java.

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
În codul de mai sus, cuvântul cheie **public** denotă modificatorul de acces. Afirmă că această clasă poate fi accesată de clasele din afara ierarhiei claselor. Modificatorul de acces mai poate fi **protejat** (poate fi accesat în același pachet) sau **privat** (metodele pot fi accesate doar de aceeași clasă). **static** din fața metodei indică faptul că metoda poate fi invocată fără o instanță specifică a clasei. **void** indică faptul că metoda nu va returna nimic. Pentru a imprima șirul pe consolă. Este folosită comanda System.out.println. În această comandă, clasa *System* are un câmp static *out* care este o instanță a clasei *PrintStream* care conține metoda *println*.

Numele fișierelor Java ar trebui să fie același cu numele clasei. Deci fișierul Java pentru codul exemplu ar fi numit *ExampleApp.java*.

## Referințe ##

- [Java (limbaj de programare) - Wikipedia](https://en.wikipedia.org/wiki/Java_(limbaj_de_programare))

