{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file CR2 - File immagine Canon Raw 2",
  "description":"Scopri il formato di file CR2 e le API che possono creare e aprire file CR2.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Che cos'è un file CR2?

Un file CR2 (Camera RAW 2) è un file di immagine RAW creato dalle fotocamere digitali Canon. Memorizza i dati di immagine lossless originali non elaborati acquisiti dalla fotocamera. Il formato file CR2 è stato sviluppato da Canon per le sue fotocamere digitali e può registrare immagini di alta qualità fino a 14 bit di RGB. Ciò produce immagini di alta qualità con spazio sufficiente per la post-elaborazione. Il formato immagine CR2 è stato utilizzato da Canon nei modelli di fotocamere 350D, 20D e 1D. I file CR2 sono file RAW e contengono informazioni aggiuntive sui metadati come informazioni sulla fotocamera, informazioni sull'obiettivo, informazioni sul bracketing, bilanciamento del bianco e altre impostazioni.

## Formato file CR2

I file CR2 vengono archiviati nella scheda di memoria della fotocamera come file binari nel formato di file proprietario Canon. Il formato di file CR2 ha sostituito il formato di file CRW inizialmente utilizzato ed è stato sostituito in seguito dal formato di file Canon RAW 3. Il formato file CR2 si basa sulle specifiche [TIFF](/it/image/tiff/) che dispone di 4 Image File Directory (IFD).

|Offset |Contenuto |Commento|
---|---|---|
|0x0000 |Header |contiene l'ordine dei byte, la versione e l'offset rispetto all'immagine RAW|
|calcolato |IFD#0 |questa parte contiene la sezione Exif, che contiene la sezione Makernotes.
Informazioni sull'immagine#0|
|calcolato |immagine#0 |versione ridotta dell'immagine (un quarto delle dimensioni dell'originale), compressa in Jpeg|
|calcolato |IFD#1 |Informazioni sull'immagine#1.|
|calcolato |immagine#1 |versione ridotta dell'immagine, compressa in Jpeg|
|calcolato |IFD#2 |Informazioni sull'immagine#2.|
|calcolato |immagine#2 |versione piccola dell'immagine, non compressa|
|nell'intestazione| IFD#3| Informazioni sull'immagine n. 3, l'immagine RAW a dimensione intera|
|calcolato |immagine#3 |Dati immagine RAW, compressi senza perdita di dati in Jpeg (non dati RGB!)|

## Vantaggio del formato file CR2

La memorizzazione di immagini in formato RAW consente un'ampia post-elaborazione della fotografia, ad esempio la regolazione del bilanciamento del bianco. Questo è molto più difficile e con una grande perdita di qualità con altri formati di file immagine come [JPEG](/it/image/jpeg/).

## CR2 è meglio di JPEG?

I file CR2 sono file grezzi senza alcuna perdita di dati e, quindi, senza perdita di qualità. JPEG dall'altro è un formato di file immagine con perdita in quanto perde alcuni dati per ridurre il file. Pertanto, i file CR2 sono di alta qualità e più adatti per ritocchi e miglioramenti.

## Riferimenti

* [Formato file CR2](http://lclevy.free.fr/cr2/)

