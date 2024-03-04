{
  "date": "2022-03-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCX failo formatas – teptuko bitmap vaizdo failas",
  "description": "Sužinokite apie PCX failo formatą ir API, kurios gali kurti ir atidaryti PCX failus.",
  "linktitle": "PCX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pc-ltx"
}
},
  "lastmod": "2022-03-16"
}

## Kas yra PCX failas?

PCX failas, Picture Exchange failas, yra rastrinio vaizdo failo formatas, kuris buvo naudojamas kaip vietinis PC Paintbrush programos failo formatas. Jį sukūrė ZSoft Corporation, JAV, skirtą DOS ir Windows platformoms, ir jis buvo priimtas kaip pagrindinis vaizdo failo formatas prieš pradedant naudoti [BMP](/image/bmp/), [JPEG](/image/jpeg/) ir [PNG](/image/png/) failų formatus. PCX failai yra mažesnio dydžio, nes jie suglaudinami naudojant RLE kodavimą. Jis naudojamas kelių puslapių [DCX](/image/dcx/) faile, kuris pirmiausia naudojamas skaitmeniniams fakso failams kurti.

## PCX failo formatas

PCX failai išsaugomi diske dvejetainiu failo formatu. Vidinio failo formato struktūra atitinka mažą baitų tvarką ir turi šiuos tris skyrius:

**`PCX antraštė`** – PCX antraštė yra 128 baitų ilgio. Jame yra identifikatorius, versijos numeris, vaizdo matmenys, 16 paletės spalvų, skaičių spalvų plokštumos ir kiekvienos plokštumos bitų gylis bei suspaudimo metodo reikšmė.

PCX antraštė yra tokia, kaip parodyta toliau su nuoroda iš grafinių failų formatų enciklopedijos (2-asis leidimas).
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

**`Vaizdo duomenys`** – PCX vaizdo duomenys pateikiami iškart po antraštės. Vaizdo duomenys gali būti suspausti, atsižvelgiant į lauko nustatymą antraštėje. Duomenų saugojimas PCX faile priklauso nuo nurodytų spalvų plokštumų skaičiaus. Vaizdo duomenys suskirstyti į eilutes. Jei yra kelios plokštumos, jos saugomos pagal plokštumą eilutėje, nuosekliai išdėstant raudonos, žalios ir mėlynos spalvos duomenis. Šis modelis kartojamas kiekvienai plokštumos linijai.

## Nuorodos

* [PCX – Vikipedija](https://en.wikipedia.org/wiki/PCX)


