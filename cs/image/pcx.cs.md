{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PCX - soubor bitmapového obrázku štětce",
  "description":"Další informace o formátu souborů PCX a rozhraních API, která mohou vytvářet a otevírat soubory PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Co je soubor PCX?

Soubor PCX, soubor Picture Exchange, je formát souboru rastrového obrázku, který byl použit jako nativní formát souboru pro aplikaci PC Paintbrush. Byl vyvinut společností ZSoft Corporation, USA pro platformy DOS a Windows a byl přijat jako hlavní formát obrazových souborů před příchodem [BMP](/cs/image/bmp/), [JPEG](/cs/image/jpeg/) a [ PNG](/cs/image/png/) formáty souborů. Soubory PCX mají menší velikost, protože jsou komprimovány pomocí kódování RLE. Používá se ve vícestránkovém souboru [DCX](/cs/image/dcx/), který se primárně používá k vytváření digitálních faxových souborů.

## Formát souboru PCX

Soubory PCX se ukládají na disk v binárním formátu souboru. Vnitřní struktura formátu souboru se řídí řazením bajtů malým endianem a má následující tři části:

**`Záhlaví PCX`** - Záhlaví PCX je dlouhé 128 bajtů. Obsahuje identifikátor, číslo verze, rozměry obrázku, 16 barev palety, počet barevných rovin a bitovou hloubku každé roviny a hodnotu pro metodu komprese.

Záhlaví PCX je znázorněno níže s odkazem z Encyklopedie formátů grafických souborů (2. vydání).
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

**`Image Data`** - Obrazová data PCX následují hned za záhlavím. Obrazová data mohou být komprimována v závislosti na nastavení pole v záhlaví. Uložení dat v souboru PCX závisí na počtu zadaných barevných rovin. Obrazová data jsou uspořádána do řádků. V případě více rovin jsou tyto uloženy po rovině v řadě v sekvenčním uspořádání červených, zelených a modrých dat. Tento vzor se opakuje pro každý řádek v rovině.

## Reference

* [PCX – podle Wikipedie](https://en.wikipedia.org/wiki/PCX)

