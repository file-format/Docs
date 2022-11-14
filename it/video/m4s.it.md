{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File M4S - Che cos'è un file M4S?",
  "description":"Scopri il formato di file M4S e le API che possono creare e aprire file M4S.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Che cos'è un file M4S?

Un file M4S è un piccolo segmento di un video trasmesso in streaming su Internet utilizzando la tecnica di streaming **MPEG-DASH**. Contiene un segmento video sotto forma di dati binari. L'applicazione ricevente (solitamente un browser Web o lettori multimediali) riproduce questi segmenti nell'ordine in cui vengono ricevuti. Il primo segmento M4S è identificato dai dati di inizializzazione che contiene. In **riepilogo**, i file M4S sono piccoli segmenti multimediali individuali di un file completo.

## Formato file M4S

I file M4S sono basati sul [formato ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Questi piccoli segmenti di un file di grandi dimensioni possono essere scaricati indipendentemente tramite HTTP. Pertanto, se si dispone di un file filmato [MP4](/it/video/mp4/) di grandi dimensioni, è possibile riprodurlo in streaming utilizzando la tecnica MPEG-DASH (Dynamic Adaptive Streaming over HTTP) segmentandolo come file di segmento M4S. Se questo file di film di grandi dimensioni viene scaricato su disco come M4S, vengono scaricati più file M4S. Se tutti questi segmenti .m4s sono concatenati, viene prodotto un file riproducibile completo. I lettori multimediali non possono riprodurre il file a meno che il primo segmento di inizializzazione non sia disponibile anche con il file.

## Informazioni sullo streaming MPEG-DASH

MPEG-DASH utilizza una tecnica di streaming adattivo con bitrate che rende possibile lo streaming di contenuti multimediali di alta qualità su Internet. Questo viene fatto suddividendo il contenuto in una sequenza di piccoli segmenti che vengono trasmessi in streaming su HTTP. In questo modo è possibile eseguire lo streaming di file multimediali di grandi dimensioni come film, podcast o trasmissioni in diretta di un evento sportivo. Questi segmenti sono codificati a velocità di trasmissione diverse. I lettori multimediali abilitati per MPEG-DASH selezionano automaticamente il segmento con il bit rate più alto utilizzando un algoritmo di adattamento del bit rate. Ciò evita lo stallo o il re-buffering degli eventi nella riproduzione.

### API open source per file M4S

Sono disponibili API open source che possono essere utilizzate per leggere e convertire file M4S.

* [libdash](https://github.com/bitmovin/libdash) - API .NET per file M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - Client Javascript per file M4S
* [Vai alla libreria per la creazione di file Dash](https://github.com/zencoder/go-dash)

### API open source per convertire M4S in MP4

* [MfourStoMp4](https://github.com/muri11o/mfourstomp4)

## Riferimenti ###

* [Formato ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Streaming dinamico adattivo su HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

