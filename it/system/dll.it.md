{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "estensione", "file", "format", "sistema", "Dynamic Link Library", "impostazioni", "programmi", "computer", "applicazione" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Libreria di collegamento dinamico",
  "description":"Scopri il formato di file DLL e le API che possono creare e aprire file DLL.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Che cos'è un file DLL? ##

Un file DLL o Dynamic Link Library è un tipo di file eseguibile. È uno dei file di estensione più comunemente trovati sul tuo dispositivo e di solito è archiviato nella cartella System32 su Windows. Il file di estensione DLL è stato sviluppato da Microsoft ed è comunemente utilizzato da loro. Ha un'elevata popolarità tra gli utenti. La DLL funziona come uno scaffale che contiene i *driver/procedure/funzioni/proprietà* progettati e applicati per un programma/applicazione dal server Windows. Un singolo file DLL può anche essere condiviso tra vari programmi Windows. Questi file di estensione sono vitali per il corretto funzionamento dei programmi Windows sul dispositivo in quanto sono responsabili dell'abilitazione e dell'esecuzione di varie funzioni del programma come la scrittura e la lettura di file, la connessione con altri dispositivi esterni alla configurazione.
Questi file tuttavia possono essere aperti solo su un dispositivo che supporta qualsiasi versione di Windows (Windows 7/Windows 10/ecc.) e quindi non possono essere aperti direttamente su un dispositivo che supporta Mac OS. (Se desideri aprire un file DLL su Mac OS, varie applicazioni esterne possono aiutarti ad aprirlo.)


## Formato file DLL ##

Il file DLL è stato sviluppato da Microsoft e ha l'estensione ".dll" che rappresenta il tipo. È stato parte integrante del server Windows 1.0 e oltre. È un tipo di file binario e supportato da tutte le versioni di Microsoft Windows. Questo tipo di file è stato creato come mezzo per creare un sistema di librerie condivise all'interno dei programmi Windows, per consentire modifiche o modifiche separate e indipendenti nelle librerie di programmi senza la necessità di ricollegare i programmi.


## Esempio DLL ##

Di seguito è possibile trovare un codice di esempio per un punto di ingresso DLL:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## Riferimento ##

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
