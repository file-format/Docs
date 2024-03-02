{
  "date": "2022-03-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid PCX - Comhad Íomhá Giotán Scuab Péinte",
  "description": "Foghlaim faoi fhormáid comhaid PCX agus APIs ar féidir comhaid PCX a chruthú agus a oscailt.",
  "linktitle": "PCX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pc-gax"
}
},
  "lastmod": "2022-03-16"
}

## Cad is comhad PCX ann?

Is formáid comhaid íomhá raster é comhad PCX, comhad Malartú Pictiúr, a úsáideadh mar fhormáid comhaid dhúchais le haghaidh feidhmchlár PC Paintbrush. D'fhorbair ZSoft Corporation, USA é le haghaidh ardáin DOS agus Windows agus glacadh leis mar phríomhfhormáid comhaid íomháithe sular tháinig [BMP](/image/bmp/), [JPEG](/image/jpeg/), agus [PNG](/image/png/) formáidí comhaid. Tá comhaid PCX níos lú i méid mar go bhfuil siad comhbhrúite ag baint úsáide as an ionchódú RLE. Úsáidtear é sa chomhad il-leathanach [DCX](/image/dcx/) a úsáidtear go príomha chun comhaid facs digiteacha a chruthú.

## Formáid Comhaid PCX

Déantar comhaid PCX a shábháil ar diosca i bhformáid dhénártha comhaid. Ní leanann an struchtúr formáid comhaid inmheánach ach beagán ordú beart endian agus tá na trí chuid seo a leanas ann:

**`Ceanntásc PCX`** - Tá Ceanntásc PCX 128 beart ar fad. Cuimsíonn sé aitheantóir, uimhir leagain, toisí íomhá, 16 dathanna pailéad, plánaí datha uimhreach agus doimhneacht giotán gach eitleáin, agus luach modh comhbhrú.

Tá Ceanntásc PCX mar a thaispeántar thíos le tagairt ó Encyclopedia de formáidí comhaid grafaic (2ú eag.).
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

**`Sonraí Íomhá`** - leanann sonraí íomhá PCX díreach tar éis an ceanntásca. Is féidir na sonraí íomhá a chomhbhrú ag brath ar an socrú réimse sa cheanntásc. Braitheann stóráil sonraí sa chomhad PCX ar líon na n-eitleán dath sonraithe. Eagraítear sonraí íomhá i sraitheanna. I gcás eitleáin iolracha, déantar iad seo a stóráil ar eitleán laistigh de shraith i socrú seicheamhach de shonraí dearga, glasa agus gorm. Athdhéantar an patrún seo do gach líne san eitleán.

## Tagairtí

* [PCX - Le Vicipéid]( https://ga.wikipedia.org/wiki/PCX)


