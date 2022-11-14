{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "file", "estensione", "formato file", "File macro di Microsoft Excel", "Foglio di calcolo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"La tua guida al formato di file per sapere cos'è un file XLM Macro e API in grado di creare e aprire file XLM.",
  "title" :"Cos'è un file XLM?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Che cos'è un file XLM?

XLM, per Excel Macro, è un tipo di file di foglio di calcolo utilizzato per archiviare le macro. Dal punto di vista applicativo, una Macro è un insieme di istruzioni che vengono utilizzate per automatizzare i processi. Una macro viene utilizzata per registrare i passaggi che vengono eseguiti ripetutamente per il formato file [XLS](/it/spreadsheet/xls/) e facilita l'esecuzione delle azioni eseguendo nuovamente la macro. Le macro sono programmate con Visual Basic, Applications Edition (VBA) di Microsoft dall'interno della cartella di lavoro di Excel utilizzando Visual Basic Editor e possono essere eseguite/debug direttamente da lì.

## Breve storia ##

Microsoft Excel ha supportato la programmazione delle macro sin dal suo primo lancio pubblico. Le funzionalità delle macro sono rimaste le stesse attraverso le versioni successive di Excel con estensione come da nuove funzionalità. XLM era il linguaggio macro predefinito per Excel tramite Excel 4.0. Le macro registrate in Excel 5.0 in VBA per impostazione predefinita, ma con la versione 5.0 la registrazione XLM era ancora consentita come opzione. Dopo la versione 5.0 tale opzione è stata interrotta. Tutte le versioni di Excel, incluso Excel 2010, sono in grado di eseguire una macro XLM, anche se Microsoft ne sconsiglia l'uso.

## Registrazione di una macro in XLM ##

Excel fornisce passaggi facili da usare per la registrazione di una macro. Richiede che siano installati gli strumenti per sviluppatori per poter lavorare con le macro. Una volta che una registrazione macro è in corso, registra ogni azione dell'utente da riprodurre in seguito. La registrazione macro coinvolge effettivamente tutti i passaggi che un utente esegue dopo l'inizio della registrazione. Pertanto, se si imposta il contenuto di una cella in grassetto, corsivo e si imposta la giustificazione del testo dopo l'avvio di una registrazione di macro, tutti questi comandi verranno registrati. A ciascuna macro registrata può essere assegnata anche una scorciatoia per la riproduzione rapida in un secondo momento. La registrazione di macro genera codice VBA sotto forma di macro che può essere modificata utilizzando Visual Basic Editor (VBE).

## Modello a oggetti di Excel ##

Le macro utilizzano le routine VBA sul retro e seguono il [Modello a oggetti di Excel](https://docs.microsoft.com/en-us/office/vba/api/overview/excel/object-model) per questo scopo. Questo modello identifica gli oggetti di un foglio di calcolo per l'interazione con il foglio di calcolo tramite barre degli strumenti dei comandi, barre dei comandi o finestre di messaggi definite dall'utente. Ad esempio, l'accesso alle proprietà della cartella di lavoro viene concesso con l'oggetto Cartella di lavoro. Allo stesso modo, nel modello è presente un oggetto Foglio di lavoro per lavorare con i fogli di lavoro della cartella di lavoro a livello di codice.

## Macro e sicurezza ##

VBA consente l'accesso a tutte le aree di applicazione e al file system e può anche essere pericoloso. Ciò solleva preoccupazioni quando si condivide la cartella di lavoro con qualcuno che può eseguire il file alla sua fine. Questo è Microsoft Excel che avverte sull'apertura di un file del genere. Le macro possono essere certificate con una firma digitale in modo che altri utenti possano verificarne l'affidabilità. Pertanto, le macro possono essere abilitate dopo la verifica della loro origine.

## Riferimenti ##

* [[MS-XLS] - Struttura del formato file binario di Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Macroprogrammazione](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programmazione)

