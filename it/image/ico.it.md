{
  "date" : "2019-10-11",
  "keywords" :[ "file ico", "formato file ico", "cos'è un file ico", "file", "esempio ico", "estensione file ico", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Formato file immagine",
  "description":"Scopri il formato di file ICO e le API che possono creare e aprire file ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file ICO?

I file con estensione ICO sono tipi di file immagine utilizzati come icona per la rappresentazione di un'applicazione su [Microsoft Windows](https://www.microsoft.com/en-us/windows). Questi sono disponibili in diverse dimensioni, supporto colore e risoluzione per soddisfare i requisiti del display. Un altro formato di file immagine simile su Microsoft Windows è [CUR](/it/image/cur/) per la rappresentazione del cursore e definisce un hotspot nell'intestazione dell'immagine. Su MacOS, i formati di file ICNS hanno lo stesso scopo dei file ICO. Diversi siti Web online e applicazioni offrono la funzione di creare tali file e convertire altri formati di immagine come [BMP](/it/image/bmp/), [PNG](/it/image/png/), ecc. in formato file icona. Il tipo di supporto Internet registrato IANA ufficiale per i file ICO è image/vnd.microsoft.icon.

## Breve storia ##

Le icone sono state introdotte con il lancio di Microsoft Windows 1.0. Questi erano di dimensioni 32x32 ed erano monocromatici. Con l'arrivo di win32, è stato introdotto il supporto per le immagini delle icone in true color con dimensioni fino a 256x256 pixel. Windows XP è stato il primo a fornire supporto per immagini di icone a colori a 32 bit, consentendo di aggiungere all'icona aree semitrasparenti come ombre, anti-alias ed effetti simili al vetro. Microsoft consiglia solo dimensioni delle icone fino a 48 × 48 pixel per Windows XP. Windows Vista ha aggiunto una visualizzazione a icone di 256 × 256 pixel in Esplora risorse, oltre al supporto per il formato compresso [PNG](/it/image/png/). Con gli utenti che utilizzano risoluzioni più elevate e modalità DPI elevate, si consigliano formati di icone più grandi (come 256 × 256).

## Formato file ICO ##

Un singolo file ICO è costituito da una o più piccole immagini di più dimensioni e profondità di colore. La presenza di immagini di dimensioni multiple serve per il ridimensionamento appropriato a diverse risoluzioni dello schermo. Tutti i valori nei file ICO/CUR sono rappresentati in ordine di byte [little-endian](https://en.wikipedia.org/wiki/Little-endian).

Il file ICO è costituito da un'intestazione Icon, una directory Icon,

|Campo|Descrizione
---|---|
|Intestazione icona|Memorizza informazioni generali sul file ICO.
|Directory[1..n]|Memorizza informazioni generali su ogni immagine nel file.
|Icona #1|I "dati" effettivi per la prima immagine nel vecchio formato AND/XOR DIB o PNG più recente
|...|
|Icona #n|Dati per l'ultima immagine dell'icona

### Intestazione ###

|Offset|Dimensione (in byte)|Scopo
---|---|---|
|0|2|Riservato. Deve essere sempre 0.
|2|2|Specifica il tipo di immagine: 1 per l'immagine dell'icona (.ICO), 2 per l'immagine del cursore (.CUR). Altri valori non sono validi.
|4|2|Specifica il numero di immagini nel file.

### Directory ###

La directory contenuta in un file ICO, rappresentato come struttura ICONDIR, contiene una struttura ICONDIRECTORY per ogni immagine nel file. Lo stesso è seguito da un blocco contiguo di tutti i dati bitmap dell'immagine. Questo è come mostrato di seguito.

|Offset|Dimensione|Descrizione
---|---|---|
|0 (0)|1|Larghezza, dovrebbe essere 0 se 256 pixel
|1 (1)|1|Altezza, dovrebbe essere 0 se 256 pixel
|2 (2)|1|Conteggio colori, dovrebbe essere 0 se più di 256 colori
|3 (3)|1|Riservato, dovrebbe essere 0
|4 (4)|2|I piani di colore in formato .ICO, dovrebbero essere 0 o 1, o l'hotspot X in formato .CUR
|6 (6)|2|Bit per pixel in formato .ICO o hotspot Y in formato .CUR
|8 (8)|4|Dimensione dei dati bitmap in byte.
|12 (C)|4|Spostamento nel file.

## Riferimenti ##

* [ICO - Di Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

