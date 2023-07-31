{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier DDS- Fișier imagine DirectDraw Surface",
  "description":"Aflați despre formatul de fișier DDS și despre API-urile care pot crea și deschide fișiere DDS.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Ce este un fișier DDS?

Un fișier DDS este un fișier imagine raster care utilizează formatul de container DirectDraw Surface (DDS). Stochează texturi necomprimate și comprimate (DXTn) și implementează diferite tipuri pentru stocarea diferitelor tipuri de date. De asemenea, acceptă mai multe tipuri diferite de date, cum ar fi texturi cu un singur strat, texturi cu mipmaps, hărți cub, hărți de volum și matrice de texturi. Acest lucru permite fișierelor DDS să stocheze modele de unități de textură pentru jocuri video, pe lângă fotografiile digitale și fundalurile desktop Windows. Formatul de fișier DDS a fost dezvoltat de Microsoft pentru a fi utilizat cu DirectX SDK.

## Format de fișier DDS

Fișierele DDS sunt salvate ca fișiere binare și pot fi utilizate cu DirectX SDK. Utilizează puterea DirectX pentru a dezvolta aplicații de randare în timp real, cum ar fi jocurile 3D.

### Aspect fișier DDS

[Aspectul fișierului DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) a fost documentat de Microsoft în detaliu. Un fișier DDS binar conține următoarele informații.

* Un DWORD (număr magic) care conține valoarea codului de patru caractere „DDS” (0x20534444).
* O descriere a datelor din fișier.

DDS_HEADER descrie datele, iar DDS_PIXELFORMAT descrie formatul pixelilor. Ambele înlocuiesc structurile depreciate DDSURFACEDESC2, DDSCAPS2 și DDPIXELFORMAT DirectDraw 7.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[Ghidul de programare al formatului de fișier DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) elaborează în continuare detaliile tehnice ale acestui format de fișier.

## Referințe

* [DDS - După Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [Manual de referință tehnic pentru formatul fișierului PCX ZSoft](http://qzx.com/pc-gpe/pcx.txt)

