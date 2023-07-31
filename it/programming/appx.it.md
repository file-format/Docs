{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Che cos'è un file APPX?",
  "description":"Scopri il formato di file APPX e le API che possono creare e aprire file APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Che cos'è un file APPX?

Un file APPX è un formato di file di pacchetto distribuibile utilizzato per la distribuzione e l'installazione di un'applicazione. È stato introdotto con Windows 8 per essere pubblicato su Microsoft Windows Store. Contiene tutti i file necessari per installare un'applicazione Windows. Questi includono metadati, file e informazioni sulle credenziali. Un formato di file di confezionamento più moderno è MSIX, attualmente più comunemente utilizzato rispetto ad APPX.

## Formato file APPX - Ulteriori informazioni

I file APPX vengono salvati come file compressi nel formato file [ZIP](/it/compression/zip/). Ciò rende l'intero pacchetto un file di archivio con dimensioni del file ridotte che è facile da caricare su Microsoft Store.

## Come visualizzare i file in un file APPX?

Per visualizzare i contenuti oi file all'interno di un file APPX, è necessario seguire i seguenti passaggi.

1. Poiché i file APPX sono archiviati come file ZIP compressi, rinominare il file con estensione .zip
1. Utilizzare qualsiasi strumento di decompressione come 7-Zip, WinZip o WinRAR per estrarre i file contenuti nel file APPX

## Come creare un file APPX?

Esistono due metodi che possono essere utilizzati per creare file APPX.

1. Utilizzo di MakeApp.exe - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) viene utilizzato per creare entrambi pacchetti di app (.msix o .appx) e file di bundle di pacchetti di app .msixbundle o .appxbundle). Inoltre, può estrarre file da un pacchetto di app. MakeApp.exe è disponibile con Windows 10 SDK e può essere utilizzato dal prompt dei comandi.
1. Utilizzo di Microsoft Visual Studio - Gli sviluppatori di solito [creano file APPX](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) utilizzando Microsoft Visual Studio. Una volta completato lo sviluppo dell'applicazione e l'app è pronta per essere pubblicata, è possibile creare il file del pacchetto APPX pubblicandolo da Visual Studio.

## Riferimenti

* [Crea un pacchetto MSIX o un bundle con MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Crea file APPX utilizzando Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

