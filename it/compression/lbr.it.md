{
  "date" : "2021-04-08",
  "keywords" :[ "file mst", "formato file mst", "cos'è un file mst", "file", "esempio mst", "estensione file mst", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU Library Archive File Format",
  "description":"Scopri il formato di file LBR e le API che possono creare e aprire file LBR.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Che cos'è un file LBR?

Un file con estensione .lbr è un file di archivio creato con il programma LU e utilizzato su sistemi operativi CP/M e DOS negli anni '80. Non viene più utilizzato ed è stato sostituito dai moderni formati di file di archiviazione. Il formato non comprime i file membri e funge da archivio contenitore per questi. La funzione di archiviazione è stata utilizzata principalmente per il trasferimento di file archiviati su Internet. Poiché LBR non offriva la compressione, sono state utilizzate altre utilità come SQ o CRUNCH per comprimere i file membri prima dell'archiviazione o il file di archivio risultante dopo l'archiviazione per ridurne le dimensioni.

## Formato file LBR

Il formato di file LBR è stato progettato da Gary P. Novosielski e non ha dettagli tecnici disponibili pubblicamente. I file LBR iniziano con un byte 0x00, seguito da 11 spazi (0x20), quindi due byte 0x00, quindi due byte che non sono entrambi 0x00. Essendo un formato di file contenitore, può essere estratto utilizzando LU.COM e NULU.COM.

## Riferimenti

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))

