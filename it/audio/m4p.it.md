{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "file", "estensione", "format", "che cos'è il formato file m4p", "music", "formato file m4p", "M4b vs MP3", "specifica del formato file m4p "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file M4P e le API che possono creare, convertire e aprire file M4P.",
  "title" :"M4P - Formato file audiolibro MPEG-4",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Che cos'è un file M4P?
Il file con estensione .m4p è un file audio che di solito è disponibile presso l'Apple iTunes Store per il download. In altre parole possiamo dire che M4P è un file AAC ma protetto da copia utilizzando un Digital Rights Management (DRM). Significa che i file M4P possono essere riprodotti solo su sistemi o dispositivi autorizzati. Di solito i file M4P sono specifici per i dispositivi multimediali Apple. Quindi questi file possono essere riprodotti solo su macbook Apple, podcast, smartphone come iPhone 6 o iPhone 7.

## Formato file M4P
M4P sta per MPEG 4 Protected (audio) e codifica l'audio con Advanced Audio Codec (AAC) e protegge il file dall'uso non autorizzato del file. Questo formato di file è generalmente considerato un formato di file audio di iTunes Music Store. Apple utilizza il suo sistema FairPlay Digital Rights Management (DRM) per proteggere i file M4P. FairPlay DRM si basa sulla tecnologia sviluppata da Veridisc. Il suo meccanismo di protezione funziona crittografando il flusso audio AAC utilizzando la crittografia AES. L'utente riceve una chiave principale che viene assegnata al suo account per la decrittazione. Questo formato di file è stato introdotto in sostituzione del formato di file MP3, perché l'MP3 non era originariamente inteso come file audio, ma come livello III in un file video MPEG 1 o 2.


## Specifiche del formato file M4P

Simile a [M4A](/it/audio/m4a/), anche i file M4P sono costituiti da blocchi consecutivi. Ogni blocco ha 8 byte di intestazione e suddiviso come:
- Dimensione del blocco di 4 byte (big-endian, prima il byte alto)
- Tipo di blocco da 4 byte - una delle firme predefinite: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt ", "ctab", "ssrc".

Simile a M4A, il primo blocco in M4P sarà di tipo "ftype" e ha un sottotipo all'offset 8. L'M4P definito dal sottotipo che deve essere "M4P_".

Iterando i blocchi, finché non viene rilevato un blocco di tipo sconosciuto, comporrà il file M4P (MPEG-4 Audio).

## Riferimenti ##

* [MPEG-4 Parte 14 - Di Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Esempio di formato e recupero audio MPEG-4 parte 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

