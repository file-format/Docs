{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c", "che cos'è il file ac", "come aprire il file c", "estensione", "file", "file c", "formato file c", "estensione file c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File di programmazione del linguaggio C - C",
  "description":"Scopri il formato di file C e le API che possono creare e aprire file C.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Che cos'è un file C?

Un file salvato con estensione c è un file di codice sorgente scritto nel linguaggio di programmazione C. Il **file C** include tutta l'implementazione delle funzionalità dell'applicazione sotto forma di codice sorgente. La dichiarazione del codice sorgente viene scritta nei file di intestazione che vengono salvati con estensione [.h](/it/programmazione/h/). C++ è la forma moderna del linguaggio C ed è utilizzato per sviluppare la maggior parte del software al giorno d'oggi.

## Breve storia

Il linguaggio C è nato come risultato della creazione di diverse utilità per il sistema operativo UNIX. Denis Ritchie, l'uomo dietro la creazione di questo linguaggio di programmazione, il lavoro iniziò originariamente negli anni '60 e all'inizio degli anni '70.

## Formato file C

I file C sono scritti in formato di file di testo normale seguendo la sintassi del linguaggio di programmazione. Un tipico file C avrà:

* istruzione import nella parte superiore del file per importare qualsiasi file di intestazione
* uno o più metodi per implementare la funzionalità desiderata

### Importazione di intestazioni

I file di intestazione, con estensione .h, contengono le istruzioni include necessarie per includere altri file di funzionalità nel progetto. Inoltre, questi contengono le dichiarazioni dei metodi definiti nel file di implementazione. I file di intestazione sono inclusi utilizzando l'istruzione include come mostrato di seguito.

```
#include <filename.h>
```

### Implementazione del codice sorgente

L'effettiva implementazione dei requisiti funzionali è codificata come metodi nel file C. Ciascun metodo in un file C ha un tipo restituito, un nome del metodo e potrebbe avere alcuni parametri di input. Se il tipo restituito non è void, il metodo potrebbe restituire un valore.

### Esempio di codice C
Ecco un programma di esempio ac:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Riferimenti** ##

* [Implementazione della classe - Da Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

