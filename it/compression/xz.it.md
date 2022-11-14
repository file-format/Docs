{
  "date" : "2022-01-23",
  "keywords" :[ "file xz", "formato file", "cos'è un file xz", "file", "esempio xz", "estensione file xz", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File XZ - Archivio compresso XZ",
  "description":"Scopri il formato di file XZ e le API che possono creare e aprire file XZ.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Che cos'è un file XZ?

XZ è un formato di file compresso che utilizza l'algoritmo di compressione LZMA2. È stato progettato come sostituto dei popolari formati gzip e bzip2 e offre numerosi vantaggi rispetto a questi standard precedenti. I file XZ sono ben supportati su molte piattaforme e possono essere decompressi rapidamente e facilmente. Sebbene non siano comuni come i file [ZIP](/it/compression/zip/) o [RAR](/it/compression/rar/), gli archivi XZ possono essere utilizzati per archiviare grandi quantità di dati senza sacrificare la qualità della compressione. Se è necessario comprimere o decomprimere file di grandi dimensioni, vale la pena considerare l'estensione del file XZ.

## Formato file XZ

I file XZ vengono generati e salvati come file binari su disco. Utilizza l'algoritmo LZMA per comprimere i dati e può raggiungere un rapporto di compressione fino al 50%. I file XZ vengono in genere utilizzati per le distribuzioni di software e gli archivi di backup. Possono essere decompressi utilizzando l'utilità XZ, inclusa nella maggior parte delle distribuzioni Linux.

## Decomprimi i file XZ su Linux/Unix

Per decomprimere i file XZ, installa prima il pacchetto `xz-utils`:
```
$ sudo apt-get install xz-utils
```

Usa il comando `unxz` per estrarre i file .xz:
```
$ unxz compressed_xz_file.xz
```

o usando con l'opzione --decompress di XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Riferimenti

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)

