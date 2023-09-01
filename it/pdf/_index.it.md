{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "fondamentali" ],
  "description":"Portable Document Format (PDF) è una rappresentazione standard di documenti indipendente da software, hardware e sistema operativo. Gli standard PDF includono PDF/A, PDF/E, PDF/UA, PDF/VT e PDF/X.",
  "title" :"Formato file PDF - Che cos'è un file PDF?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) è un tipo di documento creato da Adobe negli anni '90. Lo scopo di questo formato di file era quello di introdurre uno standard per la rappresentazione di documenti e altro materiale di riferimento in un formato indipendente dal software applicativo, dall'hardware e dal sistema operativo. Il formato di file PDF ha la piena capacità di contenere informazioni come testo, immagini, collegamenti ipertestuali, campi modulo, rich media, firme digitali, allegati, metadati, caratteristiche geospaziali e oggetti 3D che possono diventare parte del documento di origine.

Nella maggior parte dei casi, i documenti esistenti vengono convertiti in PDF anziché creare un nuovo PDF da zero. Ma ciò non significa che non ci siano software per la creazione o la manipolazione di file PDF.

**(Devi condividere qualcosa sul formato del file PDF? Puoi pubblicare i tuoi risultati nella sezione [Notizie sul formato del file PDF](https://news.fileformat.com/t/PDF).)**

## Formato file PDF - Breve storia

Una rapida panoramica della sequenza temporale sulla formazione del file PDF in termini di sequenza temporale è la seguente:

**1993** - Adobe Systems ha reso disponibili gratuitamente le specifiche PDF

**2008** - Il PDF è stato rilasciato come standard aperto il 1 luglio 2008 ed è stato pubblicato dall'Organizzazione internazionale per la standardizzazione come **ISO 32000-1:2008**.

**2008** - Adobe ha pubblicato una licenza di brevetto pubblico in formato ISO 32000-1 diritti esenti da royalty per tutti i brevetti di proprietà di Adobe necessari per realizzare, utilizzare, vendere e distribuire implementazioni conformi ai PDF.

La prima versione di PDF designata come PDF 1.0 che in seguito ha subito revisioni fino a PDF 1.7. PDF 1.7, che è diventato ISO 32000-1, include alcune tecnologie proprietarie non standardizzate, come Adobe XML Forms Architecture (XFA) e l'estensione JavaScript per Acrobat. Era il 28 luglio 2017 quando è stato pubblicato il PDF 2.0, noto come ISO 32000-2:2017 che non include tecnologie non standardizzate.

## Specifiche del formato file PDF

Un file PDF è un insieme di byte che possono essere raggruppati in token in base a regole di sintassi definite dalle specifiche PDF. Una o più token vengono combinati per formare entità sintattiche di livello superiore, principalmente oggetti, che sono i valori dei dati di base da cui viene costruito un documento PDF.

### Struttura dei file dei file PDF

Il contenuto del file PDF è disposto nella seguente sequenza all'interno del file.

|Intestazione
|Corpo
|Tabella di riferimento incrociato
|Rimorchio

#### Intestazione del file PDF ####

Indipendentemente dalla versione PDF, un file PDF inizia con un'intestazione contenente l'identificatore univoco per PDF e la versione del formato come %PDF-1.x dove x varia da 1 a 7.

#### Corpo del file ####

Il corpo di un file PDF è costituito da una sequenza di oggetti indiretti che rappresentano il contenuto di un documento. Gli oggetti, come descritto sopra, rappresentano componenti del documento come caratteri, pagine e immagini campionate. A partire da PDF 1.5, il corpo può anche contenere flussi di oggetti, ognuno dei quali contiene una sequenza di oggetti indiretti.

#### Tabella di riferimento incrociato ####

La tabella dei riferimenti incrociati contiene informazioni che consentono l'accesso casuale agli oggetti indiretti all'interno del file in modo che non sia necessario leggere l'intero file per individuare un oggetto particolare. La tabella deve contenere una voce di una riga per ogni oggetto indiretto, specificando l'offset di byte di quell'oggetto all'interno del corpo del file. (A partire da PDF 1.5, alcune o tutte le informazioni sui riferimenti incrociati possono in alternativa essere contenute in flussi di riferimenti incrociati.

#### File Trailer ####

Il trailer di un file PDF consente a un lettore conforme di trovare rapidamente la tabella dei riferimenti incrociati e determinati oggetti speciali. I lettori conformi dovrebbero leggere un file PDF dalla sua fine. L'ultima riga del file deve contenere solo l'indicatore di fine file, %%EOF. Le due righe precedenti devono contenere, una per riga e nell'ordine, la parola chiave startxref e l'offset di byte nel flusso decodificato dall'inizio del file all'inizio della parola chiave xref nell'ultima sezione di riferimento incrociato.

### Oggetti PDF ###

Un file PDF include diversi tipi di oggetti dei seguenti tipi

* Valori booleani - che rappresentano il vero o il falso condizionale
* Numeri: valori interi e reali
* Stringhe: contiene i caratteri tra parentesi
* Nomi - iniziano con un carattere / avanti es. /ASomewhatLongerName risulta in AsomewhatLongerName
* Array: il PDF supporta gli array unidimensionali. Gli array di dimensioni superiori possono essere costruiti utilizzando gli array come elementi nidificati
* Dizionari: raccolta di oggetti come coppie chiave-valore. Può avere zero voci.
* Streams - rappresenta la sequenza di byte che può essere anche di lunghezza illimitata
* Null Object: rappresenta un valore nullo

Possono esserci altri oggetti come commenti che vengono introdotti con il segno % e possono contenere caratteri a 8 bit.

### Oggetti indiretti ###

Qualsiasi oggetto in un file PDF può essere etichettato come oggetto indiretto. Agli oggetti indiretti viene assegnato un identificatore di oggetto univoco mediante il quale altri oggetti possono fare riferimento ad esso. I riferimenti incrociati a questi vengono mantenuti in una tabella di indice e contrassegnati con la parola chiave xref che segue il corpo principale e fornisce l'offset di byte di ciascun oggetto indiretto dall'inizio del file.

### Layout PDF lineari e non lineari ###

I layout PDF sono classificati come Llnear e non lineare a seconda delle applicazioni di destinazione e di altri fattori.

Non lineare: i file PDF non lineari utilizzano meno spazio su disco rispetto ai file PDF lineari. Le pagine PDF del documento risiedono in forma sparsa nel file PDF ed è per questo che i file non lineari sono più lenti rispetto ai file lineari.

PDF lineare - Destinati ai visualizzatori PDF online, i file PDF lineari sono costruiti in modo tale da essere scritti su disco in modo lineare. Ciò non richiede plug-in del browser per il caricamento dell'intero documento prima della visualizzazione.

### Panoramica degli oggetti ###

Come accennato, PDF body è una raccolta di oggetti sopra menzionati. Il PDF è in gran parte basato su PostScript senza le funzionalità di controllo dei linguaggi di programmazione come i comandi if e loop. I comandi emessi dal codice Postscript per generare contenuti grafici vengono raccolti e tokenizzati in aggiunta a eventuali file, grafici o font riferiti dal documento. Tutti questi contenuti vengono accumulati in un unico file, risultando in un output PostScript composto.

#### Testo ####

Il testo in PDF è rappresentato da elementi di testo che vengono effettivamente visualizzati con glifi dai caratteri. Un glifo è una forma grafica ed è soggetto a tutte le manipolazioni grafiche, come la trasformazione delle coordinate. A causa dell'importanza del testo nella maggior parte delle descrizioni delle pagine, PDF offre funzionalità di livello superiore per descrivere, selezionare e rendere i glifi in modo comodo ed efficiente.

#### Grafica ####

Gli operatori grafici utilizzati nei flussi di contenuto PDF descrivono l'aspetto delle pagine da riprodurre su un dispositivo di output raster. Le strutture sono destinate sia alle applicazioni di stampa che di visualizzazione. Gli operatori grafici formano sei gruppi principali:

* Gli operatori dello stato grafico manipolano la struttura dei dati chiamata stato grafico, il framework globale all'interno del quale vengono eseguiti gli altri operatori grafici. Lo stato grafico include l'attuale matrice di trasformazione (CTM), che mappa le coordinate dello spazio utente utilizzate all'interno di un flusso di contenuto PDF nelle coordinate del dispositivo di output. Include anche il colore corrente, il tracciato di ritaglio corrente e molti altri parametri che sono operandi impliciti degli operatori di pittura.
* Gli operatori di costruzione di percorsi specificano percorsi, che definiscono forme, traiettorie di linea e regioni di vario tipo. Includono operatori per iniziare un nuovo percorso, aggiungere segmenti di linea e curve e chiuderlo.
* Gli operatori di tracciatura riempiono un tracciato con un colore, dipingono un tratto lungo di esso o lo usano come contorno di ritaglio.
* Altri operatori di pittura dipingono alcuni oggetti grafici autodescrittivi. Questi includono immagini campionate, ombreggiature geometricamente definite e interi flussi di contenuto che a loro volta contengono sequenze di operatori grafici.
* Gli operatori di testo selezionano e mostrano i glifi dei caratteri dai caratteri (descrizioni di caratteri tipografici per rappresentare caratteri di testo). Poiché PDF tratta i glifi come forme grafiche generali, molti degli operatori di testo possono essere raggruppati con lo stato grafico o con gli operatori di disegno. Tuttavia, le strutture dei dati e i meccanismi per gestire le descrizioni dei glifi e dei caratteri sono sufficientemente specializzati.
* Gli operatori del contenuto contrassegnato associano informazioni logiche di livello superiore agli oggetti nel flusso di contenuto. Queste informazioni non influiscono sull'aspetto reso del contenuto; è utile per le applicazioni che utilizzano PDF per lo scambio di documenti.

## Riferimenti ##

* [Formato file PDF: struttura di base](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [Riferimento PDF - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

