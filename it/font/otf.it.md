{
  "date" : "2020-08-20",
  "keywords" :[ "file otf", "formato file otf", "cos'è un file otf", "file", "esempio otf", "estensione file otf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - Formato file font TrueType",
  "description":"Scopri il formato di file OTF e le API che possono creare e aprire file OTF.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Che cos'è un file OTF?

Un file con estensione .otf si riferisce al formato del carattere OpenType. Il formato dei caratteri OTF è più scalabile ed estende le funzionalità esistenti dei formati [TTF](/it/font/ttf/) per la tipografia digitale. Sviluppato da Microsoft e Adobe, OTF combina le caratteristiche dei formati di font PostScript e TrueType. Ciò rende il formato OTF adatto ai sistemi di scrittura della maggioranza ed è per questo che viene utilizzato uniformemente sulle principali piattaforme di computer. Il formato del carattere OpenType è supportato da Mac OS X e Windows 2000 e versioni successive.

## Breve storia

Il requisito dei caratteri OpenType è nato come requisito per un formato di carattere più espressivo in grado di gestire una tipografia fine. Inoltre, mirava a soddisfare i requisiti di comportamento complesso di molti dei sistemi di scrittura del mondo. Microsoft ha tentato di concedere in licenza la tecnologia tipografica avanzata di Apple, nota come GX Typography, all'inizio degli anni '90. Ciò non è andato bene e, di conseguenza, Microsoft ha iniziato a migliorare la propria tecnologia dei caratteri TrueType nel 1994. Le modifiche includevano anche l'introduzione di un formato di carattere più adatto che soddisfa anche le caratteristiche dei formati di caratteri Type 1 (PostScript) di Adobe.

Adobe, nel 1996, si unì a Microsoft nei suoi sforzi per sostituire sia il TrueType di Apple che i propri formati di carattere Type 1. Ciò ha comportato la combinazione di entrambi i formati dei caratteri sottostanti per superare i limiti e aggiungere nuove estensioni. Questa nuova tecnologia è stata introdotta lo stesso anno con il nome **OpenType**.

## Specifiche del formato file OTF

Le specifiche OTF sono disponibili pubblicamente da Microsoft e possono essere richiamate dal punto di vista dello sviluppatore. Come TTF, utilizza la stessa struttura del contenitore 'sfnt' ed è compatibile con le specifiche TrueType. I dati all'interno di un file di font OpenType vengono utilizzati per diversi scopi, come il calcolo del layout del testo, la definizione di glifi come contorni TrueType o Compact Font Format (CFF), la fornitura di bitmap monocromatiche oa colori o documenti SVG come descrizioni di glifi alternativi e informazioni sui metadati.

### Tipi di dati OTF
I file OTF utilizzano i seguenti tipi di dati che sono tutti in Big Endian.

|Tipo di dati| Descrizione|
---|---|
|uint8| Intero senza segno a 8 bit.|
|int8| Intero con segno a 8 bit.|
|uint16| Intero senza segno a 16 bit.|
|int16| Intero con segno a 16 bit.|
|uint24| Intero senza segno a 24 bit.|
|uint32| Intero senza segno a 32 bit.|
|int32| Intero con segno a 32 bit.|
|Risolto| Numero a virgola fissa con segno a 32 bit (16.16)|
|FWORD| int16 che descrive una quantità in unità di progettazione dei caratteri.|
|UFWORD| uint16 che descrive una quantità in unità di progettazione dei caratteri.|
|F2DOT14| Numero fisso con segno a 16 bit con i 14 bit bassi della frazione (2.14).|
|LONGDATETIME| Data e ora rappresentate in numero di secondi dalle 12:00 mezzanotte del 1 gennaio 1904 UTC. Il valore è rappresentato come un intero a 64 bit con segno.|
|Etichetta| Matrice di quattro uint8 (lunghezza = 32 bit) utilizzata per identificare una tabella, un asse di variazione del design, uno script, un sistema linguistico, una funzione o una linea di base|
|Offset16| Scostamento corto su una tabella, come uint16, NULL offset = 0x0000|
|Offset32| Offset lungo su una tabella, come uint32, offset NULL = 0x00000000|
|Versione16Dot16| Valore compresso a 32 bit con numeri di versione principali e secondari. (Vedere i numeri di versione della tabella.)|

### Directory tabelle OTF

Un file OTF inizia con una directory di tabella. Questa directory è la raccolta di primo livello delle tabelle nel file dei caratteri. A seconda del numero di caratteri in un file, la directory della tabella potrebbe trovarsi in una posizione diversa nel file. Ad esempio, nel caso in cui il file di font abbia un solo font, la directory della tabella inizia dal byte 0 del file. In caso di più raccolte di caratteri OpenType,
l'inizio della directory della tabella è indicato in TTCHeader.

|Tipo |Nome |Descrizione|
---|---|---|
|uint32 |sfntVersion| 0x00010000 o 0x4F54544F ('OTTO')|
|uint16| numTables |Numero di tabelle.|
|uint16| searchRange |Potenza massima di 2 minore o uguale a numTables, volte 16 ((2\**floor(log2(numTables)))) * 16, dove “**” è un operatore di esponenziazione).|
|uint16 |entrySelector Log2 della potenza massima di 2 minore o uguale a numTables (log2(searchRange/16), che è uguale a floor(log2(numTables))).|
|uint16 |rangeShift |numTables volte 16, meno searchRange ((numTables * 16) - searchRange).|
|tabellaRecord| tableRecords[numTables] |Matrice di record di tabella: uno per ogni tabella di livello superiore nel font|


### Record tabella

Per ogni tabella di primo livello nel carattere, c'è un record tabella che consiste nei seguenti campi.

|Tipo| Nome| Descrizione|
---|---|---|
|Etichetta| tabellaTag| Identificatore tabella.|
|uint32| somma di controllo| Checksum per questa tabella.|
|Offset32| sfalsare| Offset dall'inizio del file del carattere.|
|uint32| lunghezza Lunghezza di questa tabella.|

Ogni tabella nel file di font OpenType è rappresentata da nomi noti come tag di tabella. È necessario che tutti i record nell'array siano ordinati in ordine crescente per tag.

## Riferimenti
* [Specifiche dei caratteri OpenType di Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [Panoramica TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

