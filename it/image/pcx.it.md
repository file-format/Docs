{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file PCX - File immagine bitmap pennello",
  "description":"Scopri il formato di file PCX e le API che possono creare e aprire file PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Che cos'è un file PCX?

Un file PCX, Picture Exchange file, è un formato di file di immagine raster utilizzato come formato di file nativo per l'applicazione PC Paintbrush. È stato sviluppato da ZSoft Corporation, USA per piattaforme DOS e Windows ed è stato adottato come formato di file di imaging principale prima dell'arrivo di [BMP](/it/image/bmp/), [JPEG](/it/image/jpeg/) e [ PNG](/it/image/png/). I file PCX sono di dimensioni inferiori poiché vengono compressi utilizzando la codifica RLE. Viene utilizzato nel file multipagina [DCX](/it/image/dcx/) utilizzato principalmente per creare file fax digitali.

## Formato file PCX

I file PCX vengono salvati su disco in formato binario. La struttura del formato del file interno segue l'ordinamento dei byte little endian e ha le seguenti tre sezioni:

**`Intestazione PCX`** - Un'intestazione PCX è lunga 128 byte. Contiene un identificatore, un numero di versione, dimensioni dell'immagine, 16 colori della tavolozza, numero di piani di colore e profondità di bit di ciascun piano e un valore per il metodo di compressione.

L'intestazione PCX è come mostrato di seguito con riferimento dall'Enciclopedia dei formati di file grafici (2a ed.).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Dati immagine`** - I dati dell'immagine PCX seguono subito dopo l'intestazione. I dati dell'immagine possono essere compressi a seconda dell'impostazione in loco nell'intestazione. La memorizzazione dei dati nel file PCX dipende dal numero di piani colore specificati. I dati dell'immagine sono organizzati in righe. In caso di più piani, questi vengono memorizzati per piano all'interno di una riga in una disposizione sequenziale di dati rossi, verdi e blu. Questo schema viene ripetuto per ogni linea del piano.

## Riferimenti

* [PCX - Di Wikipedia](https://en.wikipedia.org/wiki/PCX)

