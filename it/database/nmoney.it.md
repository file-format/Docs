{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Informazioni sul formato file NMONEY e sulle API che possono creare e aprire file NMONEY.",
  "title" :"File NMONEY - Formato file conto Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Cos'è un file NMONEY?

Un file NMONEY è un file di database di archiviazione di dati finanziari che contiene un track record di transazioni finanziarie. È stato sviluppato da Nickvision ed è stato utilizzato nel software Nickvision Denaro, un'applicazione software finanziaria personale. I dati archiviati all'interno di un file NOMONEY includono informazioni sulle transazioni di credito e debito su un conto.

I file NOMONEY possono essere aperti con l'applicazione [Github](https://github.com/NickvisionApps/Denaro).

## Informazioni su Denaro Software

Denaro è stato inizialmente sviluppato da [Nickvision](https://nickvision.org/) come prodotto che è stato successivamente convertito in un'app software open source ospitata su [Github](https://github.com/NickvisionApps/Denaro) . Da allora l'app è stata modificata e aggiornata solo su Github. L'app è sviluppata in C# nell'interfaccia utente di Windows con Windows App SDK (WinUI 3 al momento).

### Funzionalità offerte da Denaro

* Gestisci più account contemporaneamente con la sua interfaccia a schede più popolare e familiare
* Filtra le transazioni per tipo, gruppo o data
* Ripeti transazioni come le fatture che si verificano ogni mese
* Trasferisci denaro da un conto all'altro
* Esporta i dati da un conto come file CSV e importa un file CSV, OFX o QIF per aggiungere transazioni a un conto

## Formato file Denaro: ulteriori informazioni

I file Denaro vengono salvati su disco in formato file binario. I dati finanziari vengono archiviati come file di database nel formato file **.SQLITE3**. SQLITE è un file di database SQL leggero creato con il software SQLite. Fornisce un motore di database autonomo in grado di fornire un database completo e altamente affidabile. I file di database SQLite possono essere utilizzati per condividere contenuti avanzati tra sistemi semplicemente scambiando questi file sulla rete. Esistono collegamenti SQLite per linguaggi di programmazione come C, [C#](/it/programming/cs/), [C++](/it/programming/cpp/), [Java](/it/programming/java/), [PHP](/it/programming/php/) e molti altri.

## Riferimenti

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

