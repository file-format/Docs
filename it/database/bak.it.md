{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "estensione", "file", "formato file", "Tipo file BAK", "Estensione file BAK", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file BAK e le API che possono creare e aprire file BAK.",
  "title" :"Formato file BAK - File di backup del database",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Che cos'è un file BAK?

Un file con estensione .bak è solitamente un file di backup utilizzato da diversi strumenti software per archiviare backup di dati. Dal punto di vista del database, un file BAK viene utilizzato da Microsoft SQL Server per archiviare il contenuto di un database. Tutti i dati e i file associati al database vengono archiviati in questo formato di file per essere recuperati nel caso in cui il database possa essere danneggiato o non valido per qualsiasi motivo. I file di backup possono essere archiviati e indicizzati su altri server per motivi di sicurezza. Diverse applicazioni possono creare file BAK come SQL Server Management Studio, Transact-SQL e Windows PowerShell.

## Formato file BAK

I dettagli interni di un file BAK non sono noti, ma è opinione diffusa che sia basato sul Microsoft Tape Format (MTF). Le specifiche MTF sono disponibili e possono essere consultate per comprendere la struttura del file. Il documento fornisce dettagli sull'archiviazione MTF per chiunque abbia una conoscenza generale delle operazioni di gestione dell'archiviazione, delle unità nastro e dei file system.

### Set di dati

Un set di dati è una raccolta di oggetti scritti su un supporto di memorizzazione (nastro, disco ottico, ecc.) durante il backup o il ripristino dei dati. I set di dati comprendono più supporti in caso di grandi volumi di dati.

### Elementi Fondamentali di MTF

Un file MTF è costituito da alcuni elementi fondamentali che ne costituiscono gli elementi costitutivi. Questi elementi sono:

#### Blocchi descrittore

I blocchi descrittore (DBLK) vengono utilizzati per il controllo del formato e costituiscono le basi primarie di un file MTF. Un singolo file MTF definisce più DBLK per ogni ruolo univoco. Ogni DBLK è un blocco di dati di lunghezza variabile suddiviso nelle seguenti quattro parti:

* `Common Block Header` - Struttura a lunghezza fissa comune a tutti i DBLK. Questa è l'unica intestazione di blocco richiesta.
* `Informazioni sul tipo DBLK` - Blocco a lunghezza fissa specifico per il tipo di DBLK in fase di definizione
* `Dati del sistema operativo` - Dati specifici definiti in base al tipo di DBLK e ai sistemi operativi
* `Informazioni DBLK` - Informazioni specifiche DBLK a lunghezza variabile che non possono essere salvate con le informazioni DBLK a lunghezza fissa.

 {{< figure src="../bak.png" alt="Formato file di backup Microsoft SQL" >}}

#### Flusso di dati

I flussi di dati in un file MTF vengono utilizzati per l'incapsulamento e l'allineamento dei dati. Comprende un'intestazione di flusso, seguita dai dati di flusso. Un'intestazione di flusso può incapsulare solo un singolo tipo di dati di flusso.

{{< figure src="../bak_datastream.png" alt="Formato file di backup Microsoft SQL" >}}

#### Marchi di file

Un contrassegno di file viene utilizzato per la separazione logica e l'accesso rapido all'interno di un supporto. I contrassegni di file vengono emulati dal driver del dispositivo o mediante l'uso del blocco Soft Filemark Descriptor nel caso in cui il dispositivo utilizzato non fornisca contrassegni di file.

## Riferimenti ##

* [[MS-BCP]: Formato copia in blocco](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

