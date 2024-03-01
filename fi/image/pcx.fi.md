{
  "date": "2022-03-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCX-tiedostomuoto - sivellin bittikarttakuvatiedosto",
  "description": "Opi PCX-tiedostomuodosta ja API:ista, jotka voivat luoda ja avata PCX-tiedostoja.",
  "linktitle": "PCX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pc-fix"
}
},
  "lastmod": "2022-03-16"
}

## Mikä on PCX-tiedosto?

PCX-tiedosto, Picture Exchange -tiedosto, on rasterikuvatiedostomuoto, jota käytettiin alkuperäisenä tiedostomuotona PC Paintbrush -sovelluksessa. Sen on kehittänyt ZSoft Corporation, USA DOS- ja Windows-alustoille, ja se hyväksyttiin pääasialliseksi kuvantamistiedostomuodoksi ennen tiedostomuotojen [BMP](/image/bmp/), [JPEG](/image/jpeg/) ja [PNG](/image/png/) saapumista. PCX-tiedostot ovat kooltaan pienempiä, koska ne pakataan RLE-koodauksella. Sitä käytetään monisivuisessa [DCX](/image/dcx/)-tiedostossa, jota käytetään ensisijaisesti digitaalisten faksitiedostojen luomiseen.

## PCX tiedostomuoto

PCX-tiedostot tallennetaan levylle binääritiedostomuodossa. Sisäinen tiedostomuotorakenne noudattaa vähän endian tavujärjestystä, ja siinä on seuraavat kolme osaa:

**`PCX-otsikko`** - PCX-otsikko on 128 tavua pitkä. Se sisältää tunnisteen, versionumeron, kuvan mitat, 16 paletin väriä, numerotasot ja kunkin tason bittisyvyyden sekä pakkausmenetelmän arvon.

PCX-ylätunniste on alla näkyvän kuvan mukainen viittauksella Encyclopedia of Grafiikkatiedostomuotoihin (2. painos).
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

**`Image Data`** - PCX-kuvadata seuraa heti otsikon jälkeen. Kuvatiedot voidaan pakata otsikon kenttäasetuksen mukaan. Tietojen tallennus PCX-tiedostoon riippuu määritettyjen väritasojen lukumäärästä. Kuvatiedot on järjestetty riveihin. Jos on useita tasoja, ne tallennetaan tasoittain riviin punaisen, vihreän ja sinisen datan järjestyksessä. Tämä kuvio toistetaan jokaiselle tason riville.

## Viitteet

* [PCX - Wikipedia](https://en.wikipedia.org/wiki/PCX)


