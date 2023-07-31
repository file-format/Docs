{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh", "che cos'è un file .hh", "come aprire un file .hh", "estensione", "file", "file .hh", "formato file .hh", " Estensione file .hh","Esempio file .HH"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - Formato file di intestazione C++",
  "description":"Scopri il formato di file HH e le API che possono creare e aprire file HH.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Che cos'è un file HH?

Un file con estensione .hh è un file di intestazione C++ che include la dichiarazione di variabili, costanti e funzioni. Queste dichiarazioni vengono utilizzate dai corrispondenti file di implementazione C++, solitamente salvati come file [.cpp](/it/programming/cpp/) che contengono l'effettiva implementazione della logica utente. I file di intestazione .hh sono referenziati nei file CPP di implementazione usando la direttiva `#include`. Puoi aggiungere il maggior numero possibile di file di intestazione al tuo progetto C++ per includere dichiarazioni a livello di progetto.

## Formato file .HH

Un file .hh è un file di testo normale che viene creato tenendo presenti le regole di definizione del file di intestazione. Le informazioni più comuni dichiarate in un file .hh includono quanto segue.

**`Variabili`** - In caso di programmazione orientata agli oggetti (OOP), un file di intestazione di classe contiene le definizioni di tutte le variabili a livello di classe accessibili attraverso i file di codice sorgente dell'implementazione
**`Dichiarazione dei metodi`** - Tutte le dichiarazioni dei metodi sono incluse nei file di intestazione .h per essere accessibili in più file di implementazione.
**`Definizioni di funzioni non in linea`** - I file di intestazione possono anche contenere definizioni di metodi non in linea.
**`Mappe dei messaggi`** - Un file di intestazione può anche contenere mappe dei messaggi in caso di implementazione del codice sorgente MFC. In tal caso, le mappe dei messaggi sono collegate all'implementazione della funzionalità che è collegata agli elementi dell'interfaccia utente come pulsante, casella di controllo, pulsanti di opzione, ecc.

## Differenza tra file .H e .HH

Apparentemente, non esiste tale differenza tra i file di intestazione .h e .hh oltre al modo consigliato di utilizzarli per i rispettivi linguaggi, ad esempio [C](/it/programmazione/c/) o C++. Denominare i file di intestazione in base a questi linguaggi consente di distinguerli in un progetto di grandi dimensioni che può essere un mix di implementazioni C e C++.

Inoltre, se le intestazioni sono separate per estensione, il tuo editor può applicare automaticamente la formattazione appropriata rispettivamente per.

Nel complesso, la differenziazione di questi due formati di file non arrecherà alcun danno, ma sarà vantaggiosa ed è incoraggiata a seguire la distinzione C e C++.

### Guardie di testata

I file di intestazione possono generare errori complessi in cui più dichiarazioni sono incluse nello stesso file a seguito dell'aggiunta di altri file di intestazione. Queste definizioni duplicate generano errori del compilatore. Questa situazione problematica può essere evitata tramite un meccanismo chiamato header guard che sono direttive di compilazione condizionale come mostrato di seguito.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Con questa intestazione, il preprocessore controlla se `ANY_UNIQUE_NAME_HERE_HPP` è già stato definito. Se l'intestazione viene inclusa ripetutamente nello stesso file, il contenuto dell'intestazione verrà ignorato.

## Riferimenti

* [File di intestazione - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Differenza tra i formati di file .h e .hh](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

