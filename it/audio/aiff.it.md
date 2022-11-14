{
  "date" : "2021-04-26",
  "keywords" :[ "aiff", "file", "estensione", "formato", "formato file di interscambio audio", "musica", "formato file aiff", "aiff in mp3", "aiff vs wav", "converti aiff in mp3"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file AIFF e le API che possono creare, convertire e aprire file AIFF.",
  "title" :"AIFF - Formato file di scambio audio",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Che cos'è un file AIFF?
L'AIFF (Audio Interchange File Format) è un formato di file audio non compresso sviluppato da Apple nel 1998, ma si basa su **EA IFF 85** (Standard for Interchange Format Files sviluppato da Electronic Arts), un formato wrapper utilizzato sui sistemi Amiga . Questo formato di file presenta uno standard per la memorizzazione dei suoni campionati. Il formato è abbastanza buono in termini di flessibilità e consente la memorizzazione di suoni campionati mono o multicanale a varie frequenze di campionamento e larghezze di campionamento. Poiché i file AIFF non sono compressi, questa cosa li rende di dimensioni maggiori rispetto ad altri formati con perdita di dati come [MP3](https://docs.fileformat.com/audio/mp3/).

I file AIFF sono costituiti da 2 canali di audio stereo non compresso con una dimensione del campione di 16 bit, registrati a 44,1 kHz. A causa dell'elevata qualità dell'audio, un audio di 5 minuti può richiedere fino a 50 MB di spazio su disco, simile al formato di file [WAV](https://docs.fileformat.com/audio/wav/).

## AIFF vs WAV

L'AIFF e il WAV sono quasi gli stessi in termini di qualità. Entrambi utilizzano la stessa codifica PCM (pulse-code modulation), che li rende di dimensioni maggiori rispetto ad altri formati con perdita di dati, come [MP3](https://docs.fileformat.com/audio/mp3/), [M4A](). Alcune delle differenze generali sono riportate nella tabella seguente:

|AIFF|WAV|
---|---|
|Utilizzato principalmente per MAC|Utilizzato principalmente per PC|
|Consente metadeta| Non consente metadeta|

## Struttura del file AIFF

**EA IFF 85** stabilisce una struttura generale per la memorizzazione dei dati nei file. Un file **EA IFF 85** è costituito da una serie di blocchi di dati. Un blocco è un blocco di file AIFF costituito da alcune informazioni di intestazione seguite da dati:
{{< figure src="../chunk.png" alt="Pezzo AIFF" >}}

Un file AIFF è una raccolta di diversi tipi di blocchi. Esistono due tipi generali di blocchi che sono importanti per formare un blocco di file AIFF:
- **Common Chunk**: contiene parametri importanti che descrivono il suono campionato, come la sua lunghezza e frequenza di campionamento.
- **Sound Data Chunk**: contiene i campioni audio effettivi.
Ci sono molti altri blocchi opzionali che elencano i parametri dello strumento, definiscono i marker, memorizzano informazioni specifiche dell'applicazione, ecc.

### Tipi di blocchi locali

I tipi di blocchi per formare AIFF sono riportati nella tabella seguente:

|Tipo di pezzo| Descrizione|
---|---|
|Common Chunk|Il Common Chunk descrive i parametri fondamentali del suono campionato|
|Sound Data Chunk|Il Sound Data Chunk contiene i frame di esempio effettivi|
|Marker Chunk|Il Marker Chunk contiene marker che puntano a posizioni nei dati audio|
|Instrument Chunk|Lo Instrument Chunk definisce i parametri di base che uno strumento, come un campionatore, potrebbe utilizzare per riprodurre i dati del suono|
|MIDI Data Chunk|Il MIDI Data Chunk può essere utilizzato per memorizzare dati MIDI|
|Audio Recording Chunk|Audio Recording Chunk contiene informazioni relative ai dispositivi di registrazione audio|
|Application Specific Chunk|Il Application Specific Chunk può essere utilizzato per qualsiasi scopo dai produttori di applicazioni|
|Comments Chunk|Il Comments Chunk viene utilizzato per memorizzare i commenti nel FORM AIFF|
|Gruppi di testo: nome, autore, copyright, annotazione| Tutti sono frammenti di testo|

## Riferimenti ##

* [Formato file di interscambio audio - Di Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)

