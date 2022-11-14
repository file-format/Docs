{
  "date" : "2019-12-13",
  "keywords" :[ "file ppt", "formato file ppt", "cos'è un file ppt", "file", "esempio ppt", "estensione file ppt", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file PPT e le API che possono creare e aprire file PPT.",
  "title" :"PPT - Formato file PowerPoint",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file PPT?

Un file con estensione PPT rappresenta un file PowerPoint che consiste in una raccolta di diapositive da visualizzare come SlideShow. Specifica il formato file binario utilizzato da Microsoft PowerPoint 97-2003. Un file PPT può contenere diversi tipi di informazioni come testo, punti puntati, immagini, contenuti multimediali e altri oggetti OLE incorporati. Microsoft ha creato un nuovo formato di file per PowerPoint, noto come [PPTX](/it/presentation/pptx/), dal 2007 in poi, basato su Office OpenXML ed è diverso da questo formato di file binario. Diversi altri programmi applicativi come OpenOffice Impress e Apple Keynote possono anche creare file PPT.

## Breve storia ##

Microsoft ha introdotto il formato di file PPT con il rilascio di PowerPoint nel 1987. Il formato binario stabile è stato condiviso come predefinito in PowerPoint 97-2003 per Windows. Il formato di file binario è supportato per la lettura e la scrittura dalle versioni più recenti di PowerPoint, incluso PowerPoint 2016.

## Specifiche del formato file ##

Dalla sua introduzione, il formato di file PPT ha subito diverse revisioni per l'aggiunta di nuove funzionalità e miglioramenti. Le ultime specifiche della versione disponibili sono quelle della revisione 6.0 che sono state pubblicate nell'agosto 2018 che non dovrebbero essere mescolate con il numero di prodotto reale del formato di file PPT poiché Microsoft non fornisce più modifiche per questo formato.

### Panoramica del formato file ###

Alcuni dei componenti chiave di un formato di file PPT sono i seguenti:

#### Diapositive ####

I dati utente come forme, testo, animazioni e contenuti multimediali vengono aggiunti a una presentazione all'interno di una diapositiva. Una presentazione può contenere una o più diapositive che vengono visualizzate come presentazione quando viene eseguita una presentazione. Una presentazione contiene diapositive master e diapositive master titolo che fungono da modello per le proprietà visive comuni delle diapositive della presentazione. C'è anche una diapositiva master di note e una diapositiva master di dispensa che ha uno scopo simile e fornisce proprietà visive comuni per tutte le diapositive delle note e tutte le dispense stampate.

#### Forme ####

Le forme sono oggetti che consentono agli utenti di aggiungere una varietà di contenuti a una diapositiva sotto forma di forme segnaposto, immagini e grafici. Le forme su una diapositiva master definiscono dati comuni per gruppi di forme.

#### Segnaposto Forme ####

Questi sono segnaposto speciali che fungono da contenitori per una varietà di oggetti. Diverse forme segnaposto possono essere utilizzate per fornire indizi per inserire tipi specifici di forme come tabelle o grafici. All'interno di una diapositiva, una forma segnaposto adotta le proprietà visive di una diapositiva master principale, una diapositiva master del titolo o una diapositiva master delle note.

#### Oggetti esterni ####

Oggetti esterni come audio incorporato e collegato, video collegato, oggetti OLE incorporati e collegati e collegamenti ipertestuali possono essere incorporati in una diapositiva. Questi oggetti possono essere utilizzati per attivare oggetti collegati per l'accesso a risorse esterne durante una presentazione.

### Strutture dei formati dei file ###

I formati di file binari di PowerPoint consistono nei seguenti flussi per rappresentare la struttura e i dati generali del documento.

* Flusso utente corrente
* Flusso di documenti PowerPoint
* Flusso di immagini
* Informazioni di riepilogo e Informazioni di riepilogo del documento (opzionale)

Le specifiche complete per il formato file DOC possono essere trovate fornite da [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) e dovrebbero essere consultate in riferimento alle sezioni citate nei dettagli seguenti.

#### Stream utente corrente ####

Tiene traccia dell'ultimo utente che ha aperto il documento e il suo nome deve essere "Utente corrente".

#### Flusso di documenti PowerPoint ####

Tiene traccia di tutte le informazioni su una presentazione PowerPoint e ne spiega il layout e il contenuto. È un flusso obbligatorio il cui nome DEVE essere "Documento PowerPoint". I contenuti di questo flusso sono specificati da una sequenza di record di primo livello. Le restrizioni di ordinamento parziale sulla sequenza di record sono specificate nei record PersistDirectoryAtom e UserEditAtom.

Come record contenitore, i record DocumentContainer, MainMasterContainer (sezione 2.5.3), HandoutContainer (sezione 2.5.8), SlideContainer (sezione 2.5.1) e NotesContainer (sezione 2.5.6) sono ciascuno la radice di un albero di record contenitore e record di atomi. All'interno di qualsiasi record contenitore, possono esistere altri record che non sono elencati in modo esplicito come record figlio. I record sconosciuti vengono identificati quando il campo recType della struttura RecordHeader (sezione 2.3.1) contiene un valore non specificato dall'enumerazione RecordType (sezione 2.13.24). Questi record sconosciuti, se incontrati, DEVONO essere ignorati e MAGGIO<1> essere conservati. I record sconosciuti possono essere ignorati cercando i byte recLen in avanti dalla fine della struttura RecordHeader.

Ogni volta che questo flusso viene scritto, è possibile aggiungere nuovi record di primo livello, una modifica dell'utente al flusso esistente, oppure l'intero contenuto del flusso può essere sostituito con una sequenza aggiornata di record di primo livello. Se l'intero flusso non viene sostituito, tutti i record di livello superiore precedentemente esistenti che comprendevano qualsiasi modifica utente precedente, possono essere resi obsoleti dai record di livello superiore aggiunti successivamente che comprendono la modifica utente corrente.

#### Streaming di immagini ####

Questo è un flusso facoltativo che contiene i dati sulle immagini contenute in una presentazione PowerPoint. Il suo nome DEVE essere "Immagini". I contenuti di questo flusso sono specificati dal record OfficeArtBStoreDelay come specificato nella sezione [MS-ODRAW] 2.2.21.

#### Flusso di informazioni di riepilogo ####

Mantiene le statistiche sul documento seguendo lo standard di Microsoft Office. Il nome del flusso di informazioni di riepilogo deve essere "\005SummaryInformation", dove \005 è il carattere con valore 0x0005, non la stringa letterale "\005". Questo flusso DOVREBBE essere omesso per i documenti crittografati. I contenuti di questo flusso sono specificati nella sezione [MS-OSHARED] 2.3.3.2.1.

#### Flusso di informazioni di riepilogo del documento ####

Un flusso facoltativo il cui nome DEVE essere "\005DocumentSummaryInformation", dove \005 è il carattere con valore 0x0005, non la stringa letterale "\005". Questo flusso PUÒ<2> essere omesso per i documenti crittografati. I contenuti di questo flusso sono specificati nella sezione [MS-OSHARED] 2.3.3.2.2.

#### Flusso di informazioni di riepilogo crittografato ####

Un flusso facoltativo il cui nome DEVE essere "EncryptedSummary". Questo flusso esiste solo in un documento crittografato. I contenuti di questo flusso sono specificati nella sezione [MS-OFFCRYPTO] 2.3.5.4.

#### Archiviazione firma digitale ####

Una memoria opzionale il cui nome DEVE essere "_xmlsignatures". PUÒ essere omesso e PUÒ essere ignorato. I contenuti di questa memoria sono specificati nella sezione [MS-OFFCRYPTO] 2.5.2.

#### Archiviazione dati XML personalizzata ####

Una memoria opzionale il cui nome DEVE essere "MsoDataStore". I contenuti della memoria sono specificati nella sezione [MS-OSHARED] 2.3.6.

#### Stream firme ####

Un flusso opzionale il cui nome DEVE essere "_signatures". DOVREBBE essere omesso e PUÒ essere ignorato. I contenuti di questo flusso sono specificati nella sezione [MS-OFFCRYPTO] 2.5.1.

## Riferimenti ##

* [Specifiche del formato file PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: tipi di dati comuni di Office e strutture di oggetti](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Struttura di crittografia dei documenti di Office](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [Formati file PowerPoint](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

