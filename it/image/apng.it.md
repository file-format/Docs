{
  "date" : "2019-10-11",
  "keywords" :[ "file apng", "formato file apng", "cos'è un file apng", "file", "esempio apng", "estensione file apng", "estensione", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file APNG - File grafico di rete portatile animato",
  "description":"Scopri il formato di file APNG e le API che possono creare e aprire file APNG.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Che cos'è un file APNG?

Un file con estensione .apng (Animated Portable Network Graphics) è un formato grafico raster ed è un'estensione non ufficiale di Portable Network Graphic ([PNG](/it/image/png/) ). Comprende più fotogrammi (ciascuno di un'immagine PNG) che rappresenta una sequenza di animazione. Ciò fornisce una visualizzazione simile a un file [GIF](/it/image/gif/). I file APNG supportano immagini a 24 bit e trasparenza a 8 bit. APNG è compatibile con le versioni precedenti di file GIF non animati. I file APNG utilizzano la stessa estensione .png e possono essere aperti da applicazioni come Mozilla Firefox, Chrome con supporto APNG, app iMessage per iOS 10.

## Breve storia

* Le specifiche APNG sono state create nel 2004 per fornire supporto per le immagini PNG animate
* I decoder APNG sono stati sviluppati con dimensioni molto più ridotte e utilizzando il retro del decoder PNG
* Dopo continue deliberazioni, è stato formulato un nuovo tipo MIME image/apng mantenendo l'estensione uguale a .png invece di .apng
* APNG è stato ufficialmente rifiutato dal gruppo PNG il 20 aprile 2007 a causa della sua uniformità alle immagini PNG pur avendo specifiche diverse

## Formato file APNG

I file APNG vengono archiviati come file binari su disco e utilizzano le specifiche estese di PNG per le immagini animate. Il primo fotogramma di un file APNG è un normale flusso PNG leggibile dai decoder PNG per la visualizzazione. Il formato di file APNG segue le specifiche PNG e i dati vengono archiviati in segmenti chiamati blocchi. Tuttavia, APNG ha introdotto i seguenti nuovi blocchi:

`Animation Control Chunk (acTL)` - Indica che questo file è un file PNG animato anziché un normale file PNG. Agisce come un marker e viene prima del blocco IDAT. Contiene anche il numero di fotogrammi e informazioni sui tempi di ripetizione delle animazioni

`Frame Control Chunk` - Si verifica all'inizio di ogni e delle informazioni sui metadati come dimensioni, posizione, applicazione di trasparenza e informazioni di sostituzione con il fotogramma precedente o successivo una volta terminato.

`Frame Data Chunk` - Memorizza il contenuto del frame e inizia con un numero di sequenza. Questo numero di sequenza ha la stessa struttura del blocco IDAT dell'immagine predefinita.

{{< figure src="../APNG.png" alt="PNG animato - Formato file APNG" >}}

APNG è compatibile con le versioni precedenti di PNG poiché le specifiche del laterale sono state progettate in modo tale che un'applicazione che legge un file PNG dovrebbe semplicemente ignorare i blocchi che non comprende. Le specifiche relative a profondità di bit, tipo di colore, compressione, filtri, metodi di interlacciamento e informazioni sulla tavolozza vengono utilizzate come quelle del formato PNG predefinito.

## APNG vs GIF

Con GIF già in atto e utilizzato per un lungo periodo di tempo, potresti chiederti in che modo APNG è diverso da GIF. Di seguito è riportato un insieme di confronto tra APNG e GIF che fornisce una breve idea di entrambi i formati di file.

||APNG|GIF|
---|---|---|
|Pubblicato|2004|1987|
|Profondità colore|24 bit|8 bit|
|Frequenza fotogrammi|Illimitato|10 fotogrammi al secondo|
|Trasparenza|Completo e parziale|Completo|
|Compressione|Molto buono|Buono|

## Riferimenti

* [Formato file APNG](https://en.wikipedia.org/wiki/APNG)
* [Specifiche ufficiali del formato PNG](https://www.w3.org/TR/PNG/)

