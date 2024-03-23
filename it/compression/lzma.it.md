{
  "date" : "2021-04-08",
  "keywords" :[ "file lzma", "formato file lzma", "cos'è un file lzma", "file", "esempio lzma", "estensione file lzma", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZMA - Formato file compresso LZMA",
  "description":"Cos'è un file LZMA e le API che possono creare e aprire file LZMA.",
  "linktitle" : "LZMA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-18"
}

## Che cos'è un file LZMA?

Un file con estensione .lzma è un file di archivio compresso creato utilizzando il metodo di compressione LZMA (Algoritmo della catena Lempel-Ziv-Markov). Questi si trovano/usano principalmente sul sistema operativo Unix e sono simili ad altri algoritmi di compressione come [ZIP](/it/compression/zip/) per ridurre al minimo le dimensioni del file. LZMA è un formato di file legacy, che è stato o è stato sostituito dal formato .xz. Il tipo MIME del formato .lzma è \`application/x-lzma'. Questo formato di file è stato progettato da Igor Pavlov per l'uso in LZMA SDK.

## Formato file LZMA

Il file LZMA è composto da due parti principali:

1. Intestazione
1. Dati compressi


### Intestazione LZMA

I file LZMA hanno un'intestazione di 13 byte seguita dai dati compressi LZMA. L'intestazione LZMA è composta da:

* Proprietà
* Dimensione del dizionario
* Dimensioni non compresse

#### Proprietà dell'intestazione LZMA

Il campo Proprietà contiene tre proprietà. Tra parentesi viene fornita un'abbreviazione, seguita dall'intervallo di valori della proprietà. Il campo è composto da

1) il numero di bit di contesto letterali (lc, [0, 8]);
2) il numero di bit di posizione letterali (lp, [0, 4]); e
3) il numero di bit di posizione (pb, [0, 4]).

#### Dimensione del dizionario LZMA

Viene memorizzato come intero little endian a 32 bit senza segno con valori compresi tra 2^n e 2^n + 2^(n-1). LZMA Utils può decomprimere file con qualsiasi dimensione del dizionario.

#### Dimensioni non compresse
La dimensione non compressa viene archiviata come intero little endian a 64 bit senza segno. Un valore speciale di 0xFFFF_FFFF_FFFF_FFFF indica che la dimensione non compressa è sconosciuta. Il valore è rappresentato da End of Payload Marker (\*) se e solo se la dimensione non compressa è sconosciuta.

## Riferimenti

* [Algoritmo della catena Lempel–Ziv–Markov](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)

