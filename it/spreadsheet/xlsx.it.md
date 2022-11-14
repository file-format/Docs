{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "file", "estensione", "formato file", "Excel", "Foglio di calcolo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri cos'è un file XLSX e le API che possono creare e aprire file XLSX.",
  "title" :"Formato file XLSX - Che cos'è un file XLSX?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Che cos'è un file XLSX?

**XLSX** è un formato ben noto per i documenti Microsoft Excel che è stato introdotto da Microsoft con il rilascio di Microsoft Office 2007. Basato su una struttura organizzata secondo le Open Packaging Conventions come delineato nella [Parte 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) dello standard OOXML ECMA-376, il nuovo formato è un pacchetto zip che contiene una serie di file XML. La struttura ei file sottostanti possono essere esaminati semplicemente decomprimendo il file .xlsx.

## Breve storia del formato file XLSX

Il formato di file XLSX è stato introdotto nel 2007 e utilizza lo standard Open XML adattato da Microsoft nel 2000. Prima di XLSX, il formato di file comune utilizzato era [XLS](/it/spreadsheet/xls/) che era un formato di file binario puro. Il nuovo tipo di file ha aggiunto vantaggi di file di piccole dimensioni, meno modifiche alla corruzione e rappresentazione delle immagini ben formattata. Fu all'inizio del 2000 quando Microsoft decise di adottare la modifica per accogliere lo standard per **Office Open XML**. Entro il 2007, questo nuovo formato di file è entrato a far parte di Office 2007 e viene mantenuto anche nelle nuove versioni di Microsoft Office.

## Specifiche del formato file XLSX

Le [specifiche del formato file XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) sono disponibili online da Microsoft. Per vedere cosa c'è all'interno del file XLSX, rinominalo in file [ZIP](/it/compression/zip/) modificandone l'estensione, quindi estrailo per visualizzare i file costitutivi di questa cartella di lavoro di Excel. Una cartella di lavoro vuota, quando estratta nei suoi file, ha i seguenti file e cartelle costitutivi.

### [Tipi_di_contenuto].xml ###

Questo è l'unico file che si trova a livello di base quando viene estratto lo zip. Elenca i tipi di contenuto per le parti all'interno del pacchetto. Tutti i riferimenti ai file XML inclusi nel pacchetto sono referenziati in questo file XML.

### \_rels (Cartella) ###

Questa è la cartella Relazioni che contiene un singolo file XML che memorizza le relazioni a livello di pacchetto. I collegamenti alle parti chiave dei file Xlsx sono contenuti in questo file come URI. Questi URI identificano il tipo di relazione di ciascuna parte chiave con il pacchetto. Ciò include la relazione con il documento dell'ufficio principale situato come xl/workbook.xml e altre parti all'interno di docProps come proprietà principali ed estese.

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

## Esempio di formato XLSX ##


Per ogni foglio di lavoro Excel contenuto in una cartella di lavoro, esiste un file XML. Puoi trovare questi file XML nella cartella xl/worksheets. Tutte le informazioni contenute in un foglio di lavoro sono organizzate in diverse sezioni nel file XML. Esaminiamo un foglio di lavoro di esempio da una cartella di lavoro mostrata nell'immagine seguente.

{{< figure src="../XLSX file format.png" alt="Formato file XLSX" >}}

Come si può vedere, questo foglio di lavoro contiene contenuti nelle celle da A1 a B2 e un'immagine. Inoltre, la cella G13 è attualmente la cella attiva nel foglio di lavoro. Ora, esaminiamo il file xl/worksheets/sheet1.xml per vedere come queste informazioni sono rappresentate nel file XML. Il contenuto di questo file XML è mostrato di seguito.

{{< figure src="../XLSX File Format Details.png" alt="Formato file XPS" >}}

1. Alla scheda è applicato il colore del tema. È menzionato nel file XML con tag<tabColor> seguendo il tema id.
1. Il valore tabSelected è impostato su 1 che mostra che questo è il foglio selezionato
1. Come si può vedere nella prima immagine sopra, la cella G13 nel foglio di lavoro è una cella attiva menzionata anche nel file XML.
1. La scheda sheetData rappresenta i dati contenuti nel foglio di lavoro. Tuttavia, puoi vedere che il contenuto originale del foglio di lavoro non si trova da nessuna parte in questa sezione. Questo perché il testo è indirettamente referenziato dal foglio XML "sharedStrings". Questo collegamento assicura che ogni testo venga salvato una sola volta e possa essere nuovamente referenziato per risparmiare spazio.
1. L'immagine come si può vedere è referenziata dall'id di riferimento "rId2"

## Contribuire

Devi condividere qualcosa sui formati di file XLSX o Spreadsheet? Puoi pubblicare i tuoi risultati nella sezione [Notizie sul formato del file di Spreadsheet](https://news.fileformat.com/t/Spreadsheet).

## Riferimenti

* [[MS-XLSX] - Formato file XLSX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

