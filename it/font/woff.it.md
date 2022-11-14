{
  "date" : "2020-08-20",
  "keywords" :[ "file woff", "formato file woff", "cos'è un file woff", "file", "esempio woff", "estensione file woff", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Formato file aperto Web",
  "description":"Un file WOFF è un formato di carattere aperto creato in Web Open Font Format.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Che cos'è un file WOFF?

Un file con estensione .woff è un file di font web basato sul Web Open Font Format (WOFF). Ha un contenitore compresso specifico per il formato basato sui tipi di carattere TrueType (.TTF) o OpenType (.OTT). WOFF è stato introdotto con l'obiettivo di differenziare i caratteri Web dai file di caratteri utilizzati nelle applicazioni desktop. Inoltre, il formato mirava a ridurre la latenza del trasferimento dei caratteri dal server al computer del client tramite la rete. Sono disponibili diversi strumenti in grado di convertire file WOFF in TTF e altri formati di file di caratteri.

## **Formato file WOFF**

Il formato dei caratteri WOFF comprime le tabelle dei dati dei caratteri delle strutture sfnt basate su tabelle utilizzate in diversi tipi di carattere come TrueType, OpenType e Open Font Format. È come un contenitore per questi tipi di font e ha anche lo spazio per includere i metadati del font e i dati di uso privato da includere nel contenitore. I convertitori utilizzano i file sfnt in un file formattato WOFF e i programmi utente ripristinano il file codificato per l'uso con il documento web. Va notato che i dati del font ripristinati corrispondono esattamente al formato del font di input sotto tutti gli aspetti.

Le utilità di file WOFF spesso contengono funzionalità aggiuntive come sottoimpostazioni di glifi, convalida o aggiunte di funzionalità dei caratteri, ma non sono necessarie. Sia il creatore che gli agenti di utilizzo devono garantire che la validità dei dati dei caratteri sottostanti sia preservata.

### Struttura del file WOFF

La struttura del file WOFF è simile a quella dei caratteri sfnt. Si basa su una directory di tabelle che contiene le lunghezze e gli offset di ciascuna tabella di dati dei caratteri. Tutte le tabelle sono seguite dopo queste prime informazioni. Il file contiene un database dei caratteri che è lo stesso dei caratteri originali. Anche l'ordine delle tabelle è lo stesso, ma ciascuna può essere compressa. Tuttavia, la directory della tabella WOFF sostituisce la directory della tabella originale.

Un file WOFF è composto da:

* WOFFHeader - Intestazione del file con tipo e versione di font di base, insieme a offset per metadati e blocchi di dati privati.
* TableDirectory - Directory delle tabelle dei caratteri, che indica la dimensione originale, la dimensione compressa e la posizione di ciascuna tabella all'interno del file WOFF.
* FontTables - Le tabelle dei dati dei caratteri dal carattere sfnt di input, compressi per ridurre i requisiti di larghezza di banda.
* ExtendedMetadata - Un blocco opzionale di metadati estesi, rappresentato in formato XML e compresso per l'archiviazione nel file WOFF.
* PrivateData: un blocco opzionale di dati privati che può essere utilizzato dal designer di font, dalla fonderia o dal fornitore.

### Intestazione WOFF
L'intestazione WOFF comprende una firma identificativa che indica il tipo di dati inclusi nel file. L'intestazione WOFF insieme ai suoi campi è la seguente.

|Tipo|Nome campo|Descrizione|
---|---|---|
|UInt32|firma |0x774F4646 'wOFF' |
|UInt32| sapore |La "versione sfnt" del carattere di input.|
|UInt32| length |Dimensione totale del file WOFF.|
|UInt16| numTables |Numero di voci nella directory delle tabelle dei caratteri.|
|UInt16| riservato |Riservato; impostato a zero.|
|UInt32| totalSfntSize |La dimensione totale necessaria per i dati dei caratteri non compressi, incluse l'intestazione sfnt, la directory e le tabelle dei caratteri (incluso il riempimento).|
|UInt16| majorVersion |Versione principale del file WOFF.|
|UInt16| minorVersion |Versione secondaria del file WOFF.|
|UInt32| metaOffset |Offset al blocco di metadati, dall'inizio del file WOFF.|
|UInt32| metaLength |Lunghezza del blocco di metadati compressi.|
|UInt32| metaOrigLength |Dimensione non compressa del blocco di metadati.|
|UInt32| privOffset |Offset al blocco dati privato, dall'inizio del file WOFF.|
|UInt32| privLength |Lunghezza del blocco dati privato.|


## **Riferimenti**
* [Formato file w3 WOFF](https://www.w3.org/TR/WOFF/)

