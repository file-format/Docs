{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "file", "estensione", "formato file", "Word", "Documento" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - File di documento di Microsoft Word",
  "description":"Scopri il formato di file DOC e le API che possono creare e aprire file DOC.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Che cos'è un file DOC?

I file con estensione .doc rappresentano documenti generati da Microsoft Word o altri documenti di elaborazione testi in formato binario. L'estensione è stata inizialmente utilizzata per la documentazione in testo normale su diversi sistemi operativi. Può contenere diversi tipi di dati come immagini, formattati e testo normale, grafici, grafici, oggetti incorporati, collegamenti, pagine, formattazione della pagina, impostazioni di stampa e molti altri. Il formato era popolare per tutti i tipi di documentazione grazie alla varietà di opzioni che offre agli utenti per la scrittura di manuali, proposte, specifiche, curriculum, articoli o documenti simili. La versione aggiornata di DOC è [DOCX](/it/word-processing/docx/) che si basa su Office OpenXML le cui specifiche sono pubblicamente disponibili.

## Breve storia ##

WordPerfect, un prodotto di [Corel](https://www.corel.com/en/), utilizzava DOC come estensione del proprio formato proprietario. Negli anni '80, WordPerfect è rimasta la scelta di utilizzo sulla maggior parte dei computer grazie alla sua facile disponibilità, alla conformità con la maggior parte dei computer e dei sistemi operativi. Tuttavia, WordPerfect ha visto la sua caduta sul sistema operativo Windows quando Microsoft ha introdotto Microsoft Word come prodotto per il formato di file di documenti e ha scelto l'estensione DOC per il loro formato proprietario. Man mano che Microsoft Word è diventato sempre più popolare, il formato file DOC ha subito diverse revisioni da Microsoft Word 97 - 2003. Era il 2007 quando il formato file DOC predefinito è stato sostituito dal formato Office Open XML (noto come DOCX) e dalle nuove versioni di Microsoft Word ora usa questa nuova estensione come formato di file predefinito.

## Specifiche del formato file DOC - Ulteriori informazioni

Microsoft non ha rilasciato le specifiche del formato di file DOC per molto tempo fino al 2008. Nel febbraio 2008, le specifiche di formato sono state rilasciate per il formato di file .doc nell'ambito della Microsoft Open Specification Promise. Sebbene la specifica non descriva tutte le funzionalità utilizzate dal formato DOC, fornisce ampie informazioni sulle conoscenze richieste per lavorare con questo formato di file. Tuttavia, è necessario il reverse engineering per utilizzare le informazioni disponibili. Le specifiche sono state aggiornate più volte e l'ultima [revision](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) è 8.0, aggiornata ad agosto 2018 .

### Alcuni concetti fondamentali ###

Prima di entrare nei dettagli sulle specifiche del formato di file per DOC, è necessario comprendere alcuni concetti fondamentali per poter lavorare con questo formato di file.

**File Information Base (Fib):** La struttura Fib contiene informazioni sul documento e specifica i puntatori di file alle varie parti che compongono il documento.
Il Fib è una struttura a lunghezza variabile. Ad eccezione della porzione di base che ha dimensioni fisse, ogni sezione è preceduta da un campo di conteggio che specifica la dimensione della sezione successiva.

**Posizione carattere:** CP o Posizione carattere rappresenta un numero intero a 32 bit senza segno che funge da indice in base zero di un carattere nel testo del documento. La posizione e la dimensione di ciascun carattere nel file non possono essere recuperate direttamente e devono essere calcolate utilizzando un algoritmo pre-specificato. I personaggi includono:

* Testo del documento
* Ancoraggi di oggetti come note a piè di pagina o caselle di testo
* Controllare i caratteri come i segni di paragrafo e i segni di cella della tabella

**PLC:** La struttura del PLC è un array di CP seguito da un array di elementi di dati. Gli elementi di dati per qualsiasi PLC devono avere la stessa dimensione di zero o più byte e, per questo motivo, il numero di CP deve essere uno in più rispetto al numero di elementi di dati. Le strutture del PLC sono di tipi diversi in cui ogni tipo specifica se sono consentiti o meno CP duplicati per quel tipo. Una struttura PLC è composta da:

* **aCP (lunghezza variabile):** Un array di elementi CP. Ciascun tipo di struttura **PLC** specifica il significato degli elementi CP e l'intervallo consentito.
* **aData (lunghezza variabile):** Ciascun tipo di struttura **PLC** specifica la struttura e il significato degli elementi di dati, eventuali restrizioni sul numero di elementi di dati ed eventuali restrizioni sui dati in essi contenuti. Specifica inoltre la relazione tra gli elementi di dati ei CP corrispondenti.

**Selezione valida:** I costrutti di file .DOC sono principalmente descritti da un intervallo di CP. Esistono diverse [regole](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) specificate da Microsoft da seguire in questo caso.

**STTB:** STTB è una tabella di stringhe composta da un'intestazione seguita da una matrice di elementi. Il valore **cData** specifica il numero di elementi contenuti nell'array.

**Archiviazione proprietà:** Un file word può avere diversi elementi come testo, paragrafi, tabelle, immagini e sezioni in cui ognuno può avere le proprie proprietà. Le proprietà di questi sono memorizzate nel file di Word come differenze rispetto all'impostazione predefinita. Tali differenze sono specificate da PRl che consiste in un Single Property Modifier (Sprm) e il suo operando. Un'applicazione può determinare l'insieme finale di proprietà mediante l'applicazione di elenchi di **Prl**s.

**Protezione con password:** anche i file di Word possono essere protetti con password, per i quali è possibile utilizzare uno dei seguenti meccanismi.

* XOR offuscamento
* Crittografia del documento binario di Office RC4
* Crittografia del documento binario di Office RC4 CryptoAPI

Se FibBase.fEncrypted e FibBase.fObfuscation sono entrambi 1, il file viene offuscato utilizzando l'offuscamento XOR.

Se FibBase.fEncrypted è 1 e FibBase.fObfuscation è 0, il file viene crittografato utilizzando Office Binary Document RC4 Encryption o Office Binary Document RC4 CryptoAPI Encryption, con EncryptionHeader archiviato nei primi byte FibBase.lKey del flusso della tabella. EncryptionHeader.EncryptionVersionInfo specifica quale meccanismo di crittografia è stato utilizzato per crittografare il file.

### Struttura del file ###

Un file binario di Word nella sua originalità è un file composto OLE che comprende diversi archivi e flussi. Questi archivi e flussi hanno una propria struttura e dimensioni, che specificano i parametri per la scrittura e la lettura. Questi sono:

#### Flusso WordDocument ####

Questo flusso contiene il testo del documento e altre informazioni a cui si fa riferimento da altre parti del file. Il flusso non ha una struttura predefinita diversa dal FIB all'inizio che è obbligatorio e dovrebbe essere all'offset 0. Questo flusso non deve essere maggiore di 2147 MB.

#### 1TableStream o 0TableStream ####

Un file Word binario può contenere flussi di tabelle noti come flusso 1Table o flusso 0Table. Almeno uno di questi dovrebbe essere presente nel documento. Tuttavia, se un documento contiene entrambi i flussi 1Table e 0Table, viene utilizzato solo il flusso a cui fa riferimento base.fWhichTblStm. Il flusso non referenziato DEVE essere ignorato.
Il flusso della tabella NON DEVE essere maggiore di 2147 MB.

#### Flusso di dati ####

Il flusso di dati non ha una struttura predefinita. Contiene dati a cui si fa riferimento dalla FIB o da altre parti del file. Questo flusso non deve essere presente se non ci sono riferimenti ad esso. Il flusso di dati NON DEVE essere maggiore di 2147 MB.

#### Stoccaggio pool di oggetti ####

L'archivio del pool di oggetti contiene gli archivi per gli oggetti OLE incorporati. Questa memoria non deve essere presente se non sono presenti oggetti OLE incorporati nel documento.

#### Archiviazione dati XML personalizzata ####

L'archiviazione dei dati XML personalizzati è una memoria opzionale il cui nome DEVE essere "MsoDataStore".

#### Flusso di informazioni di riepilogo ####

Il flusso di informazioni di riepilogo è un flusso facoltativo il cui nome DEVE essere "\005Informazioni di riepilogo", dove \005 è il carattere con valore 0x0005 e non la stringa letterale "\005".

#### Flusso di informazioni di riepilogo del documento ####

Il flusso di informazioni di riepilogo del documento è un flusso opzionale il cui nome DEVE essere "\005DocumentSummaryInformation", dove \005 è il carattere con valore 0x0005, non la stringa letterale "\005".

#### Flusso di crittografia ####

Il flusso di crittografia è un flusso opzionale il cui nome DEVE essere "crittografia". Questo flusso NON DEVE essere presente a meno che non siano soddisfatte entrambe le seguenti condizioni:

* Il documento è crittografato con la crittografia Office Binary Document RC4 CryptoAPI.
* Il valore fDocProps è impostato in EncryptionHeader.Flags.

#### Archiviazione macro ####

La memoria Macro è una memoria facoltativa che contiene le macro per il file. Se presente, DEVE essere un archivio principale del progetto.

#### Archiviazione firme XML ####

La memoria delle firme XML è una memoria opzionale il cui nome DEVE essere "_xmlsignatures".

#### Stream firme ####

Il flusso delle firme è un flusso opzionale il cui nome DEVE essere "_signatures". Questo flusso contiene firme digitali.

#### Gestione dei diritti di informazione Archiviazione dello spazio dati ####

Lo spazio di archiviazione di Information Rights Management Data Space è un archivio opzionale il cui nome DEVE essere "\006DataSpaces", dove \006 è il carattere con valore 0x0006 e non la stringa letterale "\006". Se questa memoria è presente, DEVE essere presente anche il flusso di contenuto protetto.
Se questo spazio di archiviazione è presente, tutti i flussi e gli archivi specificati diversi da questo archivio e dal flusso di contenuti protetti DEVONO essere letti dal flusso di contenuti protetti come specificato in [MS-OFFCRYPTO] e se uno di questi flussi e archivi esiste al di fuori del contenuto protetto Stream, DEVONO essere ignorati.

#### Flusso di contenuti protetto ####

Il flusso di contenuto protetto è un flusso facoltativo il cui nome DEVE essere "\009DRMContent", dove \009 è il carattere con valore 0x0009 e non la stringa letterale "\009".
Se questo flusso è presente, DEVE essere presente anche l'Information Rights Management Data Space Storage.

## Riferimenti ##

* [Specifiche di formazione dei file MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))

