{
  "date" : "2019-10-11",
  "keywords" :[ "file j2c", "formato file j2c", "cos'è un file j2c", "file", "esempio j2c", "estensione file j2c", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Scopri il formato di file J2C e le API che possono creare e aprire file J2C.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Che cos'è un file J2C?

Un file con estensione .j2c è una variante del formato di file JPEG ed è compresso con la compressione wavelet. Ha un sistema di marcatori e segmenti quasi identico al formato di file JPEG 2000. Il formato di file J2C è quello definito nella Parte 1 del supporto JPEG 2000 che supporta la compressione sia con perdita che senza perdita di dati. Il codestream JPEG 2000 è stato progettato per essere incorporato in [JP2](/it/image/jp2/) o in un altro formato di file, sebbene possa apparire in un file da solo. Un file J2C può essere aperto utilizzando Adobe Photoshop 2020, Adobe Illustrator 2020 e Corel Paintshop Pro.

## Formato file J2C

Il formato del file J2C è lo stesso di JPEG 2000 che viene spesso salvato come .jp2 e .jpc. Ciò fa sì che i file J2C seguano lo stesso approccio di codifica dei metadati in formato XML in cui lo standard 12234-1 viene utilizzato come riferimento tra i tag Exif e i componenti XML. È ulteriormente migliorato dall'estensione JPEG 2000 parte-2 che combina il meccanismo di animazione e le configurazioni del flusso di codice in un'unica immagine. Tali file in formato file esteso vengono salvati come [.jpx](/it/image/jpx/).

### Layout di un file JPEG2000

JPEG2000 supporta una varietà di applicazioni basate sulla conformità per formati di file estensibili. Sebbene il tipo più semplice possa contenere una singola immagine, i tipi più complessi possono includere una serie di immagini, impilate l'una sull'altra o sequenziate in base al tempo.

#### Scatola JP2
È l'elemento costitutivo di primo livello del formato di file JP2 e contiene campi di tipo e lunghezza nell'intestazione e una sezione di dati. Il tipo più notevole di box è il box contiguo codestream. Questa casella memorizza nella sua sezione dati il codestream JPEG2000.

#### JPEG2000 CodeStream

Il CodeStream JPEG2000 è una sequenza di byte necessaria per decodificare l'immagine compressa JPEG2000. Nel caso in cui il file non abbia nient'altro che questo codestream, viene chiamato file codestream non elaborato. Di solito un codestream JPEG è l'applicazione dell'algoritmo di compressione JPEG2000 su un'immagine, sebbene non sia l'unico modo.

#### Parti di piastrelle ####

Un'immagine codificata JPEG2000 è una raccolta di unità di dati chiamate pacchetti. Questi pacchetti sono mantenuti nel codestream all'interno di gruppi di pacchetti chiamati tile-parts. Prima di codificare un'immagine, il codificatore divide l'immagine in una griglia rettangolare di blocchi, chiamati riquadri, in cui ogni riquadro è codificato separatamente indipendentemente dalle altre riquadri.

{{< figure src="../JPEG2000_Codestream.png" alt="Formato file JPEG2000" >}}

## Compressione J2C
JPEG 2000 utilizza la tecnologia di compressione wavelet che lo rende veloce in base al fatto che relativamente pochi pixel vengono mostrati in qualsiasi finestra o finestra in cui il visualizzatore visualizzi l'immagine. Ciò può essere enfatizzato dal fatto che sullo schermo appariranno solo pochi megabyte di pixel per immagini di dimensioni molto grandi (in gigabyte). Questo aiuta a recuperare e rendere rapidamente solo quella parte dei dati dell'immagine necessaria per popolare i pixel del display. Ciò richiede anche una tecnologia di decompressione ad alta velocità per accelerare il meccanismo di recupero delle immagini per creare le immagini richieste al volo.

J2C sfrutta la decompressione rapida e recupera solo le informazioni necessarie ai dati dei pixel per rendere rapidamente parte delle immagini visibili sugli schermi. J2C è progettato principalmente per la visualizzazione dei dati e non per la modifica.

## Identificazione J2C
I file JPEG 2000 hanno byte di firma `FF 4F FF 51`.

### Tipi di mimo
I tipi Mime registrati per i file JPEG 2000 includono:
* immagine/j2c
* immagine/jpx
* immagine/jpm
* video/mj2

## Miglioramenti rispetto allo standard JPEG
I miglioramenti rispetto allo standard JPEG includono:
* Prestazioni di compressione superiori
* Rappresentazione a risoluzione multipla
* Trasmissione progressiva per pixel e precisione della risoluzione
* Scelta di compressione lossless o lossy
* Resilienza agli errori, formato file flessibile
* Supporto ad alta gamma dinamica
* Informazioni spaziali del canale laterale

## Riferimenti ##
* [Taubman, David; Marcellino, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

