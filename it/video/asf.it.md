{
  "date" : "2021-02-15",
  "keywords" :[ "file asf", "formato file asf", "cos'è un file asf", "file", "esempio asf", "estensione file asf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Formato file di sistemi avanzati",
  "description":"Scopri il formato di file ASF e le API che possono creare e aprire file ASF.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Che cos'è un file ASF?

Un file con estensione .asf è un formato di file multimediale per la memorizzazione e la riproduzione di flussi multimediali digitali sulla rete. È un formato di file contenitore che può avere contenuti sia video che audio per lo streaming online. Raramente troverai file ASF e più probabilmente ti imbatterai nei file Windows Media Audio ([WMA](/it/audio/wma/)) e Windows Media Video ([WMV](/it/video/wmv/)) che specificano entrambi i file ASF avere il contenuto codificato con i rispettivi codec. I file multimediali di Windows possono essere creati e letti utilizzando Windows Media Format SDK.

## Formato file ASF

Un file ASF può comprendere più flussi indipendenti o dipendenti. Ciò può includere più flussi audio per l'audio multicanale o più flussi video a velocità di trasmissione. I bitrate multipli rendono i flussi adatti alla trasmissione su diverse larghezze di banda. Inoltre, i flussi in un file ASF possono essere in formato compresso o non compresso. La migliore compressione si ottiene con i codec Microsoft Windows Media Audio e Video 9 Series. Le specifiche complete del formato di file ASF sono disponibili su [Sito Web Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Struttura dei file di primo livello ASF

I file ASF contengono logicamente tre tipi di oggetti di primo livello:

* `Header Object` - obbligatorio e deve essere posizionato all'inizio di ogni file ASF
* `Data Object` - obbligatorio e deve seguire l'oggetto header
* `Index Object(s)` - opzionale, ma utile per fornire un accesso casuale basato sul tempo ai file ASF

L'immagine seguente mostra la struttura dei file di primo livello dei file ASF.

![ASF File Structure](../asf.png "ASF File Structure")

#### Oggetto di intestazione di primo livello ASF

L'oggetto Header fornisce una nota sequenza di byte all'inizio dei file ASF e può contenere facoltativamente metadati come informazioni bibliografiche. Contiene tutte le informazioni necessarie per interpretare correttamente le informazioni all'interno dell'oggetto dati. L'oggetto Header può includere diversi oggetti standard inclusi, ma non limitati a:

* Oggetto Proprietà file - Contiene attributi di file globali.
* Stream Properties Object - Definisce un flusso multimediale digitale e le sue caratteristiche.
* Header Extension Object: consente di aggiungere funzionalità aggiuntive a un file ASF mantenendo la compatibilità con le versioni precedenti.
* Contenuto Descrizione Oggetto - Contiene informazioni bibliografiche.
* Oggetto comando script - Contiene comandi che possono essere eseguiti sulla timeline di riproduzione.
* Oggetto Marker - Fornisce punti di salto con nome all'interno di un file.

L'oggetto Header è rappresentato utilizzando la seguente struttura:

|Nome campo |Tipo campo |Dimensione (bit)|
---|---|---|
|ID oggetto| GUIDA| 128|
|Dimensioni oggetto| QWORD| 64|
|Numero di oggetti di intestazione| DWORD| 32|
|Riservato1| BYTE| 8|
|Riservato2| BYTE| 8|

#### Oggetto dati di primo livello ASF

Tutti i dati multimediali digitali per un file ASF sono contenuti nell'oggetto dati e vengono archiviati sotto forma di pacchetti di dati ASF. Ciascun pacchetto di dati ha una lunghezza fissa e contiene dati per uno o più flussi multimediali digitali.

#### Oggetti indice di primo livello ASF

Gli oggetti indice di primo livello ASF hanno i due tipi seguenti:

* `Simple Index Object` - Contiene un indice basato sul tempo dei dati video in un file ASF. L'intervallo di tempo tra le voci dell'indice è costante e viene memorizzato nell'oggetto Indice semplice.
* `Oggetto indice` - Si riferisce all'oggetto indice, all'oggetto indice oggetto multimediale e all'oggetto indice timecode, i cui formati sono simili. Come l'oggetto indice semplice, l'oggetto indice indicizza in base al tempo con un intervallo di tempo fisso ma non è limitato ai flussi video.

## Riferimenti

* [Formato file ASF - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [Formato file QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

