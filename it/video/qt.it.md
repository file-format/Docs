{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file QT - File filmato rapido",
  "keywords" :[ "QT", "QuickTime video", "qt format", "come riprodurre file qt", "Quick Movie File", "QTFF", "video", "Apple" ],
  "description":"Scopri il formato di file QT e le API che possono creare e aprire file QT.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Che cos'è un file QT?

Un file con estensione .qt è un file contenitore multimediale utilizzato dal framework QuickTime per archiviare i contenuti dei file multimediali. Sviluppato da Apple Inc., QuickTime File Format (QTFF) è un file contenitore multimediale che contiene audio, video o testo per la riproduzione in seguito. È il formato preferito per lo scambio di media digitali tra dispositivi, applicazioni e sistemi operativi. I file QT vengono anche salvati nel formato [MOV](/it/video/mov/) sviluppato anche da Apple Inc. Alcune delle applicazioni che possono aprire i file QT includono Apple QuickTime Player, VLC media player e Media Player Classic con K- Pacchetto codec Lite.

## Formato file QT

Il QTFF è orientato agli oggetti che espone una raccolta flessibile di oggetti per facilitare l'analisi e l'espansione. Ogni traccia in un file QT contiene un flusso multimediale codificato digitalmente o un riferimento di dati al flusso multimediale che si trova in un altro file. La struttura dati gerarchica composta da oggetti chiamati atomi funge da contenitori di tracce. Le specifiche del formato file per [QT file format](https://developer.apple.com/documentation/quicktime-file-format) sono ufficialmente disponibili da Apple Inc per riferimento dello sviluppatore.

### Descrizione del supporto

La descrizione del supporto di un file QuickTime viene memorizzata separatamente dai dati del supporto. Informazioni come il numero di tracce, il formato di compressione video e le informazioni sull'intervallo sono archiviate nella descrizione del supporto (nota anche come risorsa del film, atom del film o semplicemente film). I dati multimediali sono referenziati da un indice in questa struttura multimediale. I dati multimediali sono i dati di esempio effettivi, come fotogrammi video e campioni audio, utilizzati nel film.

### Atomi

Atom è l'unità di base del file QuickTime. Ci sono due campi principali in ogni atomo prima di qualsiasi altro campo: i campi Dimensione e Tipo. Il campo della dimensione mostra la dimensione dell'atomo mentre il campo del tipo indica il tipo di dati memorizzati nell'atomo. Per natura, gli atomi sono gerarchici, il che significa che un atomo può contenere altri atomi che possono ancora contenerne altri. Il layout di un atomo campione è mostrato nell'immagine seguente.

Ogni atomo ha due parti, intestazione e dati. L'intestazione contiene i campi di dimensione e tipo e la parte di dati contiene i dati effettivi. Inoltre, ogni campo è spiegato di seguito:

#### Dimensione dell'atomo

L'intestazione e il contenuto dell'atomo sono indicati da un numero intero a 32 bit noto come dimensione dell'atomo. Il campo size contiene la dimensione dell'atomo in byte, espressa in un intero senza segno a 32 bit.

#### Tipo di atomo

Il tipo dell'atomo è mostrato anche da un numero intero a 32 bit, che è per lo più trattato come un campo di quattro caratteri con valore knemonico, come 'moov' (0x6D6F6F76) per un atomo di film, o 'trak' (0x7472616B) per un atomo di traccia. Una volta che il tipo di atomo è noto, consente di interpretare i suoi dati.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Struttura del file ##

I file QT/MOV sono costituiti da blocchi consecutivi. Ogni blocco ha un'intestazione di 8 byte: dimensione del blocco di 4 byte (big-endian, byte alto prima) e tipo di blocco di 4 byte - una delle firme predefinite: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Il primo pezzo è di tipo "ftype" e ha un sottotipo all'offset 8. MOV definito dal sottotipo che deve essere "qt". Per comporre il file MOV, è necessario iterare i blocchi fino a quando non viene rilevato un tipo sconosciuto.

Ecco un esempio di esempio: esaminando i dati binari di un file MOV di esempio, è evidente che inizia con una firma **ftyp** (esadecimale: 66 74 79 70) all'offset 4, che definisce QuickTime Container File Type. Il sottotipo di file è **qt~_~_** (esadecimale: 71 74 20 20) che punta al tipo di file MOV. La dimensione del primo blocco è 32 (hex: 00 00 00 20, big-endian, high byte prima), dimensione situata all'offset 0. All'offset 32 (hex: 20) si trova il secondo blocco, che ha una dimensione di 8 e digitare **mdat** (esadecimale: 6D 64 61 74).

Il blocco successivo si trova all'offset 32+8#40 (hex: 28) e ha una dimensione 3.263.028 (hex: 00 31 CA 34) e digita **mdat** (hex: 6D 64 61 74) all'offset 44 (hex : 2C). Il blocco successivo si trova all'offset 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) e ha una dimensione 21.189 (hex: 00 00 52 C5) e digita **moov** (hex: 6D 6F 6F 76) all'offset 1.836.019.574 (esadecimale: 00 31 CA 60). Questo è l'ultimo pezzo, quindi la dimensione totale del file è 3.263.068+21.189#3.284.257 byte.

## Riferimenti ##

* [Formato file QT - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [Formato file QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

