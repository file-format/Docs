{
  "date": "2020-01-10",
  "keywords": [
"dib failą",
"dib failo formatas",
"kas yra dib failas",
"failą",
"dib pavyzdys",
"dib failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DIB",
  "description": "Sužinokite apie DIB failo formatą ir API, kurios gali kurti ir atidaryti DIB failus.",
  "linktitle": "DIB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-di-ltb"
}
},
  "lastmod": "2020-01-10"
}

## Kas yra DIB failas?

Nuo įrenginio nepriklausoma bitmap (DIB) yra rastrinio vaizdo failas, savo struktūra panaši į standartinius bitmap failus ([BMP]()/image/bmp/)). Jame yra spalvų lentelė, kurioje aprašomas RGB spalvų susiejimas su pikselių reikšmėmis. Tai leidžia DIB vaizduoti vaizdą bet kuriame įrenginyje. Jį galima atidaryti su beveik visomis programomis, kurios gali atidaryti standartinį BMP failą Windows ir MacOS. DIB yra dvejetainiai failai ir turi sudėtingą failo formatą, panašų į BMP. DIB vaizdai nepriklauso nuo atvaizdavimo įrenginių išvesties galimybių spalvų gylio ir pikselių colyje atžvilgiu.

## DIB failo formato specifikacijos ##
DIB yra šios spalvos ir matmenų informacija:

  * Įrenginio, kuriame buvo sukurtas stačiakampis vaizdas, spalvų formatas.
  * Įrenginio, kuriame buvo sukurtas stačiakampis vaizdas, skiriamoji geba.
  * Įrenginio, kuriame buvo sukurtas vaizdas, paletė.
  * Bitų masyvas, susiejantis raudoną, žalią, mėlyną (RGB) trigubas su pikseliais stačiakampiame vaizde.
  * Duomenų glaudinimo identifikatorius, nurodantis duomenų glaudinimo schemą (jei yra), naudojamą bitų masyvo dydžiui sumažinti.

### DIB duomenų bloko formatas ###

DIB yra atminties bloko kontekste, palyginti su .DIB failais, saugomais diske. Atminties bloką sudaro struktūra, kuri atitinka Windows API specifikacijas DIB. Faktinį DIB sudaro:
  * Antraštė
  * Spalvų paletė
  * Pikselių duomenys

Praktiškai darbas su paletės, antraštės ir vaizdo duomenimis atliekamas taip, lyg tai būtų trys atskiri atminties blokai. Šio bendro atminties bloko rankena priskiriama naudojant GlobalAlloc ir žinoma kaip HDIB, kuri naudojama antraštės, spalvų lentelės ir pikselių duomenims išgauti ir dirbti su jais.

### Struktūros ###
DIB esanti informacija yra pavaizduota skirtingomis struktūromis. Jie apima:

BITMAPIinfo – apibrėžia DIB matmenų ir spalvų informaciją
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Jį sudaro BITMAPINFOHEADER:

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
po to seka dvi ar daugiau RGBQAD struktūrų.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Duomenų bitai ###
|Bits|Aprašymas|
---|---|
|1 bito formatas (vienspalvis)|Vienspalviai taškai susideda iš dviejų spalvų (juodos ir baltos). Dėl šio riboto spalvų skaičiaus šie taškai užima mažiau vietos diske. BitBitCount grąžina true arba false, kad pavaizduotų abi spalvas. Dauguma programų visiškai praleidžia paletę, jei bitBitCount==1.
|4 bit format (VGA or 16 color)|Each byte of image data represents two pixels and bitBitCount==4. Šie bitai rodo pikselio spalvą mažėjančia tvarka.
|8 bitų formatas (256 spalvos)|Šis 8 bitų formatas gali rodyti daugiausia 256 spalvas. Kiekvienas baitas vaizdo taškinės diagramos duomenų masyve reiškia vieną pikselį. To baito reikšmė yra spalvų paletės įrašo, kuris bus naudojamas iš 256 įrašų, nurodytas bmciColors, skaičius.
|24 bit format (TrueColor)|These bitmaps can have a maximum of 2^24 colors (biBitCount == 24).Each three-byte sequence in the bitmap data array represents the relative intensities of the three primary hues of a pixel. The hues are described as values ranging from 0 to 255 and are stored in the three bytes in the order Blue, Green and Red. This is an important distinction, because most references to colors in Windows use the opposite order: Red/Green/Blue, so think "BGR" when working with TrueColor images instead of "RGB". A color palette can be specified to accelerate the drawing process for Windows, in which case biClrUsed will not be 0. Bet kaip matote, to nereikia, nes pačiuose pikselių duomenyse yra informacijos apie spalvą.
|32 bitų formatas|32 bitų vaizdai turi daugiausiai 2^24 spalvų (biBitCount == 24).

## Nuorodos Nr.
  * [Nuo įrenginio nepriklausomos bitų schemos – Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

