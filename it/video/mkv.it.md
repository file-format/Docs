{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file MKV",
  "keywords" :[ "mkv", "matroska video", "mkv format", "come riprodurre file mkv", "video", "file", "format" ],
  "description":"Scopri il formato di file MKV e le API che possono creare e aprire file MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Che cos'è un file MKV? ##

MKV (Matroska Video) è un contenitore multimediale simile al formato [MOV](/it/video/mov/) e [AVI](/it/video/avi/) ma supporta più di una traccia audio e sottotitoli nello stesso file. Un file MKV è il formato contenitore multimediale Matroska utilizzato per i video. MKV è basato su Extensible Binary Meta Language e supporta diversi formati di compressione video e audio. La principale differenza tra MKV e altri formati video è che MKV è un contenitore e non un codec. I file MKV vengono salvati con l'estensione .mkv. MKV può incorporare audio, video e sottotitoli in un unico file anche se tali elementi utilizzano diversi tipi di codifica. Ad esempio, potresti avere un file MKV che contiene video H.264 e MP3 o AAC per l'audio. MKV supporta anche descrizioni, valutazioni, copertine e persino capitoli. Ci sono diverse caratteristiche chiave che MKV è a prova di futuro. Queste caratteristiche includono:

- Supporto per la ricerca rapida.
- Possibilità di selezionare diversi flussi audio e video.
- Supporto per i sottotitoli (hardcoded e soft-coded).
- Supporto per metadati, capitoli e menu.
- Possibilità di streaming online.
- Possibilità di recuperare file errati che forniscono la capacità di riprodurre file danneggiati.

## Breve storia ##

Il file MKV è nato nel 2002 in Russia. Lo sviluppatore principale era Lasse Kärkkäinen che ha lavorato con il fondatore di Matroska, Steve Lhomme, e un team di programmatori. MKV è stato sviluppato come un progetto di standard aperti, il che significa che è open source e gratuito. Col passare del tempo, il formato è stato migliorato ed è diventato la base del formato multimediale WebM nel 2010.

## Matroska Design ##

Matroska aggiunge i seguenti vincoli alla specifica EBML.

- Il **docType** dell'**EBML Header** deve essere 'matroska'.
- **EBMLMaxIDLength** di **EBML Header** deve essere 4.
- **EBMLMaxSizeLength** di **EBML Header** deve essere compreso tra 1 e 8 (incluso).

Tutti gli elementi di primo livello sono codificati in 4 ottetti.

- Codici lingua: Matroska (versioni da 1 a 3) utilizzava codici lingua che possono essere il modulo bibliografico ISO-639-2 di 3 lettere (come "fre" per il francese), o un codice paese aggiuntivo potrebbe essere utilizzato come "fre-ca " per il francese canadese. A partire da Matroska versione 4, ISO 639-2 o BCP 47 POSSONO essere utilizzati per i codici lingua, sebbene sia consigliato BCP 47.
- Tipi fisici: hanno un significato diverso per i file audio e video. Ad esempio, ChapterPhysicalEquiv = 60 significa (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) per l'audio e (DVD / VHS / LASERDISC) per il video.
- Struttura del blocco - Intestazione del blocco: l'intestazione del blocco contiene informazioni relative al numero di traccia, timestamp, tipo di allacciatura, ecc.
- Allacciatura: è un meccanismo per risparmiare spazio durante la memorizzazione dei dati che viene generalmente utilizzato per piccoli blocchi di dati (frame). Esistono 3 tipi di allacciatura:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- Struttura SimpleBlock: è ispirata alla **struttura a blocchi** con la differenza principale che è l'aggiunta di **Keyframe** e **Discardable** flag. A parte questo, tutto è uguale.

## Struttura Matroska ##

Un documento Matroska deve essere composto da almeno un **Documento EBML** che utilizza il **Tipo di documento Matroska**. Ciascun **documento EBML** deve iniziare con un **intestazione EBML** seguita dall'**elemento radice EBML** definito come segmento. Matroska definisce diversi elementi di primo livello che possono verificarsi all'interno del **segmento**.

EBML utilizza un sistema di elementi per comporre un documento EBML. Di seguito è riportato l'elenco degli elementi di primo livello nel file Matroska:

- **Documento EBML**: wrapper per l'intero file.
- **EBML Header**: contiene le informazioni di intestazione per il file come DocType.
- **Segmento**: l'elemento principale che contiene tutti gli altri elementi di primo livello.
- **SeekHead**: contiene la posizione dei segmenti di altri elementi di primo livello.
- **Info**: contiene informazioni generali sul Segmento.
- **Tracce**: un elemento di informazioni di primo livello con molte tracce descritte.
- **Capitoli**: viene utilizzato per definire i menu di base e i dati della partizione.
- **Cluster**: l'elemento di primo livello contenente la struttura del blocco.
- **Cues**: un elemento di primo livello che contiene tutte le voci locali del segmento che velocizzano l'accesso alla ricerca.
- **Allegati**: contiene file allegati.
- **Tag**: questo elemento contiene metadati che descrivono tracce, edizioni, capitoli, allegati o il segmento nel suo insieme.

La tabella seguente mostra la struttura del documento Matroska con la maggior parte degli elementi visualizzati in una gerarchia:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Intestazione EBML | | | |
| segmento | SeekHead| cercare | Cerca ID |
| | | | CercaPosizione |
| | Informazioni | SegmentUID | |
| | | Nomefilesegmento | |
| | | PrevUID | |
| | | Nome file precedente | |
| | | NextUID | |
| | | SuccessivoNome file | |
| | | SegmentFamily | |
| | | ChapterTranslate | |
| | | Scala del timestamp | |
| | | Durata | |
| | | DataUTC | |
| | | Titolo | |
| | | MuxingApp | |
| | | ScritturaApp | |
| | tracce | TrackEntry | Numero di traccia |
| | | | TrackUID |
| | | | Tipo di traccia |
| | | | Nome |
| | | | Lingua |
| | | | CodecID |
| | | | CodecPrivato |
| | | | CodecName |
| | | | Video | FlagInterlacciato |
| | | | | Ordine di campo |
| | | | | Modalità Stereo |
| | | | | Modalità Alfa |
| | | | | Larghezza pixel |
| | | | | Altezza pixel |
| | | | | Larghezza display |
| | | | | Altezza di visualizzazione |
| | | | | Tipo rapporto aspetto |
| | | | | Colore |
| | | | Audio | Frequenza di campionamento |
| | | | | Canali |
| | | | | Profondità di bit |
| | Capitoli | EdizioneEntrata | EdizioneUID |
| | | | EdizioneFlagHidden |
| | | | EdizioneFlagDefault |
| | | | EdizioneFlagOrdinato |
| | | | Capitolo Atom | CAPITOLO |
| | | | | CapitoloStringUID |
| | | | | CapitoloTimeStart |
| | | | | ChapterTimeFine |
| | | | | ChapterFlagHidden |
| | | | | Visualizzazione capitolo | ChapString |
| | | | | | ChapLanguage |
| | Cluster | Timestamp |
| | | Silent Tracks |
| | | Posizione |
| | | Dimensione precedente |
| | | Blocco semplice |
| | | BloccoGruppo |
| | | Blocco crittografato |
| | Spunti | CuePoint | CueTime |
| | | | Posizioni CueTrack |
| | Allegati | File allegato | Descrizione file |
| | | | NomeFile |
| | | | FileMimeType |
| | | | FileUID |
| | | | Riferimento file |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | tag | Etichetta | Obiettivi | ValoreTipo Obiettivo |
| | | | | Tipo di destinazione |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAllegatoUID |
| | | | Etichetta semplice | TagName |
| | | | | TagLingua |
| | | | | TagDefault |
| | | | | Stringa di tag |
| | | | | TagBinary |
| | | | | Etichetta semplice |


### Utilizzo dei codec ###

Se non desideri un nuovo lettore multimediale e preferisci utilizzare il tuo lettore esistente, dovrai installare alcuni codec (abbreviazione di compressione/decompressione). Anche se il download di codec è un'opzione valida, dovresti fare attenzione alla fonte e questi potrebbero contenere malware.

## Riferimenti ##

- [Matroska di Wikipedia](https://en.wikipedia.org/wiki/Matroska)

