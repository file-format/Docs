{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "file", "estensione", "formato file", "Excel", "Foglio di calcolo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"La tua guida al formato dei file per sapere cos'è un file XLS e le API che possono crearli e aprirli.",
  "title" :"Cos'è il formato di file XLS? Impara dagli esperti di formati di file!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Che cos'è un file XLS?

I file con estensione XLS rappresentano il formato file binario di Excel. Tali file possono essere creati da Microsoft Excel e da altri programmi di fogli di calcolo simili come OpenOffice Calc o Apple Numbers. Il file salvato da Excel è noto come cartella di lavoro in cui ogni cartella di lavoro può avere uno o più fogli di lavoro. I dati vengono archiviati e visualizzati agli utenti in formato tabella nel foglio di lavoro e possono comprendere valori numerici, dati di testo, formule, connessioni dati esterne, immagini e grafici. Applicazioni come Microsoft Excel ti consentono di esportare i dati della cartella di lavoro in diversi formati tra cui [PDF](/it/pdf/), [CSV](/it/spreadsheet/csv/), [XLSX](/it/spreadsheet/xlsx/), [TXT](/it/word-processing/txt/), [HTML](/it/web/html/), [XPS](/it/page-description-language/xps/) e molti altri. Il formato di file XLS è stato sostituito con un formato più aperto e strutturato, XLSX, con il rilascio di Microsoft Excel 2007. Le ultime versioni forniscono ancora supporto per la creazione e la lettura di file XLS, sebbene XLSX sia la prima scelta di utilizzo ora.

## Breve storia

XLS è stato creato da Microsoft per l'uso con Microsoft Excel ed è anche noto come Binary Interchange File Format (BIFF). Questo tipo di file è stato introdotto per la prima volta rendendolo parte di Excel per Windows nel 1987. Le specifiche del formato di file XLS sono state rese pubbliche per la prima volta nel giugno 2008 come Revisione 1. Successivamente, le specifiche sono state continuamente aggiornate e l'ultima revisione disponibile è ad agosto 2018 contrassegnato come Revisione 8.0. Una breve storia delle diverse versioni del formato di file XLS è la seguente:

* Versione 7.0 (rilasciata con Office 95): questa versione di excel era la più robusta e veloce tra tutte le versioni e le riscritture del flusso interno sono state aggiornate a 32 bit.
* Versione 8 (rilasciata con Office 97): VBA è stato introdotto come linguaggio standard e le etichette in linguaggio naturale rimosse sono state incorporate per la prima volta in questa versione. Per la prima volta ha anche introdotto un assistente d'ufficio con graffette.
* Versione 9 (rilasciata con Office 2000): nella versione 9 sono state apportate solo modifiche minori in cui l'assistente per l'ufficio con graffette poteva contenere contemporaneamente più oggetti che in precedenza non erano possibili.
* Versione 10 (rilasciata con Office XP): questa versione non conteneva alcun miglioramento evidente.
* Versione 11 (rilasciata con Office 2003): importante aggiornamento nella versione 11, excel 2003 è stata l'introduzione di nuove tabelle.

## Specifiche del formato file XLS ##

I dati sono organizzati in un file XLS come flussi binari sotto forma di un file composto come descritto in [MS-CFB]. I dati vengono archiviati nel file composto utilizzando archivi, flussi e flussi secondari che contengono informazioni sul contenuto e sulla struttura di una cartella di lavoro, inclusi i dati della cartella di lavoro come le definizioni del foglio di lavoro. Ogni flusso o flusso secondario contiene una serie di record binari. Ogni record binario contiene zero o più campi strutturati che contengono i dati della cartella di lavoro. Questa sezione fornisce una breve panoramica della struttura dei file XLS, ma per le specifiche dettagliate del formato dei file, è necessario consultare le [Specifiche della formazione dei file XLS](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) documento di Microsoft.

#### Stream e Substream ####

Una cartella di lavoro è rappresentata dal flusso della cartella di lavoro. Ogni foglio di lavoro in una cartella di lavoro è rappresentato da sottostream. Inoltre, ha il sottoflusso del foglio grafico, il sottoflusso del foglio macro o il sottoflusso del foglio di dialogo che segue il flusso secondario globale. Ogni flusso binario o flusso secondario che contiene i dati della cartella di lavoro DEVE essere scritto come una serie di record binari.

#### Disco ####

Le informazioni sulle funzionalità in una cartella di lavoro vengono archiviate come record che è una sequenza di byte di lunghezza variabile. Un record binario è costituito dai tre componenti seguenti:

**Tipo di record:** Il tipo di record è un intero senza segno a due byte che specifica il tipo di informazioni specificato dal record e come è ordinata e strutturata la struttura dei dati del record specifici per questo record. I valori del tipo di record DEVONO essere un valore dall'enumerazione dei record (sezione 2.3) o il record DEVE utilizzare la futura architettura dei record (sezione 2.1.6).

**Record Size**: la dimensione del record è un intero senza segno di due byte che specifica il conteggio dei byte che specifica la dimensione totale dei dati del record. La dimensione del record DEVE essere maggiore o uguale a 0 e DEVE essere minore o uguale a 8224.

**Dati del record:** Il componente dei dati del record contiene campi che corrispondono a un particolare tipo di record e comprendono il resto del record. L'ordine e la struttura dei campi per un determinato tipo di record sono specificati nella sezione corrispondente per quel tipo di record. La dimensione del componente dei dati del record DEVE essere uguale alla dimensione del record. I campi nel componente dei dati del record possono contenere valori semplici, matrici di valori, strutture di diversi campi, matrici di campi e matrici di strutture.

#### Tabella delle celle ####

Le celle sono i blocchi fondamentali di una cartella di lavoro che memorizzano i contenuti della cartella di lavoro come testo, formule e dati numerici. Le celle mantengono il record dei dati archiviati tramite una struttura di dati chiamata Cell Table. La Cell Table stessa è memorizzata nella sequenza di record conformi alle regole CELLTABLE definite nel documento delle specifiche. Consiste in una serie di blocchi di file in cui le file sono disposte in blocchi di file. Ogni blocco di righe contiene righe dalla prima riga contenente dati all'ultima riga contenente dati.

La formattazione dei dati o delle righe viene salvata in un record Riga per ogni blocco riga. Ogni cella che contiene dati o la formattazione di una singola cella è rappresentata da un record. La formattazione associata a una cella può essere derivata dalla formattazione di una singola cella, dalla formattazione delle righe, dalla formattazione delle colonne o dal formato predefinito della cella. L'ordine di precedenza per la formattazione è la formattazione della singola cella con la precedenza più alta, seguita dalla formattazione della riga, quindi dalla formattazione della colonna e quindi dal formato della cella predefinito. Le celle che non contengono dati e non contengono formattazione individuale non vengono salvate.

#### Formule ####

Una formula è una sequenza di valori, riferimenti di cella, nomi, funzioni o operatori in una cella che insieme producono un nuovo valore. Le formule vengono archiviate in una rappresentazione tokenizzata nota come "espressioni analizzate". Un'espressione analizzata viene convertita in una formula testuale in fase di esecuzione per la visualizzazione e la modifica dell'utente. Le formule delle celle sono specificate dal record Formula. Le formule di matrice sono specificate dal record di matrice. Le formule condivise sono specificate dal record ShrFmla.

#### Grafici ####

Il foglio grafico specifica un grafico, un elemento grafico che visualizza i dati o le relazioni tra insiemi di dati in forma visiva e una cache dei dati del grafico, una copia locale dei dati utilizzata nei dati del grafico è mancante o se mancano collegamenti a dati esterni le origini dati sono interrotte. Il grafico specifica gruppi a uno o due assi, un insieme di assi su cui vengono tracciati i dati del grafico e l'insieme di serie, linee di tendenza e barra di errore specificati nel grafico. Ciascun gruppo di assi specifica da uno a quattro gruppi di grafici che specificano il tipo di visualizzazione utilizzato per visualizzare i dati. Ciascuna serie, linea di tendenza e barra di errore specifica un gruppo di grafici a cui è associata.

#### Metadati ####

I metadati sono dati aggiuntivi associati a una particolare cella o al suo contenuto. I metadati vengono registrati in BIFF8 solo per scopi di estendibilità futuri.

#### Tabelle pivot ####

Una tabella pivot è un meccanismo per riepilogare i dati di origine per ottenere una panoramica della distribuzione di tali dati. In una tabella pivot, le colonne applicabili dei dati di origine diventano campi che possono essere utilizzati per riepilogare i dati. Quando i dati di origine della tabella pivot sono dati di origine OLAP, le gerarchie OLAP e alcune altre entità OLAP diventano campi nella tabella pivot.
Una tabella pivot ha due parti principali, una visualizzazione PivotCache e una tabella pivot. Possono esistere più viste di tabella pivot basate su una singola PivotCache non OLAP.

#### Stili ####

Questa panoramica descrive come vengono specificate le informazioni di formattazione e protezione per le celle in un foglio (1). La formattazione delle celle è composta da diversi insiemi di proprietà:

* Proprietà del carattere (grassetto, corsivo, colore del carattere, dimensione del carattere, ecc...)
* Proprietà di riempimento (colore di primo piano, colore di sfondo, motivo, sfumatura, ecc...)
* Proprietà di allineamento (allineamento a sinistra, al centro, a destra, ecc...)
* Proprietà del bordo (sinistro, destro, superiore, inferiore, spesso o sottile, colore, ecc...)
* Proprietà di formattazione dei numeri (data, ora, numero di cifre decimali, ecc…)
* Proprietà di protezione (bloccato, nascosto, ecc...)

Queste proprietà, nel complesso, descrivono come viene visualizzata e stampata una determinata cella.

## Riferimenti ##

* [[MS-XLS] - Struttura del formato file binario di Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Formato file binario file composto](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

