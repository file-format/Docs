{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "estensione", "file", "formato", "immagine", "Immagine icona Apple", "macOS", "Apple", "Icona" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Immagine icona mela",
  "description":"Scopri il formato di file ICNS e le API che possono creare e aprire file ICNS.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Che cos'è un file ICNS? ##

Un formato icona utilizzato dai programmi macOS è chiamato file ICNS. Consente bande alfa a 1 bit e 8 bit e salva una o più immagini, generalmente create da documenti [PNG](/it/image/png). L'icona del programma nel browser e nell'interfaccia di macOS viene visualizzata utilizzando i file ICNS.

In base alla posizione, la stessa icona di stile può avere più impostazioni. Il formato ICNS ha subito numerose modifiche e si è evoluto al punto che ora può essere utilizzato come base per vari formati compatibili. Ecco alcuni altri punti importanti che devi sapere:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource e Mac OS icons Resource sono alcuni degli altri nomi.
* Per le informazioni sull'icona, viene utilizzata un'origine nel ramo delle risorse.
* Nella maggior parte dei casi, un file contiene numerose immagini. Le dimensioni delle immagini supportate sono 1612 pixel quadrati e 1024, 512, 256, 128, 48, 32 e 16 pixel quadrati.


## Formato file ICNS ##

Il formato dati ICNS è una capsula per una o più immagini, che supporta bande a 1 bit e numerosi stati dell'immagine.
Il sistema operativo può ridimensionare le immagini delle icone per adattarle alle dimensioni di visualizzazione richieste. Le immagini delle icone più grandi vengono in genere salvate come file [JPEG](/it/image/jpeg/) 2000 o [PNG](/it/image/png). È possibile un tipo di file ICNS compresso e non compresso.

Un'intestazione e un'icona binaria costituiscono la struttura di un file ICNS. L'intestazione contiene 8 byte di dati, quattro dei quali sono il valore letterale magico e quattro sono la lunghezza del file. Il tipo e la dimensione di ciascuna immagine dell'icona sono memorizzati nella sezione dei dati dell'icona, seguita dai dati dell'immagine binaria. La dimensione dell'immagine determina la dimensione della sezione binaria.

## Specifiche tecniche ##

### Intestazione ###

|Offset|Dimensione|Obiettivo
---|---|---|
|0|4|Magic letterale, deve essere "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Lunghezza del file, in byte, prima msb


### Dati icona ###

|Offset|Dimensione|Obiettivo
---|---|---|
|0|4|Tipo di icona
|4|4|Lunghezza dei dati, in byte (inclusi tipo e lunghezza), prima msb
|8|Variabile|Dati icona

### Compressione ###

I dati dei pixel sono compressi in una certa misura. I pixel a 32 bit ("is32", "il32", "ih32", "it32") e ARGB ("ic04", "ic05") sono spesso compressi (per canale) in modo simile a PackBits.

|Valore principale|Byte di coda|Risultato (non compresso)
---|---|---|
|0 - 127|1 - 128|1 - 128 byte
|128 - 255|1 byte|3 - 130 copie

## Riferimento ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

