{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file FMPSL e le API che possono creare e aprire file FMPSL.",
  "title" :"Formato file FMPSL - File di collegamento snapshot di FileMaker Pro 12",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Che cos'è un file FMPSL?

Un file FMPSL è un file di istantanea del database creato con FileMaker Pro 12. Memorizza i risultati della query dal database insieme ad altre informazioni come il layout visivo e le informazioni visibili. Il file FMPSL può essere utilizzato per ripristinare tutti questi dati in un'altra istanza del database FileMaker Pro. Questo formato di file è stato introdotto con il lancio di FileMaker Pro v 12. Prima di questa versione, i collegamenti alle istantanee sono stati introdotti come formato di file FPSL in FileMaker Pro v 11. I file FMPSL possono essere aperti con il software FileMaker Pro Advanced. Altri formati di file supportati da FileMaker Pro includono [FP5](/it/database/fp5/), [FP7](/it/database/fp7/) e [FMP12](/it/database/fmp12/).

## Formato file FMPSL

I dettagli del formato di file interno dei file FMPSL non sono disponibili pubblicamente per riferimento dello sviluppatore.

### Come salvare i record come file FMPSL?

I dati dal database FileMaker Pro possono essere salvati come file di collegamento istantanea utilizzando i seguenti passaggi.

1. Cerca i record dal database che devono essere salvati come file di collegamento snapshot.
1. Utilizzando l'opzione Invia record come collegamento snapshot dal menu, salvare il file immettendo un nome file.
1. Utilizzare i record esplorati per salvare l'intero set di record trovato.

Il file snapshot generato verrà salvato su disco con il nome specificato.

## Riferimenti

* [Convertire versioni precedenti dei formati file FileMaker Pro nel formato file FMP12](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Salva i record come file di collegamento snapshot](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

