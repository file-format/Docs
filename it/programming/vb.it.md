{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "file", "estensione", "formato file", "Visual Basic", "Guida alla programmazione" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - File di codice Visual Basic",
  "description":"Scopri il formato di file VB e le API che possono creare e aprire file VB.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file VB?

Un file VB è un file di codice sorgente creato in linguaggio Visual Basic che è stato creato da Microsoft per lo sviluppo di applicazioni .NET. Un altro linguaggio simile con sintassi diversa è C# i cui file vengono salvati con l'estensione di file [.CS](/it/programming/cs/). Il formato di file fornisce il linguaggio di programmazione di basso livello per la scrittura di codice che viene compilato per generare il file di output finale sotto forma di EXE o DLL. Questi possono essere creati e compilati con Microsoft Visual Studio. Microsoft Visual Studio Express può anche essere utilizzato per creare e aggiornare tali file che è un IDE gratuito. Un semplice progetto di Visual Studio [soluzione](/it/programmazione/sln/) creato con il linguaggio VB può comprendere uno o più di questi file. I file contrassegnati per l'inclusione nella compilazione sono elencati nel file [CSPROJ](/it/programming/csproj/) che fa parte del progetto e indica al compilatore di utilizzare i file contrassegnati.

## Formato file VB - Ulteriori informazioni

I file VB sono formati di file basati su testo che possono essere aperti in qualsiasi editor di testo per la modifica. Tuttavia, quando viene aperto in un IDE supportato con un'evidenziazione della sintassi adeguata, il codice è facile da leggere e organizzare. Un semplice file VB contiene:

* Dichiarazione degli spazi dei nomi - Per fare riferimento a una particolare funzionalità definita da quello specifico spazio dei nomi
* Dichiarazione di variabili - Per dichiarare variabili a livello di classe per l'implementazione particolare
* Dichiarazione dei metodi - Per dichiarare la dichiarazione dei metodi per la particolare funzionalità

## Esempio di formato file VB

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



