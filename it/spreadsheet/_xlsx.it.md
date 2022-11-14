{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"La tua guida al formato file per sapere cos'è un file _XLSX e le API che possono creare e aprire file _XLSX.",
  "title" :"Cos'è un file _XLSX?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Che cos'è un file _XLSX?

Un file con estensione .\_xlsx è in realtà un file [XLSX](/it/spreadsheet/xlsx/) che viene rinominato da qualche altra applicazione. Questo può accadere in alcuni casi quando il nome del file contiene un'estensione . alla fine del nome del file. I file \_XLSX possono essere aperti in Microsoft Excel in modo simile ai file XLSX rinominandoli nuovamente con estensione .xlsx.

## _Formato file XLSX - Ulteriori informazioni

I file _XLSX non sono diversi dai file XLSX e utilizzano lo standard Open XML adottato da Microsoft nel 2000. Prima di XLSX, [XLS](/it/spreadsheet/xls/) era il formato di file principale utilizzato per lavorare con i fogli di calcolo Excel per salvare i documenti in formato binario. Questo nuovo formato di file basato su XML presentava vantaggi come file di piccole dimensioni, resistenza alla corruzione dei file e rappresentazione delle immagini ben formattata. Questo nuovo formato di file basato su XML è diventato parte di Office 2007 e viene implementato anche nelle nuove versioni di Microsoft.

## \_Specifiche del formato file XLSX

Poiché un file \_XLSX è un file XLSX rinominato, ha le stesse specifiche del file originale. È solo un file di archivio basato sul formato di file di archivio [ZIP](/it/compression/zip/). Se vuoi vedere il contenuto di questo archivio, rinomina il file con estensione .zip ed estrailo per visualizzare i file costitutivi di questa cartella di lavoro di Excel. Una cartella di lavoro vuota, quando estratta nei suoi file, ha i seguenti file e cartelle costitutivi.

### [Tipi_di_contenuto].xml

Questo è l'unico file che si trova a livello di base quando viene estratto lo zip. Elenca i tipi di contenuto per le parti all'interno del pacchetto. Tutti i riferimenti ai file XML inclusi nel pacchetto sono referenziati in questo file XML.

### \_rels (Cartella)

Questa è la cartella Relazioni che contiene un singolo file XML che memorizza le relazioni a livello di pacchetto. I collegamenti alle parti chiave dei file Xlsx sono contenuti in questo file come URI. Questi URI identificano il tipo di relazione di ciascuna parte chiave con il pacchetto. Ciò include la relazione con il documento dell'ufficio principale situato come xl/workbook.xml e altre parti all'interno di docProps come proprietà principali ed estese.

### docProps

Questa cartella contiene le proprietà generali del documento. Questi includono un insieme di proprietà principali, un insieme di proprietà estese o specifiche dell'applicazione e un'anteprima in miniatura del documento. Una cartella di lavoro vuota contiene due file in questa cartella, ovvero app.xml e core.xml. Il core.xml contiene informazioni come autore, data di creazione, salvataggio e modifica. App.xml contiene informazioni sul contenuto del file.

### xl (Cartella)

Questa è la cartella principale che contiene tutti i dettagli sul contenuto della cartella di lavoro. Per impostazione predefinita, ha le seguenti cartelle:

* \_rels
* tema
* fogli di lavoro

e seguenti file xml:

* stili.xml
* cartella di lavoro.xml

## Riferimenti

* [MS-XLSX - Formato file .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

