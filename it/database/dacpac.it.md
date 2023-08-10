{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "Pacchetto applicazione livello dati"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file DACPAC e le API che possono creare e aprire file DACPAC.",
  "title" :"DACPAC - Pacchetto di applicazioni a livello di dati",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Che cos'è un file DACPAC?

Un file con estensione .dacpac (acronimo di Data Tier AppliCation Package) è un file di database, creato con l'applicazione di livello dati di Microsoft SQL Server, che contiene il modello di database per la rappresentazione degli oggetti di database. Poiché contiene il modello completo del database, viene utilizzato per ripristinare un database dai dettagli disponibili nel modello. I file DACPAC vengono solitamente consegnati ai team di distribuzione per l'installazione presso la sede del cliente per ripristinare il database. Questi possono essere aperti con
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Formato file DACPAC - Ulteriori informazioni

I file del pacchetto dati DACPAC sono in realtà file ZIP compressi che contengono diversi file [XML](/it/web/xml/) contenenti informazioni sul modello di database, come tabelle e viste, utilizzati per ripristinare un database. Per visualizzare il contenuto dei file DACPAC, rinominare i file da .dacpac a [.zip](/it/compression/zip/) ed estrarre l'archivio zip utilizzando qualsiasi utilità di decompressione.

Di seguito sono riportati alcuni file che si trovano all'interno di un file DACPAC.

* [Tipi_di_contenuto].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origine.xml

* modello.xml

Va notato che DACPAC non contiene DATI e altri oggetti a livello di server. Il file può contenere tutti i tipi di oggetti che potrebbero essere mantenuti nel progetto SSDT.

## Riferimenti

* [Applicazioni livello dati - Vantaggi](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Distribuzione di un'applicazione di livello dati - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Come creare un file DACPAC?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

