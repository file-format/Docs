{
  "date": "2022-04-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DDS-filformat - DirectDraw overfladebilledfil",
  "description": "Lær om DDS-filformat og API'er, der kan oprette og åbne DDS-filer.",
  "linktitle": "DDS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dd-das"
}
},
  "lastmod": "2022-04-02"
}

## Hvad er en DDS fil?

En DDS-fil er en rasterbilledfil, der bruger DDS-containerformatet (DirectDraw Surface). Den gemmer ukomprimerede og komprimerede (DXTn) teksturer og implementerer forskellige typer til lagring af forskellige typer data. Det understøtter også flere forskellige typer data, såsom enkeltlagsteksturer, teksturer med mipmaps, kubekort, volumenkort og teksturarrays. Dette gør det muligt for DDS-filerne at gemme videospilteksturenhedsmodeller ud over digitale fotos og Windows-skrivebordsbaggrunde. DDS-filformatet blev udviklet af Microsoft til brug med DirectX SDK.

## DDS filformat

DDS-filer gemmes som binære filer og kan bruges med DirectX SDK. Det udnytter kraften fra DirectX til at udvikle realtidsgengivelsesapplikationer såsom 3D-spil.

### DDS-fillayout

[DDS file layout](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) er blevet dokumenteret af Microsoft i detaljer. En binær DDS-fil indeholder følgende information.

 * Et DWORD (magisk tal), der indeholder kodeværdien på fire tegn 'DDS' (0x20534444).
 * A description of the data in the file.

DDS_HEADER beskriver dataene, og DDS_PIXELFORMAT beskriver pixelformatet. Disse erstatter begge de forældede DDSURFACEDESC2-, DDSCAPS2- og DDPIXELFORMAT DirectDraw 7-strukturer.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[programming guide of DDS file format](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) uddyber yderligere de tekniske detaljer i dette filformat.

## Referencer

* [DDS - af Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
