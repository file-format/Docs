{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Formato file immagine disco",
  "description":"Cos'è un file ISO e le API che possono creare e aprire file ISO.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Che cos'è un file ISO?

Un file con estensione .iso è un file immagine disco di archivio non compresso che rappresenta il contenuto di interi dati su un disco ottico come CD o DVD. Basato sullo standard [ISO-9660](https://www.iso.org/standard/17505.html), il formato del file immagine ISO contiene i dati del disco insieme alle informazioni sul filesystem in esso memorizzate. La capacità dei file ISO di contenere una replica esatta del contenuto lo rende il tipo di file perfetto per la creazione di copie di CD/DVD e viene utilizzato principalmente per archiviare dati avviabili per l'installazione. La maggior parte delle volte, i file ISO vengono masterizzati su USB/CD/DVD come contenuto avviabile per avviare la macchina per l'installazione. I file ISO hanno applicazione di tipo MIME/immagine-x-iso9660.

## Formato file ISO

Il formato di file ISO non è come altri formati di file di file contenitore sebbene archivi il contenuto dei dati specificato. L'archivio viene creato come file binario con la struttura esatta del contenuto e delle informazioni sul filesystem. Il formato del file ISO è descritto da [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) come segue.

### Struttura di primo livello del file ISO

La struttura complessiva del file è composta da:

* 'Area di sistema' - 32.768 byte e non è utilizzata da ISO_9660
* 'Area dati' - consiste in un insieme di descrittori di volume e tabelle di percorsi, directory e file

### Descrittore volume impostato

L'area dati inizia con il set di descrittori di volume, un set di uno o più descrittori di volume terminato con un terminatore di set di descrittori di volume. Questi agiscono collettivamente come un'intestazione per l'area dati, descrivendone il contenuto (simile al blocco di parametri BIOS utilizzato dai dischi formattati FAT, HPFS e NTFS).

Un set di descrittori di volume è come mostrato di seguito.

|Set di descrittori di volume|
---|
|Descrittore di volume n. 1|
|...|
|Descrittore di volume #N|
|Descrittore volume imposta terminatore|

#### Descrittore del volume

Ogni descrittore di volume ha una dimensione di 2048 byte e ha la struttura seguente:

|Parte |Tipo |Identificatore |Versione |Dati|
---|---|---|---|---|
|Dimensione |1 byte |5 byte (sempre 'CD001') |1 byte (sempre 0x01) |2.041 byte|

## Riferimenti

* [Immagine disco ottico - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Firme dei file](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

