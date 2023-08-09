{
  "date" : "2019-10-11",
  "keywords" :[ "file mov", "formato file mov", "che cos'è un file mov", "file", "esempio mov", "estensione file mov", "estensione", "formato", "QuickTime", "MPEG- 4"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File MOV - Formato file filmato Apple QuickTime",
  "description":"Scopri il formato di file MOV e le API che possono creare e aprire file MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Che cos'è un file MOV?

Un file MOV è un tipo di file video, sviluppato da Apple Inc., che contiene una o più tracce. Ogni traccia memorizza un filmato, audio, clip filmato e sottotitoli. È un contenitore multimediale che può contenere diversi tipi di elementi multimediali. Il formato video MOV è compatibile con i sistemi Windows e Macintosh. Utilizza la codifica MPEG-4 per la compressione e le tracce sono mantenute in oggetti chiamati atomi che sono inseriti in una struttura di dati gerarchica.

## Breve storia del formato di file MOV

Il formato di file MPEG-4 si è evoluto dalla specifica QuickTime File Format (**QTFF**) nel 2001. L'Organizzazione internazionale di standardizzazione ha approvato il formato e le specifiche di sistema MPEG-4 Part 1 sono state pubblicate nel 1999. Nel 2001, un file di revisione è stato pubblicato il formato [MP4](/it/video/mp4/).

La prima versione di MP4 è stata rivista nel 2003 come MPEG-4 Part 14 (ISO/IEC 14496-14:2003). Nel 2004, MP4 è stato generalizzato per definire una struttura generale per tutti i file multimediali basati sul tempo. Pertanto, ora viene utilizzato come base per vari altri formati di file multimediali.

## Formato file QuickTime (QTFF) - Ulteriori informazioni

Per lavorare con i contenuti multimediali digitali, QTFF può contenere molti tipi di dati. È un formato ideale per lo scambio di media digitali poiché definisce gli standard per descrivere qualsiasi tipo di struttura dei media. Il formato del file consiste in una raccolta flessibile di oggetti orientati agli oggetti. Per l'archiviazione di filmati su dischi, QuickTime utilizza due strutture, ovvero `atoms` e `QT atoms`.

### Atomi

Atom è l'unità di base del file QuickTime. Ci sono due campi principali in ogni atomo prima di qualsiasi altro campo: i campi Dimensione e Tipo. Il campo della dimensione mostra la dimensione dell'atomo mentre il campo del tipo indica il tipo di dati memorizzati nell'atomo. Per natura, gli atomi sono gerarchici, il che significa che un atomo può contenere altri atomi che possono comunque contenerne altri. Il layout di un atomo campione è mostrato nell'immagine seguente.

Ogni atomo ha due parti, 'header' e 'data'. L'intestazione contiene i campi di dimensione e tipo e la parte di dati contiene i dati effettivi. Inoltre, ogni campo è spiegato di seguito:

### Dimensione dell'atomo

L'intestazione e il contenuto dell'atomo sono indicati da un numero intero a 32 bit noto come dimensione dell'atomo. Il campo size contiene la dimensione dell'atomo in byte, espressa in un intero senza segno a 32 bit.

### Tipo di atomo

Il tipo dell'atomo è mostrato anche da un numero intero a 32 bit, che è per lo più trattato come un campo di quattro caratteri con valore knemonico, come 'moov' (0x6D6F6F76) per un atomo di film, o 'trak' (0x7472616B) per un atomo di traccia. Una volta che il tipo di atomo è noto, consente di interpretare i suoi dati.

### Atomi QT e contenitori di atomi

Gli atomi QT forniscono un formato di archiviazione per uso generico e hanno un'intestazione estesa composta da campi Dimensione, Tipo, ID Atom e Conteggio di atomi figlio. Gli atomi QT sono racchiusi in un contenitore di atomi, una struttura di dati univoca con un'intestazione con un conteggio di blocco. C'è un atomo radice in ogni contenitore di atomi che è l'atomo QT. Il layout dell'atomo QT è mostrato nella figura seguente.

L'intestazione del contenitore dell'atomo QT ha i seguenti dati:

Riservato: un elemento a 10 byte con un valore di 0.

Conteggio blocchi: intero a 16 bit con valore 0.

Le intestazioni degli atomi QT hanno i seguenti dati:

**Dimensione -** L'intestazione e il contenuto dell'atomo QT sono indicati in byte da un numero intero a 32 bit. Nel caso di un atomo foglia, questo campo contiene la dimensione di un singolo atomo.

**Tipo -** Il tipo dell'atomo è indicato da un numero intero a 32 bit. Nel caso in cui sia l'atomo radice, il valore è impostato su 'sean'.

**ID Atom -** È un numero intero a 32 bit che mostra l'ID Atom e deve essere univoco per tutti i fratelli. Atomo radice sempre il valore dell'ID atomo come 1.

**Riservato -** Un numero intero a 16 bit che deve essere impostato su 0.

**Conteggio figlio -** Un numero intero a 16 bit che indica il numero di atomi figli di un atomo.

**Riservato -** Un numero intero a 32 bit che deve essere impostato su 0.

## Struttura dei file dei file MOV

I file MOV sono costituiti da blocchi consecutivi. Ogni blocco ha un'intestazione di 8 byte: dimensione del blocco di 4 byte (big-endian, byte alto prima) e tipo di blocco di 4 byte - una delle firme predefinite: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Il primo pezzo è di tipo "ftype" e ha un sottotipo all'offset 8. MOV definito dal sottotipo che deve essere "qt". Per comporre il file MOV, è necessario iterare i blocchi fino a quando non viene rilevato un tipo sconosciuto.

Ecco un `esempio di esempio`: ispezionando i dati binari di un file MOV campione è evidente che inizia con una firma **ftyp** (esadecimale: 66 74 79 70) all'offset 4, che definisce QuickTime Container File Type. Il sottotipo di file è **qt~_~_** (esadecimale: 71 74 20 20) che punta al tipo di file MOV. La dimensione del primo blocco è 32 (hex: 00 00 00 20, big-endian, high byte prima), dimensione situata all'offset 0. All'offset 32 (hex: 20) si trova il secondo blocco, che ha una dimensione di 8 e digitare **mdat** (esadecimale: 6D 64 61 74).

Il blocco successivo si trova all'offset 32+8#40 (hex: 28) e ha una dimensione 3.263.028 (hex: 00 31 CA 34) e digita **mdat** (hex: 6D 64 61 74) all'offset 44 (hex : 2C). Il blocco successivo si trova all'offset 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) e ha una dimensione 21.189 (hex: 00 00 52 C5) e digita **moov** (hex: 6D 6F 6F 76) all'offset 1.836.019.574 (esadecimale: 00 31 CA 60). Questo è l'ultimo pezzo, quindi la dimensione totale del file è 3.263.068+21.189#3.284.257 byte.

## Come convertire file MOV?

Sono disponibili molti lettori multimediali e editor video software per convertire file MOV in altri formati di file video popolari. Alcuni dei lettori multimediali in grado di convertire i file MOV in altri formati includono:

* Lettore multimediale VLC VideoLAN
* Eltima Elmedia Player

Diversi lettori multimediali ed editor video, tra cui VideoLAN VLC media player ed Eltima Elmedia Player, possono convertire file MOV in altri formati. Questi software possono convertire i file MOV nei seguenti formati video.

* Video MPEG-4 - [MP4](/it/video/mp4/)
* Video WebM - [WEBM](/it/video/webm/)
* Flusso di trasporto video - [TS](/it/video/ts/)
* Formato sistemi avanzati - [ASF](/it/video/ts/)
* Ogg Vorbis Audio - [OGG](/it/audio/ogg/)
* Audio MP3 - [MP3](/it/audio/mp3/)
* Codec audio senza perdita gratuito - [FLAC](/it/audio/flac/)
* WAVE Audio - [WAV](/it/audio/wav/)

## API Open Source per file MOV

* [React Native API per convertire MOV in MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [API Python per riparare i file MOV](https://github.com/nrosenstein-stuff/movrepair)
* [API Ruby per convertire MOV in GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Riferimenti

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

