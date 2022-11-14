{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file MDB e le API che possono creare e aprire file MDB.",
  "title" :"Formato file MDB - Un file di database di Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Che cos'è un file MDB?

Un file con estensione .mdb è un file di database di Microsoft Access che è un sistema di gestione dei database relazionali (RDBMS). Memorizza i dati in tabelle di database che sono collegate tra loro tramite chiavi primarie ed esterne. Il file MDB contiene la struttura completa delle tabelle del database, le query, le procedure memorizzate. MDB è il formato di file predefinito per Microsoft Access 2003. Le versioni laterali di Microsoft Access utilizzano i formati di file [ACCDB](/it/database/accdb/), che è il formato di file più recente fino ad oggi. I file MDB possono essere aperti con applicazioni come Microsoft Access, MDB Viewer, MDBOpener e possono essere convertiti in ACCDB, [CSV](/it/spreadsheet/csv/), formati Excel, ecc.

## Formato file MDB

Sono disponibili specifiche pubbliche per il formato MDB e rimane il formato di file proprietario di Microsoft. Microsoft, tuttavia, fornisce l'accesso alla connettività al file MDB utilizzando lo standard ODBC (Open Database Connectivity) e Visual Basic, Applications Edition (VBA). La guida non ufficiale dell'MDB fornisce una breve descrizione informale del formato MDB basata sul reverse engineering e può essere consultata per conoscere le specifiche.

### Pagine

Secondo la guida MDB non ufficiale, un file MDB è costituito da pagine di dimensioni fisse (2048 byte per Jeb DB3 e 4096 byte per Jet DB 4). Il primo byte indica il tipo di pagina. Di seguito sono riportati i tipi di pagina chiave:

`Prima pagina:` Contiene informazioni sull'intestazione del database che includono anche l'identificazione della versione Jet DB con cui il file è compatibile. Inoltre, include anche informazioni sulla sicurezza dei file e una mappa dell'utilizzo della pagina.

`Pagina di definizione della tabella:` Una pagina di definizione della tabella specifica colonne, tipi di dati, indice e altre informazioni. Utilizza pagine aggiuntive se necessario e include una mappa di pagine che contiene i dati di riga per questa tabella.

`Pagine di dati:` Le pagine di dati sono i contenitori di dati effettivi in cui i dati sono archiviati per righe. Utilizza pagine sussidiarie per memorizzare valori di dati lunghi.

Un singolo database di Microsoft Access può comprendere più file che consentono di superare i limiti di dimensione di file e tabelle. Ciò facilita l'inserimento di moduli e codice in un file MDB front-end sul desktop dell'utente e dati in un altro file MDB di back-end su server connessi alla rete.

## Riferimenti ##

* [Specifiche di accesso](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [La guida non ufficiale di MDB](http://jabakobob.net/mdb/)

