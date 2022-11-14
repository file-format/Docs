{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "file", "estensione", "formato file", "C++", "linguaggio di programmazione" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - File di codice sorgente C++",
  "description":"Scopri il formato di file CPP e le API che possono creare e aprire file CPP.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file C++?

I file con estensione CPP sono file di codice sorgente per applicazioni scritte nel linguaggio di programmazione C++. Un singolo progetto C++ può contenere più di un file CPP come codice sorgente dell'applicazione. Tale progetto è costituito da diversi tipi di file, di cui i file CPP sono noti come file di implementazione in quanto contengono tutte le definizioni dei metodi dichiarati nel file di intestazione (.h). Il progetto C++ nel suo insieme risulta in un'applicazione eseguibile quando compilato nel suo insieme.

## Struttura del file CPP

Una struttura di file CPP è semplice rispetto ai file di intestazione. Lo scopo principale di un tale file di implementazione è dividere l'interfaccia dall'implementazione. Ciò si traduce in dichiarazioni di tutte le funzioni membro in un file di intestazione e dei relativi dettagli all'interno del file CPP. Un file di implementazione CPP può essere utilizzato come semplice file per scrivere un'applicazione o come implementazione di classe.

### Implementazione indipendente

Un file CPP quando viene utilizzato come applicazione indipendente può contenere tutte le implementazioni al suo interno senza il requisito della dichiarazione dei metodi nel file di intestazione. Tale implementazione consiste in tutti i metodi definiti nel file di implementazione in cui la voce dell'applicazione è regolata da un metodo principale che accetta l'input utente opzionale come argomenti. Può anche includere qualsiasi libreria della libreria standard C++ da utilizzare con qualsiasi metodo dichiarato nel file.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Implementazione della classe

In Object Oriented Programming (OOP), un file CPP viene utilizzato come definizione di classe. In tal caso, tutti i membri dati della classe e le funzioni membro vengono dichiarati all'interno del file di intestazione. Ciascun file di intestazione può a sua volta fare riferimento anche a metodi di libreria standard. Il file CPP di definizione della classe fa riferimento al file di intestazione in un'istruzione include all'inizio del file. Per lo più, gli sviluppatori di software includono commenti all'inizio di tale file di implementazione di classe che forniscono informazioni sul contenuto effettivo del file, i dettagli dell'autore e la data di implementazione. In questi casi, i file di implementazione dell'intestazione devono avere gli stessi nomi. Un esempio di tale file di intestazione e implementazione è il seguente.

### File di intestazione

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### File di implementazione CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Riferimenti

* [Implementazione della classe - Da Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

