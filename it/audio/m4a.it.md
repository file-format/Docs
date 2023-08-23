{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "file", "estensione", "format", "che cos'è il formato file m4a", "music", "formato file m4a", "M4A vs MP3", "specifica del formato file m4a "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file M4A e le API che possono creare, convertire e aprire file M4A.",
  "title" :"M4A - File audio MPEG-4",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Che cos'è un file M4A?

Il **formato file M4A** è un file audio creato utilizzando AAC (Advanced Audio Coding), noto come compressione con perdita di dati. La parola M4A abbreviata in MPEG 4 Audio. Questi file audio di solito hanno l'estensione .m4a. Ciò è particolarmente vero per i contenuti non protetti. Può memorizzare vari tipi di contenuti audio, come audiolibri, canzoni e podcast. M4A è solitamente realizzato come formato più avanzato dell'MP3, che in genere non era stato progettato solo per l'audio. È solo un livello audio nei file video MPEG 1 o 2.

Il formato M4A è crittografato da FairPlay Digital Rights Management poiché è stato venduto tramite iTunes Store utilizzando l'estensione .m4p. Gli iPhone Apple utilizzano l'audio MPEG-4 per le loro suonerie, ma quei file audio utilizzano l'estensione .m4r.


## M4A vs MP3

Sia M4A che [MP3](/audio/mp3/) sono formati di file solo audio.

**M4A**: migliore di MP3 in termini di qualità e dimensioni se codificato allo stesso bit rate. L'estensione del file .m4a è così comune perché è stata utilizzata da Apple per l'uso in iTunes Music Store. L'M4A è un file audio compresso utilizzando la tecnologia MPEG-4; un algoritmo per la compressione con perdita. È fondamentalmente associato a "MPEG-4 Audio Layer", i file con estensione .m4a sono il livello audio dei film MPEG-4. Ha lo scopo di superare l'MP3 e diventare il nuovo standard nella compressione audio. È molto vicino all'MP3 in molti modi, ma è stato introdotto per avere una qualità migliore con file di dimensioni uguali o addirittura inferiori. Il formato M4A è stato introdotto per la prima volta da Apple. Il tipo di formato è realizzato anche come Apple lossless Encoder (ALE).

Pertanto, attualmente l'M4A non è riuscito a ottenere il successo mainstream dell'MP3 perché il formato audio generalmente non è ancora riproducibile. In qualche modo è limitato solo a MacOS, iPod e altri prodotti Apple.

**Mp3**: Il formato audio digitale più famoso. È stato anche uno dei primi formati di compressione sulla scena ed è diventato molto popolare tra gli amanti della musica. Il suo successo mainstream è così veloce che il tipo di file può essere riprodotto universalmente e con quasi tutto, hardware o software. In senso generale, l'M4A produrrà una migliore qualità del suono, ma molti sosterrebbero che, che sia vero o meno, la differenza sonora non è distinguibile e sarebbe una perdita di tempo cercare di convertire file MP3 in file M4A. Alla fine, la conversione ti farà solo perdere la qualità del suono originale.

## Specifica del formato di file M4A

I file M4A sono costituiti da blocchi consecutivi. Ogni blocco ha 8 byte di intestazione e suddiviso come:
- Dimensione del blocco di 4 byte (big-endian, prima il byte alto)
- Tipo di blocco di 4 byte - una delle firme predefinite: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

Il primo pezzo sarà di tipo "ftype" e avrà un sottotipo all'offset 8. L'M4A definito dal sottotipo che deve essere "M4A_", per il sottotipo M4B deve essere "M4B_" e per il sottotipo M4P deve essere essere "M4P_".

Iterando i blocchi, finché non viene rilevato un blocco di tipo sconosciuto, comporrà il file M4A (MPEG-4 Audio).

## Riferimenti ##

* [MPEG-4 Parte 14 - Di Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Esempio di formato e recupero audio MPEG-4 parte 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

