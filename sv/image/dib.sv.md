{
  "date" : "2020-01-10",
  "keywords" :[ "dib-fil", "dib-filformat", "vad är en dib-fil", "fil", "dib-exempel", "dib-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Läs mer om DIB-filformat och API:er som kan skapa och öppna DIB-filer.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Vad är DIB fil?

En enhetsoberoende bitmapp (DIB) är en rasterbildsfil som i struktur liknar standardbitmappsfilerna ([BMP]()/image/bmp/)). Den innehåller en färgtabell som beskriver mappningen av RGB-färger till pixelvärdena. Detta gör att DIB kan representera bilder på vilken enhet som helst. Den kan öppnas med nästan alla applikationer som kan öppna en standard BMP-fil på Windows såväl som macOS. DIB är binära filer och har ett komplext filformat som liknar BMP. DIB-bilder är oberoende av utdatakapaciteten hos renderingsenheter när det gäller färgdjup och pixel per tum.

## DIB-filformatspecifikationer ##
En DIB innehåller följande färg- och dimensionsinformation:

* Färgformatet för enheten där den rektangulära bilden skapades.
* Upplösningen för enheten där den rektangulära bilden skapades.
* Paletten för enheten där bilden skapades.
* En uppsättning bitar som mappar röda, gröna, blå (RGB) tripletter till pixlar i den rektangulära bilden.
* En datakomprimeringsidentifierare som indikerar datakomprimeringsschemat (om sådant finns) som används för att minska storleken på arrayen av bitar.

### DIB-datablockformat ###

DIB kommer i sammanhanget med minnesblock jämfört med .DIB-filer lagrade på skiva. Minnesblocket består av struktur som är i enlighet med Windows API-specifikationer för DIB:er. Faktisk DIB består av:
* En rubrik
* Färgpalett
* Pixeldata

Praktiskt taget arbetar man med palett-, rubrik- och bilddata som om de vore tre separata minnesblock. Ett handtag till detta gemensamma minnesblock tilldelas med GlobalAlloc och är känt som HDIB, som används för att extrahera och arbeta med rubriken, färgtabellen och pixeldata.

### Strukturer ###
Information som finns i en DIB representeras av olika strukturer. Dessa inkluderar:

BITMAPInfo - Definierar dimension och färginformation för en DIB
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Den består av en BITMAPINFOHEADER:

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
följt av två eller flera RGBQAD-strukturer.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Databitar ###
|Bits|Beskrivning|
---|---|
|1-bitars format (monokrom)|Monokroma bitmappar består av två färger (svart och vit). På grund av detta begränsade antal färger tar dessa bitmappar mindre plats på skivan. BitBitCount returnerar sant eller falskt för representation av båda färgerna. De flesta av applikationerna hoppar över paletten helt om bitBitCount==1.
|4 bitars format (VGA eller 16 färger)|Varje byte med bilddata representerar två pixlar och bitBitCount==4. Dessa bitar representerar färgen på pixeln i fallande ordning.
|8-bitarsformat (256 färger)|Detta 8-bitarsformat kan representera maximalt 256 färger. Varje byte i bildens bitmappsdatamatris representerar en enda pixel. Värdet på den byten är numret på färgpalettposten som ska användas från de 256 posterna som representeras av bmciColors.
|24-bitarsformat (TrueColor)|Dessa bitmappar kan ha maximalt 2^24 färger (biBitCount == 24). Varje trebytesekvens i bitmappsdatamatrisen representerar de relativa intensiteterna för de tre primära nyanserna i en pixel. Nyanserna beskrivs som värden från 0 till 255 och lagras i de tre byten i ordningen blå, grön och röd. Detta är en viktig skillnad, eftersom de flesta referenser till färger i Windows använder motsatt ordning: Röd/Grön/Blå, så tänk "BGR" när du arbetar med TrueColor-bilder istället för "RGB". En färgpalett kan specificeras för att påskynda ritprocessen för Windows, i vilket fall biClrUsed inte kommer att vara 0. Men som du kan se behövs den inte, eftersom själva pixeldatan innehåller färginformationen.
|32 bitars format|32 bitars bilder har maximalt 2^24 färger (biBitCount == 24).

## Referenser ##
* [Enhetsoberoende bitmappar - av Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

