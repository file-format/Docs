{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file LDF e le API che possono creare e aprire file LDF.",
  "title" :"LDF - Formato file database master di SQL Server",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Che cos'è un file LDF?

Un file con estensione .ldf è un file di registro gestito da Microsoft SQL Server che è un sistema di gestione di database relazionali (RDBMS). Tutte le transazioni eseguite sui file di database primari ([MDF](/it/database/mdf/))(come inserimento, aggiornamento, cancellazione) vengono registrate nel file LDF. I file LDF sono componenti critici di qualsiasi database. In caso di errore del sistema, il file di registro viene utilizzato per ripristinare uno stato coerente del database. Il file di registro delle transazioni può aumentare di dimensioni se le transazioni non sono state completamente salvate. I file LDF possono essere aperti con l'applicazione software Microsoft SQL Server.

## Operazioni registrate nel file LDF

Un file di registro SQL registra le seguenti operazioni:

* L'inizio e la fine di ogni transazione.

* Ogni modifica dei dati (inserimento, aggiornamento o eliminazione). Ciò include anche le modifiche apportate da procedure memorizzate di sistema o istruzioni DDL (Data Definition Language) a qualsiasi tabella, comprese le tabelle di sistema.

* Ogni estensione e allocazione o deallocazione di pagine.

* Creazione o eliminazione di una tabella o indice.

## Formato file LDF

Il file LDF è costituito da record di transazione di SQL Server organizzati come stringa di record di registro. Ogni record di registro ha un numero di sequenza di registro (LSN) che è maggiore dell'LSN del record precedente. Le stringhe sono concatenate una dopo l'altra nel file. A causa dei moderni computer ad alta velocità, è possibile inserire record in cui l'LSN2 esiste nel file di registro prima di LSN1. Poiché le operazioni sono registrate in un seriale, la modifica descritta da LSN2 è stata eseguita dopo il record di log LSN1. I record per una determinata transazione sono collegati all'indietro utilizzando i puntatori utilizzati e velocizzano il rollback della transazione.
 

## Riferimenti

* [File di database e filegroup](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Guida all'architettura e alla gestione del registro delle transazioni](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql- server-ver15)

