{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "file", "estensione", "format", "cos'è un file amr", "music", "formato file amr", "file amr", "convert file amr to mp3", "riproduci file amr" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file AMR e le API che possono creare, convertire e aprire file AMR.",
  "title" :"AMR - File codec adattivo multi-rate",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## Che cos'è un file AMR?
Il file con estensione .amr è un formato di dati audio relativo al codec audio **Adaptive Multi-Rate**; consiste in un codec vocale a banda stretta multi-rate che codifica i segnali a banda stretta con una velocità in bit di 4,75-12,2 kbit/s con una qualità vocale a partire da 7,4 kbit/s; utilizza l'adattamento del collegamento per selezionare uno degli otto diversi bit rate basati.

## Formato file AMR
Il formato di file AMR utilizza molte tecniche di codifica, l'algoritmo ACELP (Algebraic Code Excited Linear Prediction) una delle migliori tecniche; progettato per comprimere l'audio parlato umano in modo più efficiente. L'AMR è stato impostato come codec vocale o vocale standard da 3GPP nel 1999. Il formato di file AMR viene utilizzato anche per memorizzare l'audio parlato utilizzando il codec audio **Adaptive Multi-Rate** utilizzato da molti smartphone per memorizzare le registrazioni discorsi.

### Struttura del formato file
L'AMR ( Adaptive Multi-Rate ) è un formato audio; ampiamente utilizzato in varie applicazioni e dispositivi mobili, tipicamente in lettori/registratori audio o in applicazioni di tipo VoIP. L'AMR può essere ulteriormente classificato come:

1. AMR-NB (banda stretta)
2. AMR-WB (banda larga)

Di solito, AMR si riferisce a AMR-NB. Il formato del file AMR ha la seguente struttura:

Ogni file AMR contiene un'intestazione di 6 byte che riconosce il file come audio AMR. Questa intestazione è sempre impostata su:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Questo di solito è simile a tutti i file AMR-NB. Se l'intestazione segue uno standard, è probabile che il file sia danneggiato e non debba essere utilizzato. il file AMR è costituito da un numero intero di frame di audio compressi. Ciascuno di questi fotogrammi compone 20 ms di audio. Ciascun frame può essere codificato utilizzando una qualsiasi delle modalità AMR-NB valide (0-7, 8 SID in modalità DTX). Poiché i frame possono essere codificati a velocità di trasmissione diverse, questo metodo tipico è chiamato Adaptive Multi-Rate (AMR).
#### Modalità AMR
Di seguito sono elencate le diverse modalità AMR e i relativi bitrate:

|MODALITÀ| TARIFFE BIT|
---|---|
|0| AMR 4.75 - Codifica a 4.75kbit/s|
|1 | AMR 5.15 - Codifica a 5.15kbit/s|
|2 | AMR 5.9 - Codifica a 5.9kbit/s|
|3 | AMR 6.7 - Codifica a 6.7kbit/s|
|4 | AMR 7.4 - Codifica a 7.4kbit/s|
|5 | AMR 7.95 - Codifica a 7.95kbit/s|
|6 | AMR 10.2 - Codifica a 10.2kbit/s|
|7 | AMR 12.2 - Codifica a 12.2kbit/s|

Di seguito sono riportate le dimensioni del frame delle modalità AMR in byte (incluso il byte di intestazione):

|CMR |MODO |DIMENSIONE FRAME( in byte )|
---|---|---|
|0 |AMR 4.75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## Riferimenti ##

* [codec audio Adaptive Multi-Rate - di Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [Formato payload RTP e formato di archiviazione file per codec audio AMR e AMR-WB](https://tools.ietf.org/html/rfc4867#page-35)

