{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "file", "estensione", "format", "che cos'è un file cue", "music", "formato file cue", "specifica del formato file cue", "cue sheet", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file CUE e le API che possono creare, convertire e aprire file CUE.",
  "title" :"CUE - File Cue Sheet",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Che cos'è un file CUE?

Un file con estensione .cue, noto anche come file cue sheet, è un file di metadati che contiene informazioni sul layout delle tracce su un CD o DVD. Questi sono supportati da lettori multimediali e applicazioni di creazione di dischi ottici. I principali dati audio memorizzati sul CD sono referenziati dal file cue, insieme alle specifiche della durata delle tracce, dei titoli dei dischi e degli esecutori. Pertanto, se un singolo file audio contiene più tracce, il file cue può essere utilizzato per dividere l'audio in più file o fare riferimento a varie tracce.

## Formato file CUE

I file CUE o cue sheet sono archiviati in un formato di testo semplice e leggibile. Le informazioni in un file cue sono comandi con uno o più parametri. Questi comandi si applicano all'intero file oa una singola traccia, a seconda del comando particolare e del contesto. La guida per l'utente di CDRWIN descrive le specifiche per la sintassi e la semantica del cue sheet.

## Comandi essenziali del foglio CUE

|Comando|Descrizione|
---|---|
|FILE| Si riferisce al file contenente i dati e al relativo formato, ad esempio [MP3](/it/audio/mp3/), [WAV](/it/audio/wav/), o un'immagine disco binario semplice)|
|TRACCIA| Definisce le informazioni sul contesto della traccia come il numero e il tipo o la modalità.|
|INDICE| Rappresenta la posizione come indice all'interno del FILE. Il formato è mm:ss:ff (fotogramma minuto-secondo).|
|PREGAP e POSTGAP|Indica il pregap o il post-gap di una traccia, che non è memorizzata in nessun file di dati. La lunghezza è specificata nello stesso formato fotogramma minuto-secondo come per INDEX.|

### Esempio di foglio CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Riferimenti

* [file .cda - di Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

