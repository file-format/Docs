{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "file sdf", "cos'è un file sdf", "come aprire un file sdf", "estensione", "file", "formato file sdf", "Tipo file database", "Formato file database ", "File di database" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file SDF e le API che possono creare e aprire file SDF.",
  "title" :"SDF - File di database di SQL Server Compact",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Che cos'è un file SDF?
Un file con estensione .sdf contiene il database Microsoft SQL Server Compact (SQL CE), noto anche come database relazionale compatto; prodotto da Microsoft per le applicazioni realizzate per dispositivi mobili e desktop. Supporta entrambi i sistemi operativi a 32 e 64 bit e il contenuto completo del database è incluso in un unico file SDF e può occupare più di 4 GB di spazio su disco. Per motivi di sicurezza, un file .sdf può essere crittografato con crittografia a 128 bit. Il runtime di SQL CE regola l'accesso multiutente parallelo al file .sdf. Il file SDF può essere copiato tramite **QuickOnce** o semplicemente può essere copiato nella destinazione per l'implementazione del sistema.

## Formato file SDF
Un file SDF contiene un database che di solito viene chiamato database relazionale compatto. Un file SDF contiene tutte le informazioni relative al database e SQL Server Compact è un motore di database leggero e gratuito che viene utilizzato per gestire i file .sdf. La dimensione del file .sdf non deve superare il limite di 4 GB di dimensione. I file SDF non memorizzano le informazioni su stored procedure, trigger o viste. Le applicazioni che utilizzano un database SQL CE non devono specificare il percorso di un file SDF nella stringa di connessione ADO.NET, ma possono essere citate come |DataDirectory|\database_name.sdf, definendo la directory dei dati da definire nel manifesto dell'assembly per l'applicazione
La convenzione di denominazione .sdf è facoltativa e qualsiasi estensione può essere utilizzata per salvare il file. L'impostazione di una password per il file di database è un passaggio facoltativo. Per comprimere o riparare il database, il file deve essere salvato con l'opzione del **database compattato/riparato**.

## Riferimenti

* [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Utilizzo di SQL Server Compact per applicazioni Web ASP.NET](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


