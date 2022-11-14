{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - File di codice sorgente Matlab",
  "description":"Scopri il file di codice sorgente Matlab .m e le API che possono creare e aprire file MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - File di codice sorgente Matlab

## Che cos'è un file M (Matlab)?

Un file con estensione .m è un file di codice sorgente utilizzato da Matlab, una piattaforma di programmazione e calcolo numerico utilizzata per l'analisi, lo sviluppo di algoritmi e la modellazione di simulazione. Come altri formati di file di programmazione, un file M contiene codice sorgente che esegue i comandi Matlab per tracciare grafici, eseguire simulazioni e altre operazioni matematiche. Una singola simulazione Matlab può estendersi su più file .m di questo tipo che possono classificare l'applicazione in script, classi, funzioni o dichiarazioni. I file Matlab M possono essere aperti con qualsiasi editor di testo.

## Formato file Matlab M - Ulteriori informazioni

I file Matlab .m sono file di testo che contengono codice di programmazione nel linguaggio di programmazione Matlab. Questi possono essere aperti e modificati in qualsiasi editor di testo e salvati per essere eseguiti nel software Matlab. Matlab stesso contiene un Live Editor che viene utilizzato per creare script che è una combinazione di codice, output e testo formattato.

### File di funzioni Matlab

Come altri linguaggi di programmazione, puoi creare un file .m che contiene solo la definizione di una funzione che esegue solo un compito specifico. Tali file vengono anche salvati con estensione .m e implementano le funzionalità relative solo a quella funzione.

### Esempio di file .M

Quello che segue è un esempio di file di funzione Matlab che calcola il tempo impiegato per un oggetto caduto dall'altezza h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Per chiamare questa funzione dall'editor Matlab o da un altro file .m, è possibile utilizzare il codice seguente.
```C++
TimeToGround(100)
```

## Riferimenti

* [Matlab - Formati di file supportati](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Utilizzo di Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - File di implementazione di Objective-C

## Che cos'è un file M (Obiettivo-C)?

Un file M viene anche definito file di implementazione che contiene il codice sorgente di una classe scritta in linguaggio Objective-C, un linguaggio di programmazione utilizzato per scrivere applicazioni software per OS X e iOS. Objective-C è il principale linguaggio di programmazione utilizzato dalle principali API di Apple, Cocoa e Cocoa Touch, per queste piattaforme. Una singola applicazione software sviluppata in questo linguaggio può contenere più file .m, contenenti l'implementazione delle classi di programma. Questi possono essere aperti utilizzando Apple XCode, jEdit e altri comuni editor di testo.

## Formato file Objective-CM - Ulteriori informazioni

I file M sono scritti in formato testo normale utilizzando la sintassi di programmazione di Objective-C. Ogni metodo di una classe deve essere definito con tutto il codice necessario in questi file di implementazione. Questi file M di implementazione possono importare uno o più file di intestazione .h secondo i requisiti. L'istruzione import indica al compilatore dove trovare il file di intestazione che appartiene a questo file di implementazione. La dichiarazione di importazione è scritta come segue.

```C++
#import "network.h"
```

Ogni implementazione di file M inizia quindi con la direttiva `@implementation`, seguita dal nome del file di classe di implementazione. Segue quindi l'implementazione di tutti i metodi dichiarati nel file di intestazione.

### M Esempio di formato file

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Riferimenti
* [Informazioni sull'obiettivo C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Guida all'oggetto C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

