{
  "date" : "2021-04-08",
  "keywords" :[ "file lz", "formato file lz", "cos'è un file lz", "file", "esempio lz", "estensione file lz", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Formato file compresso Lzip",
  "description":"Scopri il formato di file LZ e le API che possono creare e aprire file LZ.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Che cos'è un file LZ?

Un file con estensione .lz è un file di archivio compresso creato con Lzip, che è uno strumento gratuito da riga di comando per la compressione. Supporta la concatenazione per comprimere i file di supporto. I file LZ hanno il tipo di supporto application/lzip e supportano rapporti di compressione più elevati rispetto a [BZ2](/it/compression/bz2). LZ si basa sull'algoritmo LZMA (catena Lempel-Ziv-Markov) e include un checksum CRC a 32 bit e byte ident per controllare l'integrità del file.

## Formato compresso LZMA

Il formato compresso LZMA è costituito da un flusso compresso di bit codificato utilizzando un codificatore di intervallo binario adattivo. Il flusso è suddiviso in pacchetti. Ciascun pacchetto descrive un singolo byte o una sequenza LZ77. La lunghezza e la distanza di ciascun pacchetto è codificata in modo implicito o esplicito.

I sette tipi di pacchetti sono i seguenti ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Codice compresso (sequenza di bit) |Nome del pacchetto |Descrizione del pacchetto|
---|---|---|
|0 + byteCodice| LIT| Un singolo byte codificato utilizzando un codificatore di intervallo binario adattivo.|
|1+0 + lente + dist| PARTITA| Una tipica sequenza LZ77 che descrive la lunghezza e la distanza della sequenza.|
|1+1+0+0| SHORTREP| Una sequenza LZ77 a un byte. La distanza è uguale all'ultima distanza LZ77 utilizzata.|
|1+1+0+1 + lente| LONGREP[0]| Una sequenza LZ77. La distanza è uguale all'ultima distanza LZ77 utilizzata.|
|1+1+1+0 + lente| LONGREP[1]| Una sequenza LZ77. La distanza è uguale alla penultima distanza LZ77 utilizzata.|
|1+1+1+1+0 + lente| LONGREP[2]| Una sequenza LZ77. La distanza è uguale alla terzultima distanza LZ77 utilizzata.|
|1+1+1+1+1 + lente| LONGREP[3]| Una sequenza LZ77. La distanza è uguale alla penultima distanza LZ77 utilizzata.|


## Riferimenti

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

