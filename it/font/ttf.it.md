{
  "date" : "2020-08-20",
  "keywords" :[ "file ttf", "formato file ttf", "cos'è un file ttf", "file", "esempio ttf", "estensione file ttf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - Formato file font TrueType",
  "description":"I caratteri TrueType (TTF) si basano sulle specifiche della tecnologia dei caratteri digitali inizialmente progettate da Apple, Inc. Sia Apple che Microsoft utilizzavano TTF su sistemi operativi Mac e Windows.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Che cos'è un file TTF?

Un file con estensione .ttf rappresenta i file dei caratteri basati sulla tecnologia dei caratteri delle specifiche TrueType. Inizialmente è stato progettato e lanciato da Apple Computer, Inc per Mac OS e successivamente è stato adottato da Microsoft per Windows OS. I font TrueType forniscono la massima qualità di visualizzazione su schermi di computer e stampanti senza alcuna dipendenza dalla risoluzione. Tutte le moderne applicazioni che utilizzano i caratteri sono in grado di funzionare con i file TTF. I file di font TTF sono disponibili gratuitamente su Internet e possono anche essere convertiti in altri formati di file di font come OTF e WOFF.

## Breve storia

Progettato da Apply Computer, Inc negli anni '80 per MacOS, il formato del carattere TTF mirava a risolvere alcune limitazioni tecniche del formato Type 1 di Adobe. Apple ha incluso il supporto per i caratteri TrueType in Mac nel 1991. L'obiettivo di progettazione dietro i caratteri TTF era l'efficienza nell'archiviazione, nell'elaborazione e nell'estendibilità. Sulla base di questa estensibilità, i caratteri esistenti possono essere convertiti nel formato TrueType.

Microsoft ha utilizzato per la prima volta i caratteri TrueType in Windows 3.1 nell'aprile 1992 dopo che Apple ha accettato di concedere in licenza TrueType a Microsoft. Ha migliorato il meccanismo di rasterizzazione e ne ha migliorato l'efficienza e le prestazioni.

## Specifiche del formato file True Type

Un file di font TrueType è un file binario costituito da una sequenza di tabelle concatenate. Ogni tabella è una sequenza di parole e ha un nome noto come 'Tag'. Ciascun tag è di tipo dati uint32 ed è composto da quattro caratteri. La prima tabella nel file è la directory dei font che dà accesso ad altre tabelle nel file dei font. I dati dei caratteri sono contenuti in altre tabelle seguite dalla tabella della directory dei caratteri. Poiché ogni tabella è accessibile tramite il relativo tag, le tabelle possono essere visualizzate in qualsiasi ordine nel file.

Le tabelle richieste e i relativi nomi di tag sono mostrati nella tabella seguente.

|**Tag**|**Tabella**|
---|---|
|'cmap'| mappatura da carattere a glifo|
|'glifo'| dati glifo|
|'testa'| intestazione del carattere|
|'eh'| intestazione orizzontale|
|'hmtx'| metrica orizzontale|
|'località'| indice alla posizione|
|'maxp'| profilo massimo|
|'nome'| denominazione|
|'posta'| PostScript|

### Tipi di dati
I caratteri TrueType utilizzano il numero intero standard e tipi di dati aggiuntivi come elencato nella tabella seguente.

|**Tipo di dati** | **Descrizione** |
---|---|
|breve Frac| Frazione con segno a 16 bit|
|Risolto| Numero in virgola fissa con segno a 16,16 bit|
|FWord| Intero con segno a 16 bit che descrive una quantità in FUnits, la più piccola distanza misurabile nello spazio em.|
|uFWord| Intero senza segno a 16 bit che descrive una quantità in FUnits, la più piccola distanza misurabile nello spazio em.|
|F2Punto14| Numero fisso con segno a 16 bit con i 14 bit bassi che rappresentano la frazione.|
|longDateTime| Il formato interno lungo di una data in secondi dalla mezzanotte 12:00 del 1 gennaio 1904. È rappresentato come un intero a 64 bit con segno.|

### Directory dei caratteri

La prima tabella nel font TrueType è la directory dei font che fornisce l'accesso alle informazioni necessarie per accedere ai dati in altre tabelle. Si compone inoltre di:

* `Sottotabella offset` - tiene traccia delle tabelle nel carattere e fornisce informazioni sull'offset per accedere a ciascuna tabella nella directory
* `Table Directory` - Contiene voci per ogni tabella nel carattere

#### Sottotabella offset
La sottotabella offset è mostrata di seguito.

|**Tipo**|**Nome**|**Descrizione**|
---|---|---|
|uint32| tipo ablatore| Un tag per indicare lo scaler OFA da utilizzare per rasterizzare questo font; per ulteriori informazioni, vedere la nota sul tipo di ablatore di seguito.|
|uint16| numTabelle| numero di tabelle|
|uint16| intervallo di ricerca| (potenza massima di 2 <= numTables)*16|
|uint16| Selettore voci| log2(potenza massima di 2 <= numTables)|
|uint16| rangeShift| numTables*16-searchRange|

#### Directory della tabella
La directory della tabella arriva subito dopo la sottotabella offset. La sua struttura è quella mostrata nella tabella seguente.

|**Tipo**|**Nome**|**Descrizione**|
---|---|---|
|uint32| etichetta| Identificatore a 4 byte|
|uint32| checksum| checksum per questa tabella|
|uint32| sfalsare| offset dall'inizio di sfnt|
|uint32| lunghezza| lunghezza di questa tabella in byte (lunghezza effettiva non lunghezza imbottita)|

Ciascuna tabella in un file di font deve avere la propria voce di directory della tabella. Le voci in una tabella devono essere ordinate in ordine crescente per tag.


## Riferimenti
* [Manuale di riferimento dei caratteri TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [Panoramica TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

