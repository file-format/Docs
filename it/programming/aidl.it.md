{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File AIDL - File del linguaggio di definizione dell'interfaccia Android",
  "description":"Scopri cos'è il formato di file AIDL con esempi e API che possono creare e aprire file AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Che cos'è un file AIDL?

Un file AIDL (Android Interface Definition Language) consente agli sviluppatori Android di stabilire la comunicazione tra diverse app. Sulla base dell'interfaccia di programmazione, sia il client che il servizio concordano di comunicare utilizzando la comunicazione interprocesso (IPC). Il file AIDL contiene il codice sorgente [Java](/it/programming/java/) per definire queste interfacce e i contratti per la comunicazione tra le app.

Puoi aprire file AIDL con Google Android Studio o qualsiasi editor di testo come Microsoft Notepad e Notepad++.

## Formato file AIDL - Ulteriori informazioni

Gli AIDL sono file di testo che contengono le interfacce per la comunicazione tra le app. Il sistema operativo Android non consente a un processo di accedere alla memoria di un altro processo. Questo porta i processi a dividere i loro oggetti in primitive per comprendere il sistema operativo sottostante e stabilire il processo delle strutture di comunicazione per lo sviluppatore.

### Quali tipi di dati sono supportati da AIDL?

AIDL supporta i seguenti tipi di dati per impostazione predefinita.

* Tutti i tipi primitivi nel linguaggio di programmazione Java (come int, long, char, boolean e così via)
* Corda
* CharSequence
* Elenco
* Carta geografica

## Esempio di file AIDL

Di seguito è riportato un esempio di file AIDL.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Riferimenti

* [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

