{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file DTSX e le API che possono creare e aprire file DTSX.",
  "title" :"Formato file DTSX - File delle impostazioni DTS di SQL Server",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Che cos'è un file DTSX?

Un file con estensione .dtsx (Data Transformation Services Package XML) è un file Data Transformation Services (DTS) utilizzato da Microsoft SQL per fare riferimento a passaggi/regole di migrazione dei dati per il trasferimento di dati da un database a un altro. Ciò include le trasformazioni e le eventuali fasi di elaborazione facoltative che potrebbero essere richieste durante il trasferimento dei dati tra i punti di origine e di destinazione. SQL Server Integration Services (SSIS), un componente di Microsoft SQL Server, utilizza i file DTSX per identificare i passaggi per l'elaborazione dei dati tra i server di database. I file DTSX possono essere aperti con Microsoft SQL Server 2019.

## Formato file DTSX

Lo spostamento dei dati tra i server di database richiede regole e fasi di elaborazione per garantire l'integrità dei dati durante questa operazione. SSIS garantisce che tutte queste attività, per spostare e conformare i dati da diverse fonti in un'impresa, si svolgano in modo conveniente. È qui che arriva DTSX che definisce le strutture che devono essere utilizzate da SSIS per stabilire i passaggi in cui i dati possono essere elaborati come segue attraverso questi passaggi.

Il flusso di dati descritto da DTSX è come mostrato nell'immagine seguente.

{{< figure src="../DataFlowDTSX.png" alt="Flusso di dati DTSX" >}}

DTSX è basato su [XML](/it/web/xml/) ed è documentato in [MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd). Il refactoring avanzato di DTSX XML è DTSX 2.0 che include nuovi attributi per le strutture, la sostituzione delle proprietà denominate come attributi XML principali, specifica i valori predefiniti per la maggior parte dei valori degli attributi e il posizionamento di elementi ripetuti all'interno di un elemento padre. Le strutture DTSX sono descritte utilizzando questi [schemi XML](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) e il formato strutturale è celar-text XML.

## Riferimenti

* [Formato DTSX - Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [Formato DTSX 2 - Di Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

