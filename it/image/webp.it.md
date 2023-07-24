{
  "date" : "2019-10-11",
  "keywords" :[ "file webp", "formato file webp", "cos'è un file webp", "file", "esempio webp", "estensione file webp", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Formato file immagine raster Google",
  "description":"Scopri il formato di file WEBP e le API che possono creare e aprire file WEBP.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file WEBP?

WebP, introdotto da Google, è un moderno formato di file di immagini web raster basato sulla compressione lossless e lossy. Fornisce la stessa qualità dell'immagine riducendo notevolmente le dimensioni dell'immagine. Poiché la maggior parte delle pagine Web utilizza le immagini come rappresentazione efficace dei dati, l'utilizzo di immagini WebP nelle pagine Web determina un caricamento più rapido delle pagine Web. Secondo Google, le immagini con perdita di dati WebP sono di dimensioni inferiori del 26% rispetto a [PNG](/it/image/png/), mentre le immagini con perdita di dati WebP sono più piccole del 25-34% rispetto alle immagini [JPEG](/it/image/jpeg/) comparabili. Le immagini vengono confrontate in base all'indice di somiglianza strutturale (SSIM) tra WebP e altri formati di file immagine. WebP è un progetto gemello del formato contenitore multimediale [WebM](https://en.wikipedia.org/wiki/WebM).

## Panoramica delle funzionalità di WebP ##

Le immagini WebP utilizzano il processo di compressione basato sulla previsione dei pixel dai blocchi circostanti, risultando in pixel da utilizzare più volte in un unico file. Supporta le immagini animate e dovrebbe supportare più funzionalità in futuro. Google ha messo a disposizione il codice sorgente [online](https://developers.google.com/speed/webp/download) per il proprio codificatore e decoder così da poter essere utilizzato dove richiesto. L'immagine WebP fornisce supporto per:

* **Compressione con perdita di dati:** La compressione con perdita di dati si basa sulla codifica del fotogramma chiave [VP8](https://en.wikipedia.org/wiki/VP8). VP8 è un formato di compressione video creato da On2 Technologies come successore dei formati VP6 e VP7.
* **Compressione senza perdita di dati:** Il formato di compressione senza perdita di dati è sviluppato dal team WebP.
* **Trasparenza:** il canale alfa a 8 bit è utile per le immagini grafiche. Il canale Alpha può essere utilizzato insieme all'RGB con perdita, una funzionalità attualmente non disponibile con nessun altro formato.
* **Animazione:** Supporta immagini animate a colori reali.
* **Metadati:** potrebbero avere metadati EXIF e XMP (utilizzati dalle fotocamere, ad esempio).
* **Profilo colore:** Potrebbe avere un profilo ICC incorporato.

La compressione Lossy WebP utilizza la codifica predittiva per codificare un'immagine, lo stesso metodo utilizzato dal codec video VP8 per comprimere i fotogrammi chiave nei video. La codifica predittiva utilizza i valori nei blocchi di pixel adiacenti per prevedere i valori in un blocco, quindi codifica solo la differenza.

La compressione WebP senza perdita di dati utilizza frammenti di immagine già visti per ricostruire esattamente nuovi pixel. Può anche utilizzare una tavolozza locale se non viene trovata alcuna corrispondenza interessante.

## Formato del file ##

Il formato di file WebP è basato sul formato di documento RIFF (resource interchange file format). Il contenitore WebP fornisce supporto per funzionalità superiori a quelle che contengono solo una singola immagine codificata come fotogramma chiave VP8. L'elemento base di un file RIFF è un pezzo che consiste in:


|Campo|Descrizione
---|---|
|Chunk FourCC: 32 bit|Codice ASCII a quattro caratteri utilizzato per l'identificazione dei blocchi
|Dimensione del blocco: 32 bit (uint32)|La dimensione del blocco non include questo campo, l'identificatore del blocco o il riempimento
|Chunk Payload: Chunk Size byte|Il carico utile dei dati. Se Chunk Size è dispari, viene aggiunto un singolo byte di riempimento ~-~- che dovrebbe essere 0 ~-~-
|ChunkHeader ('ABCD')|Utilizzato per descrivere l'intestazione FourCC e Chunk Size di singoli blocchi, dove 'ABCD' è il FourCC per il blocco. La dimensione di questo elemento è di 8 byte.

### Intestazione WebP ###

Un'intestazione di file WebP è la seguente:

* Intestazione RIFF - 32 bit che rappresentano i caratteri ASCII 'R' 'I' 'F' 'F'
* Dimensione file - 32 bit (uint32) che rappresentano la dimensione del file in byte a partire dall'offset 8. Il valore massimo di questo campo è 2^32 meno 10 byte e quindi la dimensione dell'intero file è al massimo 4GiB meno 2 byte .
* 'WEBP' - 32 bit che rappresentano i caratteri ASCII 'W' 'E' 'B' 'P'

### Formato file con perdita di dati ###

Le immagini WebP utilizzano il formato file con perdita di dati se l'immagine è basata su una codifica con perdita di dati e non richiede alcuna funzionalità avanzata/estesa come trasparenza, animazione, alfa, ecc. Le immagini con perdita di dati sono più piccole e sono supportate anche dalle applicazioni precedenti.

Il file WebP, in questo caso, è composto da:

* 12 byte di intestazione del file WebP
* Pezzo VP8

La [Guida al formato e alla decodifica dei dati VP8](https://tools.ietf.org/html/rfc6386) illustra le specifiche del formato bitstream VP8.

### Formato file senza perdita di dati ###

Questo layout viene utilizzato quando l'immagine è basata su una codifica lossless e non sono necessarie le funzionalità avanzate fornite dal formato esterno. Tuttavia, le applicazioni precedenti potrebbero non essere in grado di leggere tali file.

Il file WebP, in questo caso, è composto da:

* 12 byte di intestazione del file WebP
* Pezzo VP8L

## Riferimenti ##

* [Riferimento per sviluppatori WebP - Di Google](https://developers.google.com/speed/webp/)
* [Formato file WebP - Di Wikipedia](https://en.wikipedia.org/wiki/WebP)

