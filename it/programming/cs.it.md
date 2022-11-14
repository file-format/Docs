{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "file", "estensione", "formato file", "CSharp", "Linguaggio di programmazione" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - File di codice CSharp",
  "description":"Scopri il formato di file CS e le API che possono creare e aprire file CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file CS?

I file con estensione .cs sono file di codice sorgente per il linguaggio di programmazione C#. Introdotto da Microsoft per l'uso con .NET Framework, il formato di file fornisce il linguaggio di programmazione di basso livello per la scrittura di codice che viene compilato per generare il file di output finale sotto forma di EXE o DLL. Questi possono essere creati e compilati con Microsoft Visual Studio. Microsoft Visual Studio Express può anche essere utilizzato per creare e aggiornare tali file che è un IDE gratuito. I file CS vengono utilizzati per lo sviluppo di applicazioni che possono variare da semplici applicazioni desktop a programmi più complessi. Un semplice progetto di Visual Studio [soluzione](/it/programmazione/sln/) creato con il linguaggio C# può comprendere uno o più di questi file. I file contrassegnati per l'inclusione nella compilazione sono elencati nel file [CSPROJ](/it/programming/csproj/) che fa parte del progetto e indica al compilatore di utilizzare i file contrassegnati.

## Formato file CS ##

I file CS sono formati di file basati su testo che possono essere aperti in qualsiasi editor di testo per la modifica. Tuttavia, quando viene aperto in un IDE supportato con un'evidenziazione della sintassi adeguata, il codice è facile da leggere e organizzare. Un semplice file CS contiene:

* Dichiarazione degli spazi dei nomi - Per fare riferimento a una particolare funzionalità definita da quello specifico spazio dei nomi
* Dichiarazione di variabili - Per dichiarare variabili a livello di classe per l'implementazione particolare
* Dichiarazione dei metodi - Per dichiarare la dichiarazione dei metodi per la particolare funzionalità

### Sintassi ###

* I punti e virgola sono usati per denotare la fine di un'istruzione.
* Le parentesi graffe vengono utilizzate per raggruppare le affermazioni. Le istruzioni sono comunemente raggruppate in metodi (funzioni), metodi in classi e classi in spazi dei nomi.
* Le variabili vengono assegnate utilizzando un segno di uguale, ma confrontate utilizzando due segni di uguale consecutivi.
* Le parentesi quadre vengono utilizzate con gli array, sia per dichiararli che per ottenere un valore in un determinato indice in uno di essi.

### Esempio ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

