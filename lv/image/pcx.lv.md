{
  "date": "2022-03-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCX faila formāts — otas bitkartes attēla fails",
  "description": "Uzziniet par PCX failu formātu un API, kas var izveidot un atvērt PCX failus.",
  "linktitle": "PCX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pc-lvx"
}
},
  "lastmod": "2022-03-16"
}

## Kas ir PCX fails?

PCX fails, Picture Exchange fails, ir rastra attēla faila formāts, kas tika izmantots kā vietējais faila formāts PC Paintbrush lietojumprogrammai. To izstrādāja ZSoft Corporation, ASV DOS un Windows platformām, un tas tika pieņemts kā galvenais attēlveidošanas faila formāts pirms [BMP](/image/bmp/), [JPEG](/image/jpeg/) un [PNG](/image/png/) failu formātu ienākšanas. PCX faili ir mazāki, jo tie tiek saspiesti, izmantojot RLE kodējumu. To izmanto vairāku lappušu failā [DCX](/image/dcx/), ko galvenokārt izmanto digitālo faksa failu izveidei.

## PCX faila formāts

PCX faili tiek saglabāti diskā binārā faila formātā. Iekšējā faila formāta struktūra atbilst mazajai baitu secībai, un tai ir šādas trīs sadaļas:

**`PCX galvene`** — PCX galvene ir 128 baitus gara. Tas satur identifikatoru, versijas numuru, attēla izmērus, 16 paletes krāsas, numuru krāsu plaknes un katras plaknes bitu dziļumu, kā arī saspiešanas metodes vērtību.

PCX galvene ir tāda, kā parādīts tālāk ar atsauci no grafikas failu formātu enciklopēdijas (2. izdevums).
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

**`Attēla dati`** — PCX attēla dati seko tieši aiz galvenes. Attēla dati var būt saspiesti atkarībā no lauka iestatījuma galvenē. Datu glabāšana PCX failā ir atkarīga no norādīto krāsu plakņu skaita. Attēlu dati ir sakārtoti rindās. Vairāku plakņu gadījumā tās tiek saglabātas pa plaknēm rindā secīgā sarkano, zaļo un zilo datu izkārtojumā. Šis modelis tiek atkārtots katrai plaknes līnijai.

## Atsauces

* [PCX — Wikipedia](https://en.wikipedia.org/wiki/PCX)


