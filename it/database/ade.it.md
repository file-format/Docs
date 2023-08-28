{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file ADE e le API che possono creare e aprire file ADE.",
  "title" :"ADE - Accedi al file di estensione del progetto",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Che cos'è un file ADE?

Un file con estensione .ade è un file di progetto di Microsoft Access che contiene l'output compilato delle informazioni contenute nel file di progetto ADP di Microsoft Access. Le informazioni nel file di progetto di Access, diverse da Visual Basic, Applications Edition (VBA), sono disponibili in formato compilato nei file ADE. I dati vengono archiviati in formato compresso in questi file per ridurre le dimensioni del file e migliorare le prestazioni in Access. Poiché ADE è l'output compilato del file di progetto di Access, qualsiasi codice sorgente VBA che fa parte del progetto rimane protetto non consentendogli di far parte dell'output. I file ADE possono essere aperti in Microsoft Access 365.

## Formato file ADE - Ulteriori informazioni

ADE sono file di database di Access compilati che vengono archiviati su disco come file binari. La struttura dei file interni di questi file non è nota.

I file ADE possono creare problemi nell'apertura in base alla versione di Microsoft Access che è stata utilizzata per creare questi file. I database di Access che utilizzano la versione a 64 bit di Microsoft Access 2010 e che vengono compilati come file MDE, [ACCDE](/it/database/accde/) o ADE devono essere ricompilati in Microsoft Access 2021 Service Pack 1 (SP1) per funzionare correttamente con Access 2010 SP1. Questo problema si verifica perché Access 2010 SP1 utilizza una versione più recente del file VBE7.dll (versione 7.00.1619).

## Riferimenti

* [Problema con Access ADE Files](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Quali formati di file di accesso da utilizzare](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

