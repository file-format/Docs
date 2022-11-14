{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Estensione file INC - Che cos'è un file INC?",
  "description":"Ulteriori informazioni sul formato di file INC Include e sulle API che possono creare e aprire file INC.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Che cos'è un file INC?

Un file INC è un file di inclusione utilizzato dal codice sorgente del programma software per fare riferimento alle informazioni sulle intestazioni. È simile al [formato file .h](/it/programmazione/h/) e contiene dichiarazioni, funzioni, intestazioni o macro che possono essere riutilizzate da file di codice sorgente come C++. I file INC sono utilizzati da una varietà di linguaggi di programmazione come C, [C++](/it/programming/cpp/), Pascal, [PHP](/it/programming/php/) e [Java](/it/programming/java/). Editor di testo come Microsoft Notepad, Notepad++ e TextEdit possono essere utilizzati per aprire i file INC.

## Formato file INC - Ulteriori informazioni

Un file INC viene salvato come file di testo normale con tutte le dichiarazioni incluse secondo la sintassi della dichiarazione. Un file INC può fare riferimento anche ad altri file INC. Una volta creato, il file INC diventa parte del progetto e può essere referenziato da file di origine come C++. Può essere referenziato da più file di origine per evitare qualsiasi duplicazione.

## Contenuto del file INC

I file INC possono includere le seguenti informazioni.

**`Variabili`** - In caso di programmazione orientata agli oggetti (OOP), un file di intestazione di classe contiene le definizioni di tutte le variabili a livello di classe accessibili attraverso i file di codice sorgente dell'implementazione

**`Dichiarazione dei metodi`** - Tutte le dichiarazioni dei metodi sono incluse nei file di intestazione .h per essere accessibili in più file di implementazione.

**`Definizioni di funzioni non in linea`** - I file di intestazione possono anche contenere definizioni di metodi non in linea.

## Svantaggio dell'utilizzo del file INC in PHP

PHP sono script lato server che vengono eseguiti sul server e restituiscono i risultati alle pagine Web chiamanti. Se un file PHP fa riferimento a un file INC e il server non è configurato per analizzare i file .inc (cosa molto comune), un utente può visualizzare il codice sorgente php nel file .inc visitando la directory URL. Quindi, bisogna stare attenti durante l'utilizzo di file INC come file di inclusione in PHP.

## Riferimenti

* [Utilizzo di INC in PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

