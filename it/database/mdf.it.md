{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file MDF e le API che possono creare e aprire file MDF.",
  "title" :"Formato file MDF - File di database principale di SQL Server",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Che cos'è un file MDF?

Un file con estensione .mdf è un file di database principale utilizzato da [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) per archiviare i dati dell'utente. È di primaria importanza poiché tutti i dati sono archiviati in questo file. Il file MDF memorizza i dati degli utenti nei database relazionali in colonne, righe, campi, indici, viste e tabelle del modulo. SQL Server consente di impostare le impostazioni di aumento e riduzione automatica per avere un impatto positivo sulle prestazioni del database. I file MDF possono essere caricati e allegati a un database utilizzando Microsoft SQL Server. I file MDF hanno il tipo mime Application/octet-stream.

## Formato file MDF

L'unità fondamentale di archiviazione dei dati in SQL Server è una pagina. Una pagina di archiviazione assegnata al database è suddivisa in pagine logiche numerate da 0 a n. Una singola pagina inizia con un'intestazione di 96 byte che comprende ID pagina, tipo di struttura a cui appartiene la pagina, numero di record nella pagina e puntatori alle pagine precedenti e successive.

### Struttura del file

Un file MDF ha la seguente struttura di dati.

* Pagina 0: intestazione
* Pagina 1: Primo PFS
* Pagina 2: Prima GAM
* Pagina 3: Primo SGAM
* Pagina 4: inutilizzato
* Pagina 5: inutilizzato
* Pagina 6: Primo DCM
* Pagina 7: Primo BCM

#### Intestazione del file

La pagina numero 0 di tutti i file contiene un'intestazione che memorizza i metadati sul file.

#### Spazio libero sulla pagina (PFS)
PFS identifica lo stato di allocazione e determina la quantità di spazio libero.

* Bit 1: indica se la pagina è allocata o meno.
* Bit 2: indica se la pagina è da un'estensione mista.
* Bit 3: indica che questa pagina è una pagina IAM.
* Bit 4: indica che questa pagina contiene record fantasma
* Bit da 5 a 7: un valore combinato di tre bit, che indica la pienezza della pagina come segue:
* 0: la pagina è vuota
* 1: la pagina è piena dall'1 al 50%.
* 2: La pagina è piena per il 51–80%.
* 3: la pagina è piena per l'81–95%.
* 4: la pagina è piena al 96–100%.

## Riferimenti

* [File di database e filegroup](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Database Stacca e collega - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [Analisi dell'anatomia del file di dati di SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

