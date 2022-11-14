{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "file", "estensione", "formato file", "Excel Open XML", "Foglio di calcolo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"La tua guida al formato file per sapere cos'è un file XLTX e le API che possono crearli e aprirli.",
  "title" :"Cos'è un file XLTX?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Che cos'è un file XLTX?

I file con estensione .xltx rappresentano file modello Microsoft Excel basati sulle specifiche del formato di file Office OpenXML. Viene utilizzato per creare un file modello standard che può essere utilizzato per generare file [XLSX](/it/spreadsheet/xlsx/) che presentano le stesse impostazioni specificate nel file XLTX.

## Breve storia

Fu all'inizio del 2000 quando Microsoft decise di adottare la modifica per accogliere lo standard per **Office Open XML**. I documenti, di diverso tipo, nell'ambito di questo nuovo Standard sono stati identificati apponendo "X" nelle loro estensioni, dove "X" sta per XML. Entro il 2007, questo nuovo formato di file è entrato a far parte di Office 2007 e viene mantenuto anche nelle nuove versioni di Microsoft Office. Il nuovo tipo di file ha aggiunto vantaggi di file di piccole dimensioni, meno modifiche alla corruzione e una rappresentazione delle immagini ben formattata.

## Specifiche del formato file XLTX

I file XLTX sono basati sul formato di file Office OpenXML e utilizzano XML e [ZIP](/it/compression/zip/) per ridurre le dimensioni del file. È stato creato con il rilascio di Microsoft Office 2007 per sostituire il formato di file XLT binario. Simile a XLTX, il formato file XLT può essere utilizzato per creare file [XLS](/it/spreadsheet/xls/) utilizzando Microsoft Excel 2003 e 2007. Questi possono essere aperti con Microsoft Excel facendo doppio clic sul file. L'organizzazione dei file in un formato di file XLTX può essere osservata rinominando il file in ZIP e quindi estraendone il contenuto su disco.

### [Tipi_di_contenuto].xml ###

Questo è l'unico file che si trova a livello di base quando viene estratto lo zip. Elenca i tipi di contenuto per le parti all'interno del pacchetto. Tutti i riferimenti ai file XML inclusi nel pacchetto sono referenziati in questo file XML.

### \_rels (Cartella) ###

Questa è la cartella Relazioni che contiene un singolo file XML che memorizza le relazioni a livello di pacchetto. I collegamenti alle parti chiave dei file Xltx sono contenuti in questo file come URI. Questi URI identificano il tipo di relazione di ciascuna parte chiave con il pacchetto. Ciò include la relazione con il documento dell'ufficio principale situato come xl/workbook.xml e altre parti all'interno di docProps come proprietà principali e estese.

### docProps ###

Questa cartella contiene le proprietà generali del documento. Questi includono un insieme di proprietà principali, un insieme di proprietà estese o specifiche dell'applicazione e un'anteprima in miniatura del documento. Una cartella di lavoro vuota contiene due file in questa cartella, ovvero app.xml e core.xml. Il core.xml contiene informazioni come autore, data di creazione, salvataggio e modifica. App.xml contiene informazioni sul contenuto del file.

### xl (Cartella) ###

Questa è la cartella principale che contiene tutti i dettagli sul contenuto della cartella di lavoro. Per impostazione predefinita, ha le seguenti cartelle:

* \_rels
* tema
* fogli di lavoro

e seguenti file xml:

* stili.xml
* cartella di lavoro.xml

## Riferimenti ##

* [[MS-XLSX] - Formato file .Xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

