{
  "date" : "2021-02-10",
  "keywords" :[ "file jpx", "formato file jpx", "cos'è un file jpx", "file", "esempio jpx", "estensione file jpx", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Formato file immagine",
  "description":"Scopri il formato di file JPX e le API che possono creare e aprire file JPX.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Che cos'è un file JPX? ##

Un file con estensione .jpx è un'estensione del formato file JPEG 2000. Utilizza principalmente la compressione JPEG 2000 e fornisce anche funzionalità avanzate come livelli multipli per un'immagine, vari spazi colore, opacità e flussi di codice frammentati. JPX consente anche altre compressioni come JBIG, CCITT Group3, CCITT Group4, ecc. oltre alla compressione JPEG 2000. Il formato di file JPX è stato approvato come standard [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html), ma non ha potuto ricevere un'accoglienza calorosa a causa dell'ampio utilizzo di [JPEG ](/it/image/jpeg/). Le applicazioni che possono aprire file JPX includono Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 e CorelDraw Graphics Suite 2020.

## Breve storia

Nel 2000, il comitato del Joint Photographic Experts Group ha progettato JP2 con l'obiettivo di migliorare il proprio standard JPEG basato sulla trasformata del coseno discreto con questo nuovo metodo basato su wavelet. Il comitato JPEG mirava a fornire i propri metodi di base senza costi di licenza. Nella licenza JP2 guadagnando concorrenza tra 20 aziende, hanno vinto per un soffio. JPEG 2000 è stato dichiarato standard ISO, sebbene la maggior parte dei browser Web non sia pronta a dare una mano a JPEG 2000 dal 2017. Nel 2004, il formato ISO/IEC 15444-2 è stato pubblicamente accettato come estensione del formato di file JP2.

## Formato file JPX

Il formato di file JPX è stato formulato per soddisfare i requisiti delle applicazioni che necessitavano di strutture di dati oltre la funzionalità definita dal formato di file [JP2](/it/image/jp2/). Un file JP2 con estensioni non compatibili potrebbe creare confusione nel mercato in cui alcuni lettori possono interpretare alcuni file JP2 ma non altri. JPX è la risposta per evitare tali problemi nelle applicazioni.

### Identificazione del file

I file JPX vengono archiviati come [JPF](/it/image/jpf/) se archiviati nel tradizionale file system del computer. Ecco perché il termine JPX è meno comunemente usato rispetto al JPF. Un file JPX inizia con i seguenti byte:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Organizzazione dei file

Simile a JP2, un file JPX è una raccolta di scatole aventi una struttura binaria con le scatole disposte in un ordine contiguo. La prima casella dà inizio al file con il suo primo byte e l'ultimo byte dell'ultima casella rappresenta l'ultimo byte del file.
La struttura binaria di un box in un file JPX è identica a quella definita nel formato file [JP2](/it/image/jp2/).

### Archiviazione di CodeStream in JPX

Il formato di file JPX consente di dividere il codestream dell'immagine in frammenti. Ciò consente di modificare un singolo riquadro dell'immagine e di scrivere il riquadro modificato alla fine del file senza riscrivere l'intero file. Il formato di file originale [JP2](/it/image/jp2/) limita l'archiviazione dell'intero flusso di codice in una parte contigua del file, il che può essere problematico per le applicazioni di modifica delle immagini che potrebbero voler modificare un singolo riquadro dell'immagine e ottenere la supportabilità di cui sopra per il formato di file JPX. La frammentazione del codestream dell'immagine rende il formato di file JPX superiore al formato di file JP2. Inoltre, il formato di file JPX consente di combinare più codestream e produrre risultati di rendering. I codestream possono essere combinati come compositing e animazione.

## Riferimenti ##

* [Panoramica di JPEG 2000](https://jpeg.org/jpeg2000/)

