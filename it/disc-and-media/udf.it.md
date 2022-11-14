{
  "date" : "2021-08-17",
  "keywords" :[ "file udf", "formato file udf", "cos'è un file udf", "file", "esempio udf", "estensione file udf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri il formato di file UDF e le API che possono creare e aprire file UDF.",
  "title" :"UDF - File formato disco universale",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Che cos'è un file UDF?
Il file con estensione .udf è un formato di imaging del disco generalmente utilizzato per il salvataggio di file su supporto ottico; può essere utilizzato per masterizzare DVD, CD e altri supporti ottici; memorizza una raccolta di file utilizzando la struttura di directory specificata nello standard UDF; consente di eliminare e modificare i file sul disco di destinazione anche dopo che sono stati scritti. L'Optical Storage Technology Association ha impostato il file system UDF come standard per formare un file system comune per tutti i supporti ottici, come i supporti ottici riscrivibili e i supporti di sola lettura.

## Formato file UDF
Il formato di file UDF è un file system aperto e indipendente dal fornitore per l'archiviazione dei dati del computer per un'ampia gamma di supporti. È stato usato comunemente per DVD e formati di dischi ottici più recenti. Di solito, il software gestisce un file system UDF in un processo batch e lo scrive su un supporto ottico in un unico passaggio. Tuttavia, quando scrive pacchetti su supporti riscrivibili, l'UDF consente di creare, eliminare e modificare file su disco in modo simile a un filesystem generico su supporti rimovibili come unità flash o floppy disk.
### Specifiche UDF
Lo standard UDF definisce le seguenti tre variazioni del file system:

- **Plain Build**: questo è il formato originale supportato in tutte le revisioni UDF. È stato introdotto nella prima versione dello standard, questo formato può essere utilizzato su qualsiasi tipo di disco che consente l'accesso in lettura o scrittura casuale, come DVD+RW, dischi rigidi e supporti DVD-RAM.
- **Build IVA**: utilizzato specificamente per la scrittura su supporti scrivibili una sola volta. L'IVA è una struttura aggiuntiva sul disco che consente la scrittura di pacchetti; ovvero, rimappare i blocchi fisici quando i file o altri dati sul disco vengono modificati o eliminati. Per i supporti write-once, l'intero disco viene virtualizzato, rendendo la natura write-once trasparente per l'utente; il disco può essere trattato allo stesso modo di un disco riscrivibile.
- **Build risparmiato (RW)**: utilizzato specificamente per la scrittura su supporti riscrivibili. Aggiunge una tabella di riserva aggiuntiva per gestire i guasti che alla fine si verificheranno su parti del disco che sono state riscritte più volte. Questa tabella salva la traccia dei settori usurati e li rimappa a quelli funzionanti. La gestione dei difetti di UDF non si applica ai sistemi che implementano già un'altra forma di gestione dei difetti, come Mount Rainier (MRW) per i dischi ottici o un controller del disco per un disco rigido.
 




## Riferimenti


* [Formato di imaging di Windows - di Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


