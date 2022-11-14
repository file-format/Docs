{
  "date" : "2020-01-10",
  "keywords" :[ "file dib", "formato file dib", "cos'è un file dib", "file", "esempio dib", "estensione file dib", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Scopri il formato di file DIB e le API che possono creare e aprire file DIB.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Che cos'è un file DIB?

Una bitmap indipendente dal dispositivo (DIB) è un file di immagine raster con una struttura simile ai file bitmap standard([BMP]()/image/bmp/)). Contiene una tabella dei colori che descrive la mappatura dei colori RGB ai valori dei pixel. Ciò consente a DIB di rappresentare l'immagine su qualsiasi dispositivo. Può essere aperto con quasi tutte le applicazioni in grado di aprire un file BMP standard su Windows e macOS. DIB sono file binari e hanno un formato di file complesso simile a BMP. Le immagini DIB sono indipendenti dalle capacità di output dei dispositivi di rendering in termini di profondità del colore e pixel per pollice.

## Specifiche del formato file DIB ##
Un DIB contiene le seguenti informazioni su colore e dimensione:

* Il formato colore del dispositivo su cui è stata creata l'immagine rettangolare.
* La risoluzione del dispositivo su cui è stata creata l'immagine rettangolare.
* La tavolozza per il dispositivo su cui è stata creata l'immagine.
* Una matrice di bit che mappa triplette rosse, verdi, blu ( RGB ) su pixel nell'immagine rettangolare.
* Un identificatore di compressione dei dati che indica lo schema di compressione dei dati (se presente) utilizzato per ridurre la dimensione dell'array di bit.

### Formato blocco dati DIB ###

DIB viene nel contesto del blocco di memoria rispetto ai file .DIB archiviati su disco. Il blocco di memoria comprende una struttura conforme alle specifiche API di Windows per i DIB. Il DIB effettivo è costituito da:
* Un'intestazione
* Palette dei colori
* Dati pixel

In pratica, lavorare con i dati di tavolozza, intestazione e immagine viene eseguito come se fossero tre blocchi di memoria separati. Un handle a questo blocco di memoria comune viene assegnato tramite GlobalAlloc ed è noto come HDIB, che viene utilizzato per estrarre e lavorare con l'intestazione, la tabella dei colori e i dati dei pixel.

### Strutture ###
Le informazioni contenute in un DIB sono rappresentate da diverse strutture. Questi includono:

BITMAPInfo - Definisce la dimensione e le informazioni sul colore per un DIB
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Si compone di un BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
seguito da due o più strutture RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Bit di dati ###
|Bit|Descrizione|
---|---|
|Formato a 1 bit (monocromatico)|Le bitmap monocromatiche sono composte da due colori (bianco e nero). A causa di questo numero limitato di colori, queste bitmap occupano meno spazio su disco. bitBitCount restituisce true o false per la rappresentazione di entrambi i colori. La maggior parte delle applicazioni salta completamente la tavolozza se bitBitCount==1.
|Formato a 4 bit (VGA o 16 colori)|Ogni byte di dati immagine rappresenta due pixel e bitBitCount==4. Questi bit rappresentano il colore del pixel in ordine decrescente.
|Formato a 8 bit (256 colori)|Questo formato a 8 bit può rappresentare un massimo di 256 colori. Ogni byte nell'array di dati bitmap dell'immagine rappresenta un singolo pixel. Il valore di quel byte è il numero della voce della tavolozza dei colori da utilizzare tra le 256 voci rappresentate da bmciColors.
|Formato a 24 bit (TrueColor)|Queste bitmap possono avere un massimo di 2^24 colori (biBitCount == 24).Ogni sequenza di tre byte nell'array di dati bitmap rappresenta le intensità relative delle tre tonalità primarie di un pixel. Le tonalità sono descritte come valori compresi tra 0 e 255 e sono memorizzate nei tre byte nell'ordine Blu, Verde e Rosso. Questa è una distinzione importante, perché la maggior parte dei riferimenti ai colori in Windows utilizza l'ordine opposto: rosso/verde/blu, quindi pensa a "BGR" quando lavori con immagini TrueColor invece di "RGB". È possibile specificare una tavolozza di colori per accelerare il processo di disegno per Windows, nel qual caso biClrUsed non sarà 0. Ma come puoi vedere, non è necessario, poiché i dati dei pixel stessi contengono le informazioni sul colore.
|Formato a 32 bit|Le immagini a 32 bit hanno un massimo di 2^24 colori (biBitCount == 24).

## Riferimenti ##
* [Bitmap indipendenti dal dispositivo - Di Microsoft](https://docs.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

