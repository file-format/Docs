{
  "date" : "2021-08-24",
  "keywords" :[ "file trc", "formato file trc", "cos'è un file trc", "file", "esempio trc", "estensione file trc", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file TRC e le API che possono creare e aprire file TRC.",
  "title" :"TRC - File di traccia di SQL Server",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Che cos'è un file TRC?
Un file con estensione .trc contiene i risultati della traccia dell'attività di un database del server Miscrosoft SQL. Questi file vengono creati da un software SQL Server Profiler; solitamente confezionato con il software Microsoft SQL Server. Gli amministratori del database possono analizzare una sequenza di istruzioni del database e possono rivedere il registro di traccia se si sospetta qualche tipo di errore o avviso. Questi file si trovano in genere nella tipica cartella LOG di MSSQL all'interno della directory Programmi su un sistema operativo Windows.

## Formato file TRC
Il formato di file TRC viene utilizzato da SQL Server Profiler per generare automaticamente una nuova traccia delle istruzioni eseguite di recente da MS SQL Server. SQL Server Profiler utilizza il modello predefinito per qualsiasi nuova traccia. Tuttavia, il software include diversi modelli predefiniti per il monitoraggio di determinati tipi di eventi. Inoltre, SQL Server Profiler può essere utilizzato per creare modelli che definiscono le classi di eventi e le colonne di dati da includere nelle tracce.

### Modelli predefiniti
Di seguito è riportato l'elenco di alcuni modelli predefiniti inclusi in SQL Server Profiler:
- **SP_Counts**: acquisisce il comportamento di esecuzione della procedura memorizzata nel tempo.
- **Standard**: punto di partenza generico per la creazione di una traccia.
- **TSQL**: acquisisce tutte le istruzioni Transact-SQL inviate a SQL Server dai client e l'ora emessa.
- **TSQL_Duration**: acquisisce tutte le istruzioni Transact-SQL inviate a SQL Server dai client, il loro tempo di esecuzione e le raggruppa per durata.
- **TSQL_Grouped**: da utilizzare per analizzare le query da un particolare client o utente.
- **TSQL_Locks**: da utilizzare per risolvere i deadlock, il timeout di blocco e gli eventi di escalation dei blocchi.
- **TSQL_Replay**: utilizzare per eseguire l'ottimizzazione iterativa, ad esempio test di benchmark.
- **TSQL_SPs**: utilizzare per analizzare i passaggi dei componenti delle procedure archiviate.
- **Ottimizzazione**: utilizzare per produrre l'output di traccia che Ottimizzazione guidata motore di database può utilizzare come carico di lavoro per ottimizzare i database.
### Correla una traccia con i dati del registro delle prestazioni di Windows
SQL Server Profiler può essere utilizzato per aprire un registro delle prestazioni di Microsoft Windows, per scegliere i contatori da correlare con una traccia e visualizzare i contatori delle prestazioni selezionati insieme alla traccia nella GUI di MS SQL Server Profiler. Per indicare i dati del registro delle prestazioni correlati all'evento di traccia selezionato, una barra rossa verticale nel riquadro della finestra dei dati di System Monitor di SQL Server Profiler.


## Riferimenti ##

* [SQL Server Profiler](https://docs.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

