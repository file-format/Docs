{
  "date": "2020-01-10",
  "keywords": [
"dib fil",
"dib filformat",
"hvad er en dib-fil",
"fil",
"dib eksempel",
"dib filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DIB",
  "description": "Lær om DIB filformat og API'er, der kan oprette og åbne DIB filer.",
  "linktitle": "DIB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-di-dab"
}
},
  "lastmod": "2020-01-10"
}

## Hvad er en DIB fil?

En enhedsuafhængig bitmap (DIB) er en rasterbilledfil, der i struktur ligner standard bitmapfiler ([BMP]()/image/bmp/)). Den indeholder en farvetabel, der beskriver tilknytningen af RGB-farver til pixelværdierne. Dette gør det muligt for DIB at repræsentere billede på enhver enhed. Den kan åbnes med næsten alle programmer, der kan åbne en standard BMP-fil på Windows såvel som macOS. DIB er binære filer og har et komplekst filformat, der ligner BMP. DIB-billeder er uafhængige af gengivelsesenheders output-kapaciteter med hensyn til farvedybde og pixel-per-inch.

## DIB-filformatspecifikationer ##
En DIB indeholder følgende farve- og dimensionsoplysninger:

  * Farveformatet på den enhed, hvorpå det rektangulære billede blev oprettet.
  * Opløsningen af den enhed, hvorpå det rektangulære billede blev oprettet.
  * Paletten for den enhed, hvorpå billedet blev oprettet.
  * En række bits, der kortlægger røde, grønne, blå (RGB) tripletter til pixels i det rektangulære billede.
  * Et datakomprimerings-id, der angiver datakomprimeringsskemaet (hvis nogen), der bruges til at reducere størrelsen af arrayet af bit.

### DIB-datablokformat ###

DIB kommer i sammenhæng med hukommelsesblok sammenlignet med .DIB-filer gemt på disk. Hukommelsesblokken består af en struktur, som er i overensstemmelse med Windows API-specifikationerne for DIB'er. Faktisk DIB består af:
  * Et overskrift
  * Farvepalet
  * Pixeldata

I praksis foregår arbejdet med palette-, header- og billeddata, som om de var tre separate hukommelsesblokke. Et håndtag til denne fælles hukommelsesblok tildeles ved hjælp af GlobalAlloc og er kendt som HDIB, som bruges til at udtrække og arbejde med header, farvetabel og pixeldata.

### Strukturer ###
Information indeholdt i en DIB er repræsenteret af forskellige strukturer. Disse omfatter:

BITMAPInfo - Definerer dimension og farveinformation for en DIB'er
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Den består af en BITMAPINFOHEADER:

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
efterfulgt af to eller flere RGBQAD-strukturer.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Databits ###
|Bits|Beskrivelse|
---|---|
|1-bit format (monokrom)|Monokrom bitmaps består af to farver (sort og hvid). På grund af dette begrænsede antal farver tager disse bitmaps mindre plads på disken. BitBitCount returnerer sand eller falsk for repræsentation af begge farver. De fleste af applikationerne springer paletten helt over, hvis bitBitCount==1.
|4 bit format (VGA or 16 color)|Each byte of image data represents two pixels and bitBitCount==4. Disse bits repræsenterer farven på pixlen i faldende rækkefølge.
|8 bit format (256 farver)|Dette 8-bit format kan repræsentere maksimalt 256 farver. Hver byte i billedets bitmapdataarray repræsenterer en enkelt pixel. Værdien af den byte er nummeret på farvepaletten, der skal bruges fra de 256 indgange som repræsenteret af bmciColors.
|24 bit format (TrueColor)|These bitmaps can have a maximum of 2^24 colors (biBitCount == 24).Each three-byte sequence in the bitmap data array represents the relative intensities of the three primary hues of a pixel. The hues are described as values ranging from 0 to 255 and are stored in the three bytes in the order Blue, Green and Red. This is an important distinction, because most references to colors in Windows use the opposite order: Red/Green/Blue, so think "BGR" when working with TrueColor images instead of "RGB". A color palette can be specified to accelerate the drawing process for Windows, in which case biClrUsed will not be 0. Men som du kan se, er det ikke nødvendigt, da selve pixeldataene indeholder farveinformationen.
|32 bit format|32 bit billeder har et maksimum på 2^24 farver (biBitCount == 24).

## Referencer ##
  * [Enhedsuafhængige bitmaps - af Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

