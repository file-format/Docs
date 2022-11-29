{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DDS-filformat - DirectDraw Surface Image File",
  "description":"Läs mer om DDS-filformat och API:er som kan skapa och öppna DDS-filer.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Vad är DDS fil?

En DDS-fil är en rasterbildsfil som använder containerformatet DirectDraw Surface (DDS). Den lagrar okomprimerade och komprimerade (DXTn) texturer och implementerar olika typer för lagring av olika typer av data. Den stöder också flera olika typer av data, såsom enskiktstexturer, texturer med mipmaps, kubkartor, volymkartor och texturarrayer. Detta gör det möjligt för DDS-filerna att lagra texturenhetsmodeller för videospel förutom digitala foton och Windows skrivbordsbakgrunder. DDS-filformatet har utvecklats av Microsoft för att användas med DirectX SDK.

## DDS filformat

DDS-filer sparas som binära filer och kan användas med DirectX SDK. Den använder kraften hos DirectX för att utveckla realtidsrenderingsprogram som 3D-spel.

### DDS-fillayout

[DDS-fillayouten](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) har dokumenterats av Microsoft i detalj. En binär DDS-fil innehåller följande information.

* Ett DWORD (magiskt nummer) som innehåller kodvärdet 'DDS' med fyra tecken (0x20534444).
* En beskrivning av data i filen.

DDS_HEADER beskriver data och DDS_PIXELFORMAT beskriver pixelformat. Dessa båda ersätter de föråldrade strukturerna DDSURFACEDESC2, DDSCAPS2 och DDPIXELFORMAT DirectDraw 7.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[programmeringsguiden för DDS-filformat](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) utvecklar de tekniska detaljerna för detta filformat ytterligare.

## Referenser

* [DDS - av Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [ZSoft PCX File Format Technical Reference Manual](http://qzx.com/pc-gpe/pcx.txt)

