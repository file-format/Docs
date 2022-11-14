{
  "date" : "2019-10-11",
  "keywords" :[ "file j2k", "formato file j2k", "cos'è un file j2k", "file", "esempio j2k", "estensione file j2k", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"Scopri il formato di file J2K e le API che possono creare e aprire file J2K.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## Che cos'è un file J2K?

Un file **J2K** è un'immagine compressa utilizzando la compressione wavelet anziché la compressione DCT. Questo formato di file è utilizzato dai file del Joint Photographic Experts Group (JPEG) 2000. I file J2K memorizzano le informazioni sui metadati sul file di immagine in XML a differenza di .jpeg o .jpg che utilizzano il formato EXIF per questo scopo. I file J2K supportano il colore a 15 bit, la trasparenza alfa e la compressione senza perdita di dati. Esistono diverse API commerciali per decodificare immagini JPEG 2000 come J2K-Codec. Un file J2K può essere aperto sul sistema operativo Windows utilizzando i visualizzatori di immagini standard.

## Formato file J2K ##

Il formato del file J2K è lo stesso di JPEG 2000 che viene spesso salvato come .jp2 e .jpc. Ciò fa sì che i file J2K seguano lo stesso approccio di codifica dei metadati in formato XML in cui lo standard 12234-1 viene utilizzato come riferimento tra i tag Exif e i componenti XML. È ulteriormente migliorato dall'estensione JPEG 2000 parte-2 che combina il meccanismo di animazione e le configurazioni del flusso di codice in un'unica immagine. Tali file in formato file esteso vengono salvati come .jpx.

### Layout di un file JPEG2000 ###

JPEG2000 supporta una varietà di applicazioni basate sulla conformità per formati di file estensibili. Sebbene il tipo più semplice possa contenere una singola immagine, i tipi più complessi possono includere una serie di immagini, impilate l'una sull'altra o sequenziate in base al tempo.

#### Casella JP2 ####
È l'elemento costitutivo di primo livello del formato di file JP2 e contiene campi di tipo e lunghezza nell'intestazione e una sezione di dati. Il tipo più notevole di box è il box contiguo codestream. Questa casella memorizza nella sua sezione dati il codestream JPEG2000.

#### JPEG2000 CodeStream ####

Il CodeStream JPEG2000 è una sequenza di byte necessaria per decodificare l'immagine compressa JPEG2000. Nel caso in cui il file non abbia nient'altro che questo codestream, viene chiamato file codestream non elaborato. Di solito un codestream JPEG è l'applicazione dell'algoritmo di compressione JPEG2000 su un'immagine, sebbene non sia l'unico modo.

#### Parti di piastrelle ####

Un'immagine codificata JPEG2000 è una raccolta di unità di dati chiamate pacchetti. Questi pacchetti sono mantenuti nel codestream all'interno di gruppi di pacchetti chiamati tile-parts. Prima di codificare un'immagine, il codificatore divide l'immagine in una griglia rettangolare di blocchi, chiamati riquadri, in cui ogni riquadro è codificato separatamente indipendentemente dalle altre riquadri.

{{< figure src="../JPEG2000_Codestream.png" alt="Formato file JPEG2000" >}}

## Compressione J2K ##
JPEG 2000 utilizza la tecnologia di compressione wavelet che lo rende veloce in base al fatto che relativamente pochi pixel vengono mostrati in qualsiasi finestra o finestra in cui il visualizzatore visualizzi l'immagine. Ciò può essere enfatizzato dal fatto che sullo schermo appariranno solo pochi megabyte di pixel per immagini di dimensioni molto grandi (in gigabyte). Questo aiuta a recuperare e rendere rapidamente solo quella parte dei dati dell'immagine necessaria per popolare i pixel del display. Ciò richiede anche una tecnologia di decompressione ad alta velocità per accelerare il meccanismo di recupero delle immagini per creare le immagini richieste al volo.

J2K sfrutta la decompressione rapida e recupera solo le informazioni necessarie ai dati dei pixel per rendere rapidamente parte delle immagini visibili sugli schermi. J2K è progettato principalmente per la visualizzazione dei dati e non per la modifica.

## Identificazione J2K ##
I file JPEG 2000 hanno byte di firma 6A 50 20 20.

### Tipi di mimo ###
I tipi Mime registrati per i file JPEG 2000 includono:
* immagine/jp2
* immagine/jpx
* immagine/jpm
* video/mj2

## Miglioramenti rispetto allo standard JPEG ##
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

