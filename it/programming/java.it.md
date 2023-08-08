---
date: 2019-10-11
keywords: java, .java, formato file java, come aprire file java, come eseguire file java, file java, codice di esempio java
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file Java
linktitle: Java
description: "Scopri il formato di file Java e le API che possono creare e aprire file Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Che cos'è un file Java? ##
Un file contenente codice sorgente Java e salvato con estensione .java è noto come file Java. Java è una delle tecnologie più utilizzate per lo sviluppo di giochi, applicazioni mobili, web e desktop. Poiché Java è indipendente dalla piattaforma, funziona perfettamente su Windows, Mac, Linux, Raspberry Pi, ecc. Java è molto simile a C# e C++, quindi è più facile passare da una lingua all'altra.

## Breve storia ##

Il progetto Java è stato avviato nel giugno 1991 da James Gosling, Mike Sheridan e Patrick Naughton. Java inizialmente si chiamava Oak. Successivamente è stato ribattezzato Green e infine Java. James Gosling ha progettato Java con una sintassi simile a C/C++. La prima versione pubblica di Java è stata rilasciata nel 1996 da Sun Microsystems. Potrebbe funzionare su tutti i sistemi popolari che hanno reso popolare Java rapidamente. Con il rilascio di Java 2 nel dicembre 1998, sono state create più configurazioni per diversi tipi di piattaforme. Le versioni erano le seguenti

- J2EE (Java EE): per soluzioni aziendali
- J2ME (Java ME): per applicazioni mobili
- J2SE (Java SE): per applicazioni desktop

Il 19 novembre 2006, Java Virtual Machine (JVM) è stata rilasciata da Sun come software gratuito e open source. Dopo che Oracle Corporation ha acquisito Sun Microsystems nel 2009-2010, James Gosling si è dimesso da Oracle il 2 aprile 2010.

## Come eseguire/eseguire il codice Java ##

Per eseguire il codice Java, è necessario prima compilarlo. Per questo, è richiesto l'SDK Java. Java SDK compila il codice Java in un file di classe bytecode. Esistono IDE come Eclipse e IntelliJ Idea che semplificano il lavoro con i file Java fornendo il completamento del codice e un'interfaccia facile da usare per compilare ed eseguire il codice Java.

## Formato file Java ##

La sintassi di Java è stata fortemente influenzata da C e C++ ma, a differenza di C++, Java è stato costruito quasi esclusivamente come linguaggio orientato agli oggetti. In Java, tutto il codice è scritto all'interno delle classi e ogni dato è un oggetto. A differenza di C++, Java non supporta l'overloading degli operatori o l'ereditarietà multipla.

### Codice di esempio Java ###

Quello che segue è un esempio di sintassi Java.

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
Nel codice sopra, la parola chiave **public** indica il modificatore di accesso. Afferma che a questa classe possono accedere le classi al di fuori della gerarchia di classi. Il modificatore di accesso può anche essere **protetto** (accessibile nello stesso pacchetto) o **privato** (i metodi sono accessibili solo dalla stessa classe). **static** davanti al metodo indica che il metodo può essere invocato senza un'istanza specifica della classe. **void** indica che il metodo non restituirebbe nulla. Per stampare la stringa sulla console. Viene utilizzato il comando System.out.println. In questo comando, la classe *System* ha un campo statico *out* che è un'istanza della classe *PrintStream* contenente il metodo *println*.

Il nome del file dei file Java dovrebbe essere lo stesso del nome della classe. Quindi il file Java per il codice di esempio sarebbe chiamato *ExampleApp.java*.

## Riferimenti ##

- [Java (linguaggio di programmazione) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

