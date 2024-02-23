{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Informazioni sul formato file ABCDDB e sulle API in grado di creare e aprire file ABCDDB.",
  "title" : "Formato file ABCDDB: file del database dell'elenco dei contatti della rubrica Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-it",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Cos'è un file ABCDDB?

Il file con estensione **.ABCDDB** sta per Apple Address Book Contact List Database. Appartiene all'applicazione **Rubrica**, comunemente nota anche come **Contatti**. È un'applicazione integrata e inclusa nei sistemi operativi iOS e macOS. L'applicazione Contatti consente agli utenti di salvare e organizzare le informazioni relative ai propri contatti, inclusi individui, aziende e organizzazioni. Questa app consente agli utenti di tenere traccia di dettagli come nomi, indirizzi, numeri di telefono e indirizzi e-mail, nonché di classificare i propri contatti in gruppi.

## Relazione con SQLite e percorso tipico

La rubrica di Apple (nota anche come contatti) memorizza le informazioni di contatto come vCard nella cartella dei metadati. **Il file _ABCDDB_ è in realtà _SQLite 3 datafile_**.

SQLite è un popolare sistema di gestione di database progettato per essere leggero e autonomo. Viene utilizzato in molti tipi diversi di software e dispositivi. SQLite è un tipo di RDBMS, il che significa che memorizza i dati in tabelle correlate tra loro tramite chiavi. Può gestire una vasta gamma di tipi di dati, inclusi numeri interi, numeri a virgola mobile, stringhe e dati binari. Inoltre, SQLite supporta le transazioni, che consentono agli utenti di eseguire più operazioni sul database insieme come una singola unità di lavoro.

Il file con estensione ABCDDB viene generalmente archiviato qui

`~/Libreria/Supporto applicazioni/Rubrica/Rubrica-v22.abcddb`

## Correzione del database dei contatti corrotto

Per favore, esegui prima il backup prima di tentare di farlo. Quindi vai a

~/Libreria/Supporto applicazioni/Rubrica.

In quella directory troverai tre file incluso quello con estensione .abcddb

- rubrica-v22.abcddb.
- rubrica-v22.abcddb-wal.
- rubrica-v22.abcddb-shm.

Elimina tutti questi file e riapri i Contatti ricomincerà a funzionare.

## Ripristina il database della rubrica dal backup

Supponiamo che i contatti del database AddressBook siano archiviati in `addressbook-v22.abcddb`

- Per prima cosa esegui il backup dei dati della tua rubrica e chiudi tutte le applicazioni.
- Sposta il file del database nella sottodirectory ~/Libreria/Supporto applicazioni/Rubrica.
- Avvia **Rubrica.app**.

## Esporta i dati del file ABCDDB in Microsoft Access

Poiché il file è un file di dati SQLite 3, è possibile esportare i dati all'interno del file abcddb in Microsoft Access utilizzando il connettore ODBC.

Il connettore ODBC SQLite è una libreria software e un driver che consente alle applicazioni che supportano l'interfaccia ODBC di connettersi a un database SQLite. Include una libreria che definisce l'interfaccia ODBC e un driver che traduce questa interfaccia in chiamate all'API SQLite. Per utilizzare il connettore ODBC SQLite, è necessario prima installarlo e quindi configurare un'origine dati ODBC sul computer. Dopo aver completato questi passaggi, qualsiasi applicazione dotata di supporto ODBC sarà in grado di connettersi all'origine dati e recuperare i dati dal database SQLite.

## Riferimenti
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Database dei contatti per Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Come posso aprire o esportare un file abcddb in Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

