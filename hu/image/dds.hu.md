{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DDS fájlformátum - DirectDraw felületi képfájl",
  "description":"További információ a DDS fájlformátumról és az API-król, amelyek DDS fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Mi az a DDS fájl?

A DDS fájl egy raszteres képfájl, amely a DirectDraw Surface (DDS) tárolóformátumot használja. Tömörítetlen és tömörített (DXTn) textúrákat tárol, és különböző típusú adatokat valósít meg különböző típusú adatok tárolására. Számos különböző típusú adatot is támogat, például egyrétegű textúrákat, mipmaps textúrákat, kockatérképeket, térfogattérképeket és textúratömböket. Ez lehetővé teszi, hogy a DDS-fájlok a digitális fényképek és a Windows asztali hátterek mellett videojáték-textúraegység-modelleket is tároljanak. A DDS fájlformátumot a Microsoft fejlesztette ki a DirectX SDK-val való használatra.

## DDS fájlformátum

A DDS fájlok bináris fájlként kerülnek mentésre, és használhatók a DirectX SDK-val. A DirectX erejét használja fel valós idejű renderelő alkalmazások, például 3D játékok fejlesztésére.

### DDS fájl elrendezés

A [DDS-fájl elrendezését] (https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) a Microsoft részletesen dokumentálta. Egy bináris DDS fájl a következő információkat tartalmazza.

* Egy duplaszó (varázsszám), amely a négy karakteres „DDS” kódértéket tartalmazza (0x20534444).
* A fájlban található adatok leírása.

A DDS_HEADER az adatokat, a DDS_PIXELFORMAT pedig a pixelformátumot írja le. Mindkettő az elavult DDSURFACEDESC2, DDSCAPS2 és DDPIXELFORMAT DirectDraw 7 struktúrákat váltja fel.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

A [DDS fájlformátum programozási útmutatója] (https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) részletesebben kidolgozza ennek a fájlformátumnak a technikai részleteit.

## Hivatkozások

* [DDS – a Wikipedia által](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [ZSoft PCX fájlformátumú műszaki kézikönyv] (http://qzx.com/pc-gpe/pcx.txt)

