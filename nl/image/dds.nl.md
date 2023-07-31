{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DDS-bestandsindeling - DirectDraw Surface Image-bestand",
  "description":"Meer informatie over DDS-bestandsindeling en API's die DDS-bestanden kunnen maken en openen.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Wat is een DDS-bestand?

Een DDS-bestand is een rasterafbeeldingsbestand dat gebruikmaakt van het DirectDraw Surface (DDS) containerformaat. Het slaat ongecomprimeerde en gecomprimeerde (DXTn) texturen op en implementeert verschillende typen voor het opslaan van verschillende soorten gegevens. Het ondersteunt ook verschillende soorten gegevens, zoals texturen met één laag, texturen met mipmaps, kubuskaarten, volumekaarten en textuurarrays. Hierdoor kunnen de DDS-bestanden naast digitale foto's en Windows-bureaubladachtergronden ook texture-eenheidmodellen voor videogames opslaan. Het DDS-bestandsformaat is door Microsoft ontwikkeld om te worden gebruikt met DirectX SDK.

## DDS-bestandsindeling

DDS-bestanden worden opgeslagen als binaire bestanden en kunnen worden gebruikt met DirectX SDK. Het maakt gebruik van de kracht van DirectX om realtime-renderingtoepassingen zoals 3D-games te ontwikkelen.

### DDS-bestandsindeling

De [DDS-bestandsindeling](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) is door Microsoft in detail gedocumenteerd. Een binair DDS-bestand bevat de volgende informatie.

* Een DWORD (magisch getal) met de viercijferige codewaarde 'DDS' (0x20534444).
* Een beschrijving van de gegevens in het bestand.

De DDS_HEADER beschrijft de gegevens en de DDS_PIXELFORMAT beschrijft het pixelformaat. Deze vervangen beide de verouderde DDSURFACEDESC2-, DDSCAPS2- en DDPIXELFORMAT DirectDraw 7-structuren.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

De [programmeergids van DDS-bestandsformaat](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) werkt de technische details van dit bestandsformaat verder uit.

## Referenties

* [DDS - Door Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [ZSoft PCX-bestandsindeling technische referentiehandleiding](http://qzx.com/pc-gpe/pcx.txt)

