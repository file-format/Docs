---
date: 2019-10-11
keywords: kt, .kt, formato file kotlin, come aprire file kotlin, come eseguire file kotlin, formato file .kt, file kt, estensione file kotlin, estensione .kt, kotlin vs java
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file KT
linktitle: KT
description: "Scopri il formato di file KT e le API che possono creare e aprire file KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Che cos'è un file KT? ##

Un codice sorgente scritto in Kotlin viene salvato con estensione .kt, comunemente nota come **estensione file Kotlin**. Kotlin è un linguaggio di programmazione multipiattaforma generico sviluppato da JetBrains per essere completamente interoperabile con [Java](/it/programming/java/). Il marchio Kotlin è protetto dalla Fondazione Kotlin.

Kotlin è stato annunciato come linguaggio di programmazione preferito per lo sviluppo di app Android da Google il 7 maggio 2019. Android Studio 3.0 ha iniziato a supportare Kotlin come alternativa per lo sviluppo di app Android nell'ottobre 2017.

## Breve storia del formato file Kotlin KT##

Kotlin è stato presentato da JetBrains nel luglio 2011 come nuovo linguaggio di programmazione per JVM. Il protagonista di JetBrains Dmitry Jemerov ha affermato che alla maggior parte dei linguaggi mancavano le funzionalità che stavano cercando tranne Scala, ma la lenta compilazione di Scala era uno svantaggio. Uno degli obiettivi principali di Kotlin era compilare velocemente come Java. Il progetto Kotlin è stato open source con licenza Apache 2 nel febbraio 2012.

La versione 1.0 di Kotlin è stata rilasciata il 15 febbraio 2015. Android ha annunciato il supporto di prima classe per Kotlin su Android al Google I/O 2017. Kotlin 1.2 è stato rilasciato il 28 novembre 2017 con la possibilità di condividere il codice tra JVM e piattaforme JavaScript. Kotlin 1.3 è stato rilasciato il 29 ottobre 2018 con il supporto per la programmazione asincrona. Google ha annunciato Kotlin come linguaggio di programmazione preferito per lo sviluppo di app Android il 7 maggio 2019. Kotlin 1.4 è stato rilasciato nell'agosto 2020 con alcune lievi modifiche per supportare l'interoperabilità con Swift/Objective-C.

## Sintassi Kotlin ##

Kotlin è stato progettato per essere migliore di Java ma essere comunque interoperabile con il codice Java per consentire la migrazione graduale da Java a Kotlin.

* I punti e virgola sono facoltativi in Kotlin. È sufficiente una nuova riga per indicare la fine dell'istruzione.
* Kotlin supporta due tipi di variabili, di sola lettura, definite dalla parola chiave *val*, e modificabili, definite dalla parola chiave *var*.
* Le lezioni sono private e finali per impostazione predefinita. Per derivare da una classe, la classe base deve essere dichiarata con la parola chiave *open*.
* Kotlin supporta anche la programmazione procedurale.
* Il punto di ingresso al programma Kotlin è la funzione "principale" simile a Java, C#, ecc.

### Esempio di sintassi ###

Quello che segue è un esempio di sintassi di Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Nel codice sopra, la parola chiave **fun** definisce la funzione denominata main. All'interno della funzione, viene dichiarata una variabile di sola lettura 'audience' con la parola chiave **val**. Utilizzando il metodo **println**, sulla console viene stampato "Hello World from Kotlin". Il valore della variabile audience viene inserito nella stringa con il segno **$**.

## Kotlin contro Java
Kotlin è una lingua ufficiale per scrivere app Android con molte funzionalità avanzate, ma molti sviluppatori Java esperti non mostrano ancora il loro interesse a passare a Kotlin. Pensano di poter fare tutto solo con Java. Di seguito è riportato il confronto tra due tecnologie che potrebbero convincere gli sviluppatori java a passare:

| parametro | Giava | Kotlin |
|--------------------|------------|---------------- -|
| Oggetti singleton | √ | √ |
| Tipi di caratteri jolly | √ | Χ |
| compilazione | Bytecode | Macchina virtuale |
| Espressione Lambda | Χ | √ |
| Matrice invariante | Χ | √ |
| Campi non privati | √ | Χ |
| Cast intelligenti | Χ | √ |
| Sicurezza nulla | Χ | √ |
| Membri statici | √ | Χ |

## Riferimenti ##

- [Kotlin (linguaggio di programmazione) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(linguaggio_di_programmazione))

