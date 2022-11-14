{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file CR3 - File immagine Canon Raw 3",
  "description":"Scopri il formato di file CR3 e le API che possono creare e aprire file CR3.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Che cos'è un file CR3?

Un file CR3 è un formato di file immagine RAW Canon creato da fotocamere digitali Canon selezionate. È stato introdotto da Canon per sostituire il formato di file CR2 ed è utilizzato da alcuni dispositivi digitali Canon. I file CR3 memorizzano i dati di immagine lossless originali non elaborati acquisiti dalla fotocamera. L'uso di queste immagini grezze fornisce immagini di alta qualità e offre ampio spazio per l'editing ai fotografi. Oltre ai dati dell'immagine principale, i file CR3 memorizzano anche informazioni sui metadati sull'immagine.

## Formato file CR3

I file CR3 vengono archiviati su disco come file binario nel formato file multimediale di base ISO (ISO/IEC 14496-12) e includono anche [tag Canon] personalizzati (https://exiftool.org/TagNames/Canon.html#uuid). Include anche il [codec Canon 'crx'](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) che è un mix di JPEG-LS (Rice-Golomb + RLE codifica) e JPEG-2000 (LeGall 5/3 DWT + quantificazione).

## Tag personalizzati CR3

I file CR3 contengono tag personalizzati per scopi diversi. Alcuni di questi tag sono i seguenti.

|ID tag| Nome etichetta| Scrivibile |Valori/Note|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Tag CCTP Canon|
|'CMT1' |IFD0| - |--> Tag EXIF|
|'CMT2' |ExifIFD| - |--> Tag EXIF|
|'CMT3' |MakerNoteCanon| - |--> Tag Canon|
|'CMT4' |GPSInfo| - |--> Tag GPS|
|'CNCV' |CompressorVersion| no| |
|'CNOP' |CanonCNOP| - |--> Tag CNOP Canon|
|'CNTH' |CanonCNTH| - |--> Canon CNTH Tag|
|'THMB' |Immagine miniatura| no| |

## Riferimenti

* [Formato file CR2](http://lclevy.free.fr/cr2/)
* [Tag Canon](https://exiftool.org/TagNames/Canon.html#uuid)

