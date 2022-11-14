{
  "date" : "2019-10-11",
  "keywords" :[ "file tga", "formato file tga", "cos'è un file tga", "file", "esempio tga", "estensione file tga", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file TGA - Un file di immagine grafica TARGA",
  "description":"Scopri il formato di file TGA e le API che possono creare e aprire file TGA.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file TGA?

Un file con estensione .tga è un formato grafico raster ed è stato creato da Truevision Inc. È stato progettato per le schede TARGA (Truevision Advanced Raster Adapter) e ha fornito supporto per display Highcolor/truecolor per PC compatibili con IBM. Supporta 8, 16, 24 e 32 bit per pixel e canale alfa a 8 bit. Supporta anche la compressione RLE senza perdita di dati che può essere applicata per ridurre le dimensioni dell'immagine. Le foto e le texture digitali utilizzano il formato immagine TGA.

## Breve storia

La formazione del formato di file TGA è nata nel 1984 da AT&T EPICenter (successivamente estratta e formata come entità indipendente nota come Truevision) che stava lavorando alla commercializzazione di nuove tecnologie sviluppate da AT&T per i buffer di frame a colori. EPICenter stava già lavorando sulle sue prime due schede, la VDA (Video Display Adapter) e l'ICB (Image Capture Board) per le quali era già in corso il lavoro su due tipi di file, .vda e .icb. Questi formati di file sono stati codificati ed è stato introdotto un formato di file specifico meno ampio TGA. TGA era un'estensione di ciò che era già in uso e forniva informazioni come larghezza, altezza, profondità dei pixel, mappa dei colori associata e origine dell'immagine.

La versione 2.0 di TGA, pubblicata nel 1989, incorporava diverse funzionalità avanzate come:

* Miniature
* Canale alfa
* Valore gamma
* Metadati testuali

I principali contributori alla versione 2.0 di TGA includono Shawn Steiner, Kevin Fiedly e David Spoelstra di Truevision.

## Specifiche del formato file TGA TARGA

Un file TGA è composto da 2 parti principali:

* Intestazione
* Informazioni sui pixel di colore

Tutti i valori in un file TGA sono in littl-endian secondo le specifiche del formato.

### Intestazione TGA

Un'intestazione di file TGA è composta dai seguenti 5 campi.

|Nr. campo|Lunghezza |Nome campo |Descrizione|
---|---|---|---|
|1| 1 byte |Lunghezza ID| Lunghezza del campo ID immagine (0-255)|
|2| 1 byte |Tipo mappa colori| Se è inclusa una mappa dei colori (0 - indica che nessun dato della mappa dei colori è incluso con questa immagine. 1 - indica che una mappa dei colori è inclusa con questa immagine.)|
|3| 1 byte |Tipo di immagine| Compressione e tipi di colore (0- Nessun dato immagine incluso. 1- Non compresso, Immagine mappata a colori, 2- Non compresso, Immagine True Colour, 9- Codificato run-length, Immagine mappata a colori, 11- Codificato run-Length, Immagine in bianco e nero )|
|4| 5 byte |Specifica della mappa dei colori| Descrive la mappa dei colori|
|5| 10 byte |Specifica dell'immagine| Dimensioni e formato dell'immagine|

### Dati immagine e mappa colori

|Campo n. |Lunghezza |Campo |Descrizione|
---|---|---|---|
|6 |Dal campo lunghezza ID immagine| ID immagine| Campo facoltativo contenente informazioni identificative|
|7 |Dal campo delle specifiche della mappa dei colori| Dati mappa a colori| Tabella di ricerca contenente i dati della mappa dei colori|
|8 |Dal campo delle specifiche dell'immagine| Dati immagine| Memorizzato secondo il descrittore dell'immagine|

### Area sviluppatori (opzionale)

TGA versione 2.0 fornisce supporto per ulteriori miglioramenti/extra che molti sviluppatori desideravano memorizzare più informazioni. L'informazione è facoltativa in modo che se un decoder TGA non è in grado di interpretarla, verrà ignorata.

### Area di estensione (opzionale)

|Campo n.| Lunghezza| Campo |Descrizione|
---|---|---|---|
|10| 2 byte |Dimensione estensione |Dimensione in byte dell'area di estensione, sempre 495|
|11| 41 byte| Nome dell'autore |Nome dell'autore. Se non utilizzati, i byte devono essere impostati su NULL (\0) o spazi|
|12| 324 byte| Commento dell'autore| Un commento, organizzato in quattro righe, ciascuna composta da 80 caratteri più un NULL|
|13| 12 byte| Data/ora |Data e ora di creazione dell'immagine|
|14| 41 byte| ID lavoro||
|15| 6 byte| Tempo di lavoro| Ore, minuti e secondi spesi per la creazione del file (per fatturazione, ecc.)|
|16| 41 byte| ID software |L'applicazione che ha creato il file.|
|17| 3 byte| Versione software||
|18| 4 byte| Colore chiave||
|19| 4 byte| Proporzioni pixel||
|20| 4 byte| Valore gamma||
|21| 4 byte| Offset correzione colore |Numero di byte dall'inizio del file alla tabella di correzione colore, se presente|
|22| 4 byte| Francobollo | Numero di byte dall'inizio del file all'immagine del francobollo se presente|
|23| 4 byte| Offset linea di scansione| Numero di byte dall'inizio del file alla tabella delle linee di scansione se presente|
|24| 1 byte| Tipo di attributi| Specifica il canale alfa|

### Piè di pagina del file (facoltativo)

Gli ultimi 26 byte del file rappresentano il piè di pagina, che se presente significa che è probabile che si tratti di un file TGA versione 2.

|Campo n.| Lunghezza| campo| Descrizione|
---|---|---|---|
|28| 4 byte| Offset estensione| Offset in byte dall'inizio del file|
|29| 4 byte| Offset area sviluppatore| Offset in byte dall'inizio del file|
|30| 16 byte| Firma| Contiene "TRUEVISION-XFILE"|
|31| 1 byte| | Contiene "."|
|32| 1 byte| | Contiene NULL|


## Riferimenti

* [Specifiche del formato file TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA di Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

