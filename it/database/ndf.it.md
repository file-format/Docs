{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file MDF e le API che possono creare e aprire file NDF.",
  "title" :"Formato file NDF - File database master di SQL Server",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Che cos'è un file NDF?

Un file con estensione .ndf è un file di database secondario utilizzato da [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) per memorizzare i dati dell'utente. NDF è un file di archiviazione secondario perché il server SQL archivia i dati specificati dall'utente nel file di archiviazione primario noto come [MDF](/it/database/mdf/). Il file di dati NDF è facoltativo ed è definito dall'utente per gestire l'archiviazione dei dati nel caso in cui il file MDF primario utilizzi tutto lo spazio allocato. Di solito è archiviato su un disco separato e può diffondersi su più dispositivi di archiviazione. La presenza di file MDF è necessaria per aprire i file NDF.

## Formato file NDF

Il formato del file NDF non è diverso da [MDF](/it/database/mdf/) e utilizza le pagine come unità fondamentale di archiviazione dei dati. ogni pagina inizia con un'intestazione di 96 byte che include:

* ID pagina
* Tipo di struttura
* Numero di record nelle pagine
* Puntatori alle pagine precedenti e successive

### Struttura del file NDF

Un file MDF ha la seguente struttura di dati.

* Pagina 0: intestazione
* Pagina 1: Primo PFS
* Pagina 2: Prima GAM
* Pagina 3: Primo SGAM
* Pagina 4: inutilizzato
* Pagina 5: inutilizzato
* Pagina 6: Primo DCM
* Pagina 7: Primo BCM

#### Intestazione del file NDF

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

## Pagina del file di dati

Le pagine in un file di dati di SQL Server iniziano da zero (0) e aumentano in sequenza. Ogni file è riconosciuto da un numero ID file univoco. La coppia ID file e numero di pagina identifica in modo univoco una pagina in un database. Un esempio che mostra i numeri di pagina in un database, è come nell'immagine seguente.

{{< figure src="../ndf.png" alt="Formato file di database NDF" >}}

Questo esempio mostra i numeri di pagina in un database che ha un file di dati primario da 4 MB e un file di dati secondario da 1 MB.

## Riferimenti

* [File di database e filegroup](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
* [Database Stacca e collega - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Analisi dell'anatomia del file di dati di SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

