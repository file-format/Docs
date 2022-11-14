{
  "date" : "2019-10-11",
  "keywords" :[ "file bz2", "formato file bz2", "cos'è un file bz2", "file", "esempio bz2", "estensione file bz2", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Formato file compresso",
  "description":"Scopri cos'è un file BZ2 e le API che possono creare e aprire file BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Che cos'è un file BZ2?

BZ2 sono file compressi generati utilizzando il metodo di compressione open source [BZIP2](http://www.bzip.org/), principalmente su sistemi UNIX o Linux. Viene utilizzato per la compressione di un singolo file e non è pensato per l'archiviazione di più file. Ciò è in contrasto con il formato di file TAR sulle stesse piattaforme che archivia più file in un unico file ma senza compressione. I file compressi come BZ2 possono essere decompressi con applicazioni come [WinZip](https://www.winzip.com/win/en/). BZIP2 utilizza l'algoritmo di compressione Run-Length Encoding (RLE) o [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) per ottenere livelli elevati di compressione.

## Formato file BZ2

Non sono disponibili specifiche formali per questo formato di file. Tuttavia, un [specifiche di ingegneria inversa] non ufficiale (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) mostra che un flusso .bz2 è costituito da un'intestazione di 4 byte che viene seguita da zero o più blocchi compressi. È immediatamente seguito da un marker di fine flusso contenente un CRC a 32 bit per l'intero flusso di testo normale elaborato. Non c'è riempimento tra i blocchi compressi e tutti i blocchi sono allineati ai bit.

## Decomprimi/estrai file BZ2

Puoi decomprimere un file BZ2 su Windows e Mac OS utilizzando un software come WinZip. Su Linux, il seguente comando nel terminale.

```
bzip2 -d filename.bz2
```

## Riferimenti

* [Specifiche del formato BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

