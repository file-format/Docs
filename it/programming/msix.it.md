{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Che cos'è un file MSIX?",
  "description":"Ulteriori informazioni sul file MSIX e sulle API che possono creare e aprire file MSIX.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Che cos'è un file MSIX?

Un file MSIX è un formato di pacchetto di app di Windows utilizzato per creare e distribuire applicazioni in Windows 10. Questo è il formato di file di pacchetto moderno rispetto a [APPX](/it/programming/appx/) e MSI che verranno finalmente eliminati a questo nuovo formato di file. Può essere usato per la distribuzione di app Win32, WPF e Windows Forms. I file MSIX sono affidabili e mirano all'ottimizzazione della rete e dello spazio su disco. Gli sviluppatori li usano per distribuire programmi agli utenti finali tramite Microsoft Store (precedentemente noto come Windows Store).

## Formato file MSIX - Ulteriori informazioni

I file MSIX sono [ZIP](/it/compression/zip/) compressi, con tutti i file inclusi nel file compresso. Oltre ai file relativi all'app, il file MSIX contiene file di configurazione [.xml](/it/web/xml/) che contengono informazioni relative all'installazione dell'app.

## Cosa c'è all'interno di un pacchetto MSIX?

Un pacchetto MSIX è costituito dai seguenti file.

* `AppxBlockMap.xml` - Conosciuto come il file di mappa dei blocchi del pacchetto, è un documento XML che contiene un elenco di file dell'app con indici e hash crittografici per ogni blocco di dati archiviato nel pacchetto.
* `AppxManifest.xml`: un documento XML che contiene le informazioni necessarie per la distribuzione, la visualizzazione e l'aggiornamento di un'app MSIX. Queste informazioni includono l'identità del pacchetto, le dipendenze del pacchetto, le funzionalità richieste, gli elementi visivi e i punti di estendibilità.
* `AppxSignature.p7x` - Un file che viene generato quando il pacchetto viene firmato. Tutti i pacchetti MSIX devono essere firmati prima dell'installazione. Con AppxBlockmap.xml, la piattaforma è in grado di installare il pacchetto ed essere convalidata.

## Riferimenti

* [Panoramica MSIX](https://learn.microsoft.com/en-us/windows/msix/overview)
* [Crea file APPX utilizzando Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

