{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "file", "estensione", "formato", "che cos'è il formato file m4b", "musica", "formato file m4b", "M4b vs MP3", "specifica del formato file m4b "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file M4B e le API che possono creare, convertire e aprire file M4B.",
  "title" :"M4B - Formato file audiolibro MPEG-4",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Che cos'è un file M4B?

Il file con estensione .m4b è un audiolibro generalmente utilizzato da Apple Books e iTunes. L'audio utilizzato in questo formato viene memorizzato in MPEG-4 e compresso utilizzando la codifica AAC. Un file M4B è molto simile a M4A ma supporta le funzionalità relative agli audiolibri, come i segnalibri e le interruzioni di capitolo. I file M4B sono disponibili in entrambe le versioni abilitate DRM e DRM libere. Gli audiolibri con crittografia DRM sono generalmente audiolibri a pagamento da iTunes Store. Considerando che, DRM free può essere trovato facilmente su Internet.

## Formato file M4B

I file dell'audiolibro contenenti metadati, immagini, segnalibri e collegamenti ipertestuali possono essere salvati con estensione .m4a ma generalmente viene utilizzata l'estensione .m4b durante il salvataggio, proprio per specificare che il file ha un formato di file audiolibro. Fairplay DRM (Digital Rights Management) viene utilizzato da applicare per proteggere i propri file M4B. Quindi i file scaricati da iTunes possono essere riprodotti solo su dispositivi o computer autorizzati.


## M4B contro M4A

Sia M4B che [MP3](/audio/mp3/) sono formati di file solo audio.

**M4B**: vince rispetto a MP3 in termini di qualità se codifica entrambi allo stesso bit rate. L'M4B è un file di audiolibro compresso utilizzando la codifica AAC. È fondamentalmente associato a "MPEG-4 Audio Layer", i file con estensione .m4b sono il livello audio dei film MPEG-4 ma con funzionalità aggiuntive relative agli audiolibri. Il suo obiettivo è superare l'MP3 e diventare il nuovo standard nella compressione audio. È molto simile all'MP3 in molti modi, ma è stato sviluppato per avere una qualità migliore con file di dimensioni uguali o addirittura inferiori. Il formato M4B è stato introdotto per la prima volta da Apple. Il tipo di formato è realizzato anche come Apple lossless Encoder (ALE).

Pertanto, attualmente l'M4B non è riuscito a ottenere il successo mainstream dell'MP3 perché il formato audio non è ancora riproducibile comunemente.

**Mp3**: un formato audio digitale familiare a tutti. Un primissimo formato di compressione sulla scena ed è diventato molto famoso tra gli ascoltatori di musica. Il suo successo mainstream è così rapido che il tipo di file può essere riprodotto universalmente e compatibile con quasi tutto, hardware o software. In senso generale, l'M4A produrrà una migliore qualità del suono, ma molti sosterrebbero che, che sia vero o meno, la differenza del suono non è paragonabile e sarebbe una perdita di tempo cercare di convertire file MP3 in file M4A. Infine, la conversione ti farà solo perdere la qualità del suono originale.

## Specifica del formato di file M4B

Simile a [M4A](/it/audio/m4a/), anche i file M4B sono costituiti da blocchi consecutivi. Ogni blocco ha 8 byte di intestazione e suddiviso come:
- Dimensione del blocco di 4 byte (big-endian, prima il byte alto)
- Tipo di blocco da 4 byte - una delle firme predefinite: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "skip", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT ", "scpt", "ssrc".

Simile a M4A, il primo blocco in M4B sarà di tipo "ftype" e avrà un sottotipo all'offset 8. L'M4B definito dal sottotipo che deve essere "M4B_".

Iterando i blocchi, fino a quando non viene rilevato un blocco di tipo sconosciuto, comporrà il file M4B (MPEG-4 Audio).

## Riferimenti

* [MPEG-4 Parte 14 - Di Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Esempio di formato e recupero audio MPEG-4 parte 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

