{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Formato file Microsoft OneNote",
  "description":"Scopri UN SOLO formato di file e le API che possono creare e aprire UN SOLO file.",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file .ONE? ##

Il file rappresentato dall'estensione .ONE viene creato dall'applicazione Microsoft OneNote. OneNote consente di raccogliere informazioni utilizzando l'applicazione come se si stesse utilizzando il blocco note per prendere appunti. I file di OneNote possono contenere diversi elementi che possono essere inseriti in posizioni non fisse nelle pagine del documento. Questi elementi possono contenere testo, scrittura a mano digitalizzata e oggetti copiati da altre applicazioni, inclusi immagini, disegni e clip multimediali (audio/video). Microsoft ora offre la versione online di OneNote come parte di Office365 in cui le note possono essere condivise con altri utenti di OneNote su Internet.

## Specifiche del formato file .ONE ##

Il formato di file di OneNote fornisce un modo efficace per rappresentare le note digitali come insiemi gerarchici di sezioni e pagine. Ogni pagina contiene contenuto definito dall'utente in una struttura specifica per la rappresentazione tramite il formato di file Document Object Model (DOM). Il modello dati di questo formato è illustrato di seguito.

### Panoramica della struttura ###

Come illustrato nel modello di dati per il formato di file di OneNote, un documento di OneNote è costituito da diversi elementi.

#### Sezione ####

Una sezione è il contenitore più in alto in un file di OneNote che contiene inoltre diversi elementi come:

* Pagine
* Metadati
* Proprietà

I metadati e le proprietà includono il nome della sezione, l'identificazione delle pagine contenute nella sezione e l'ordine in cui tali pagine vengono visualizzate. Il termine "sezione" si riferisce a tutte le pagine che si trovano in una sezione e alla rappresentazione di tali dati in un file di archivio delle revisioni di OneNote®, che ha un'estensione .one.

#### Pagina ####

Il contenuto definito dall'utente in un documento di OneNote è contenuto all'interno di una pagina. Le informazioni sulla pagina includono testo, elenchi, tabelle, titoli di pagina, immagini e tag di note. Una pagina è composta da oggetti struttura a cui viene aggiunta la maggior parte degli oggetti contenuti. A ciascuna pagina può essere assegnato un nome per una rappresentazione significativa e anche gli oggetti possono essere aggiunti direttamente alle pagine. Una pagina può inoltre contenere sottopagine in un sistema gerarchico.

#### Proprietà e insiemi di proprietà ####

I contenuti di OneNote sono costituiti da proprietà, set di proprietà e oggetti dati file. Un set di proprietà è una raccolta di proprietà che rappresenta un tipo di contenuto. Un oggetto dati file è un blocco di dati binari che contiene immagini, file incorporati o contenuto audio/video.

#### Blocco note di OneNote ####

Un taccuino è una raccolta di file di sezione archiviati nella stessa directory. Una raccolta di proprietà viene utilizzata per specificare impostazioni come l'ordine delle sezioni all'interno del taccuino e il colore del taccuino.

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

|Formato file|Valore
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 byte):` Un intero senza segno. DEVE essere uno dei valori nella tabella seguente, a seconda del formato del file di questo file.

|Formato file|Valore
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bytes):` Una struttura **FileChunkReference32** che DEVE avere un valore di "fcrZero".

`fcrLegacyTransactionLog (8 byte):` Una struttura **FileChunkReference32** che DEVE essere "fcrNil".

`cTransactionsInLog (4 byte):` Un numero intero senza segno che specifica il numero di transazioni nel registro delle transazioni. NON DEVE essere zero.

`cbLegacyExpectedFileLength (4 byte):` Un intero senza segno che DEVE essere zero e DEVE essere ignorato.

`rgbPlaceholder (8 byte):` Un intero senza segno che DEVE essere zero e DEVE essere ignorato.

`fcrLegacyFileNodeListRoot (8 byte):` Una struttura **FileChunkReference32** che DEVE essere "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 byte):` Un intero senza segno che DEVE essere zero e DEVE essere ignorato.

`fNeedsDefrag (1 byte):` DEVE essere ignorato.

`fRepairedFile (1 byte):` DEVE essere ignorato.

`fNeedsGarbageCollect (1 byte):` DEVE essere ignorato.

`fHasNoEmbeddedFileObjects (1 byte):` Un intero senza segno che DEVE essere zero e DEVE essere ignorato.

`guidAncestor (16 byte):` Un GUID che specifica il campo **Header.guidFile** del file del sommario, dato dalla tabella seguente:


|Formato file sommario|Posizione del file sommario
--- | --- |
|File di sezione - .One|Il file del sommario si trova nella stessa directory di questo file.
|File del sommario - .onetoc2|Il file del sommario si trova nella directory principale di questo file.

Se il GUID è {00000000-0000-0000-0000-000000000000}, questo campo non fa riferimento a un file di sommario.

`crcName (4 byte):` Un numero intero senza segno che specifica il valore CRC del nome di questo file di archivio di revisione. Il nome è la rappresentazione Unicode del nome del file con la sua estensione e un carattere null aggiuntivo alla fine. Questo CRC viene sempre calcolato utilizzando l'algoritmo CRC per il file .one, indipendentemente dal formato del file di archivio di revisione.

`fcrHashedChunkList (12 byte):` Una struttura **FileChunkReference64x32** che specifica un riferimento al primo **FileNodeListFragment** in un elenco di blocchi hash. Se il valore della struttura **FileChunkReference64x32** è "fcrZero" o "fcrNil", l'elenco di blocchi hash non esiste.

`fcrTransactionLog (12 byte):` Una struttura **FileChunkReference64x32** che specifica un riferimento alla prima struttura **TransactionLogFragment** in un registro delle transazioni. Il valore del campo **fcrTransactionLog** NON DEVE essere "fcrZero" e NON DEVE essere "fcrNil".

`fcrFileNodeListRoot (12 byte):` Una struttura **FileChunkReference64x32** che specifica un riferimento a un elenco di nodi di file radice. Il valore del campo **fcrFileNodeListRoot** NON DEVE essere "fcrZero" e NON DEVE essere "fcrNil".

`fcrFreeChunkList (12 byte):` Una struttura **FileChunkReference64x32** che specifica un riferimento alla prima struttura **FreeChunkListFragment**. Se il valore della struttura **FileChunkReference64x32** è "fcrZero" o "fcrNil", l'elenco di blocchi liberi non esiste.

`cbExpectedFileLength (8 byte):` Un numero intero senza segno che specifica la dimensione, in byte, di questo file di archivio di revisione.

`cbFreeSpaceInFreeChunkList (8 bytes):` Un intero senza segno che DOVREBBE specificare la dimensione, in byte, dello spazio libero specificato dall'elenco dei blocchi liberi.

`guidFileVersion (16 byte):` Un GUID. Quando viene modificato il valore del campo **cTransactionsInLog** o il campo **guidDenyReadFileVersion**, **guidFileVersion** DEVE essere modificato in un nuovo GUID.

`nFileVersionGeneration (8 byte):` Un numero intero senza segno che specifica il numero di modifiche del file. DEVE essere incrementato quando il campo **guidFileVersion** cambia.

`guidDenyReadFileVersion (16 byte):` Un GUID. Quando il contenuto esistente del file viene modificato, esclusa la struttura **Header** del file e i blocchi di archiviazione inutilizzati, **guidDenyReadFileVersion** DEVE essere modificato in un nuovo GUID.

`grfDebugLogFlags (4 byte):` DEVE essere zero. DEVE essere ignorato.

`fcrDebugLog (12 byte):` Una struttura **FileChunkReference64x32** che DEVE avere un valore "fcrZero". DEVE essere ignorato.

`fcrAllocVerificationFreeChunkList (12 byte):` Una struttura **FileChunkReference64x32** che DEVE essere "fcrZero". DEVE essere ignorato.

`bnCreated (4 byte):` Un numero intero senza segno che specifica il numero di build dell'applicazione che ha creato questo file di archivio di revisione. DOVREBBE essere ignorato.

`bnLastWroteToThisFile (4 bytes):` Un numero intero senza segno che specifica il numero di build dell'ultima applicazione che ha scritto su questo file di archivio di revisione. DOVREBBE essere ignorato.

`bnOldestWritten (4 byte):` Un numero intero senza segno che specifica il numero di build dell'applicazione più vecchia che ha scritto su questo file di archivio di revisione. DOVREBBE essere ignorato.

`bnNewestWritten (4 byte):` Un numero intero senza segno che specifica il numero di build dell'applicazione più recente che ha scritto su questo file di archivio di revisione. DOVREBBE essere ignorato.

`rgbReserved (728 byte):` DEVE essere zero. DEVE essere ignorato.

## Riferimenti ##

* [[MS-ONESTORE] - Formato file OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

