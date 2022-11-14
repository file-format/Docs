{
  "date" : "2021-08-09",
  "keywords" :[ "file cso", "formato file cso", "cos'è un file cso", "file", "esempio cso", "estensione file cso", "estensione", "formato", "iso", "compressione DAX "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri il formato di file CSO e le API che possono creare e aprire file CSO.",
  "title" :"CSO - Immagine disco ISO compressa",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Che cos'è un file CSO?

Un file con estensione .cso è un file immagine ISO compresso. Il CSO è un'alternativa al metodo di compressione DAX; noto anche come CISO; è stato il primo metodo per comprimere i file [ISO](/it/compression/iso/) e di solito è un metodo preferito per archiviare materiale PlayStation Portable. Questo formato utilizza la compressione Sgonfia, che può includere fino a nove livelli di compressione. Software come Prometheus e YACC vengono utilizzati per creare le immagini.

## Formato file CSO

Il formato di file CSO è stato il primo metodo di compressione per ISO per risparmiare più spazio di memoria. I miglioramenti sono stati apportati di volta in volta per una migliore compressione. Il CSO utilizza la compressione Deflate con nove livelli di preimpostazioni, di solito ogni livello può gestire blocchi da 2 KiB individualmente. Mentre i livelli più alti di compressione possono rallentare e prolungare i tempi di caricamento del software che dipende fortemente dallo streaming del disco, anche i livelli più bassi possono eseguire una compressione sostanziale.

### Struttura del file CSO

Il formato di file CSO contiene un'intestazione a 24 byte, blocchi di dati e una tabella di indice. Little-endian è assunto per i campi più grandi di un byte. L'architettura endian di PlayStation Portable è riportata di seguito.

#### Intestazione

| Offset (byte) | Nome | Dimensione (byte) | Scopo |
----------|----------|--------------|---------|
| 0x0 | Magia | 4 | Sempre CISO o 0x4F534943 se letto come intero a 32 bit. Questo campo viene utilizzato per identificare un file CSO. Si noti che questo campo può essere diverso per gli altri derivati di CSO, ad esempio ZSO ha utilizzato il codice magico ZISO. |
| 0x4 | Dimensione intestazione | 4 | Per il formato di file CSO "v1" originale, questo campo viene ignorato e pertanto non è necessario che sia accurato. Tuttavia, il formato "v2" e ZSO richiedono che questo campo sia sempre 0x18 (24 byte). |
| 0x8 | Dimensioni non compresse | 8 | La dimensione dell'ISO originale non compresso in byte. |
| 0x10 | Dimensione blocco | 4 | La dimensione di ogni blocco di dati in byte prima della compressione. Solitamente 2048 byte, la stessa dimensione di ogni settore ISO 9660. |
| 0x14 | Versione | 1 | La versione del formato di file in uso. Per il formato "v1", il valore può essere 0 o 1. Per il formato "v2", deve essere 2. Inoltre, il formato ZSO richiede che sia 1. |
| 0x15 | Allineamento dell'indice | 1 | L'allineamento di ciascuna voce dell'indice, specificato in bit. |
| 0x16 | Riservato | 2 | Questo campo è inutilizzato. Nel formato "v1", questo campo viene ignorato e può contenere valori arbitrari. Nel formato "v2", questo campo deve essere zero. |

#### Tabella indice

La tabella dell'indice contiene diverse voci di 4 byte, che indicano la posizione di ciascun blocco di dati, e un'ultima voce aggiuntiva che punta alla fine del file.
Il contenuto di ogni voce è il seguente:
| bit | Lunghezza | Maschera | Nome | Scopo |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | Posizione | Questo campo, quando viene spostato a sinistra dall'allineamento dell'indice fornito nell'intestazione, emette la posizione in cui inizia il blocco di dati. |
| 31 | 1 | 0x80000000 | Tipo di compressione | Il formato ZSO ha una semantica simile, solo che 0 rappresenta LZ4 invece di Deflate. Nel formato "v2". Il blocco è implicitamente considerato non compresso se la dimensione del blocco è uguale o maggiore della dimensione del blocco specificata nell'intestazione del file. |

#### Blocchi di dati

I blocchi di dati comprendono i dati non compressi o compressi. La dimensione di un blocco viene calcolata ottenendo la sua posizione e quindi sottraendola dalla posizione del blocco successivo. Se l'allineamento dell'indice è maggiore di zero, è probabile che la dimensione del blocco sia maggiore dei dati in esso contenuti.


## Riferimenti

* [CSO - di Wikipedia](https://en.wikipedia.org/wiki/.CSO)


