{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Formato file Microsoft OneNote",
  "description":"Scopri il formato di file ONETOC2 e le API che possono creare e aprire file ONETOC2.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Cos'è ONETOC2? ##

Coloro che hanno lavorato con l'applicazione [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) potrebbero aver notato la presenza di file .onetoc2 nella cartella del blocco appunti. Microsoft OneNote crea un file binario .onetoc2 come Sommario per mantenere un indice sull'ordine delle diverse sezioni per prendere appunti in un blocco appunti. Un taccuino è una raccolta di file di sezione archiviati nella stessa directory. Il file .onetoc2 utilizza una raccolta di proprietà per specificare impostazioni come l'ordine delle sezioni all'interno del notebook e il colore del notebook.

Quando crei un blocco appunti in OneNote 2016, viene salvato automaticamente nel nuovo formato di file 2010-2016. Avrai bisogno di questo formato se vuoi che tutte le funzionalità di OneNote 2016, come equazioni matematiche e note collegate, funzionino correttamente.

## Formato file ONETOC2 ##

Il formato di file .onetoc2 è rappresentato come OneNote Revision Store File Format ed è una raccolta di strutture che specificano un archivio di revisioni organizzato in spazi oggetti con riferimenti incrociati, contenente oggetti con set di proprietà e contenente un registro delle transazioni per garantire l'integrità dei file in modo asincrono scrive. Le specifiche complete per il formato di file .onetoc2 sono disponibili [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) e possono essere consultate per lo sviluppo di applicazioni .

### Struttura del file ###

Un file di archivio di revisione DEVE iniziare con una struttura **Header**. Il resto del file è partizionato in blocchi di byte, dove la dimensione e la struttura di ogni blocco è specificata dal campo che vi fa riferimento. Un blocco è raggiungibile se è referenziato dalla struttura **Header** o se è referenziato da un campo in un altro blocco raggiungibile. I dati al di fuori della struttura **Header** e gli eventuali blocchi raggiungibili DEVONO essere ignorati.

Tutte le strutture sono allineate su limiti di 1 byte. Tutti i numeri interi sono firmati se non diversamente specificato. Tutti i campi sono [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) se non diversamente specificato.

#### Intestazione ####

L'intestazione del file .ONE comprende blocchi che contengono diversi ID univoci e campi per la rappresentazione delle informazioni sul file come segue:

`guidFileType (16 byte):` Un GUID che specifica il tipo del file di archivio delle revisioni. DEVE essere uno dei valori della tabella seguente.

|Formato file|Valore
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 byte):` Un GUID che specifica l'identità di questo file di archivio di revisione. DOVREBBE essere unico a livello globale.

`guidLegacyFileVersion (16 byte):` DEVE essere "{00000000-0000-0000-0000-000000000000}" e DEVE essere ignorato.

`guidFileFormat (16 byte):` Un GUID che specifica che il file è un file di archivio di revisioni. DEVE essere "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 byte):` Un intero senza segno. DEVE essere uno dei valori nella tabella seguente, a seconda del tipo di file.

|Formato file|Valore
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 byte):` Un intero senza segno. DEVE essere uno dei valori nella tabella seguente, a seconda del formato del file di questo file.


|Formato file|Valore
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 byte):` Un intero senza segno. DEVE essere uno dei valori nella tabella seguente, a seconda del formato del file di questo file.
:


|Formato file|Valore
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 byte):` Un intero senza segno. DEVE essere uno dei valori nella tabella seguente, a seconda del formato del file di questo file.


|Formato file|Valore
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

## Riferimenti ##

* [[MS-ONESTORE] - Formato file OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

