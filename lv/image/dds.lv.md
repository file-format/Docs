{
  "date": "2022-04-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DDS faila formāts - DirectDraw virsmas attēla fails",
  "description": "Uzziniet par DDS faila formātu un API, kas var izveidot un atvērt DDS failus.",
  "linktitle": "DDS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dd-lvs"
}
},
  "lastmod": "2022-04-02"
}

## Kas ir DDS fails?

DDS fails ir rastra attēla fails, kas izmanto DirectDraw Surface (DDS) konteinera formātu. Tas saglabā nesaspiestas un saspiestas (DXTn) tekstūras un ievieš dažādus veidus dažāda veida datu glabāšanai. Tā atbalsta arī dažādu veidu datus, piemēram, viena slāņa faktūras, tekstūras ar mipkartēm, kubu kartes, apjoma kartes un tekstūru masīvus. Tas ļauj DDS failos saglabāt videospēļu tekstūras vienību modeļus papildus digitālajiem fotoattēliem un Windows darbvirsmas foniem. DDS faila formātu izstrādāja Microsoft, lai to izmantotu kopā ar DirectX SDK.

## DDS faila formāts

DDS faili tiek saglabāti kā bināri faili, un tos var izmantot kopā ar DirectX SDK. Tas izmanto DirectX jaudu, lai izstrādātu reāllaika renderēšanas lietojumprogrammas, piemēram, 3D spēles.

### DDS faila izkārtojums

Microsoft ir detalizēti dokumentējusi [DDS file layout](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout). Binārais DDS fails satur šādu informāciju.

 * DWORD (maģisks skaitlis), kas satur četru rakstzīmju koda vērtību DDS” (0x20534444).
 * A description of the data in the file.

DDS_HEADER apraksta datus un DDS_PIXELFORMAT apraksta pikseļu formātu. Tās abas aizstāj novecojušās DDSURFACEDESC2, DDSCAPS2 un DDPIXELFORMAT DirectDraw 7 struktūras.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[programming guide of DDS file format](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) ir sīkāk izstrādāta šī faila formāta tehniskā informācija.

## Atsauces

* [DDS — Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)

* [ZSoft PCX faila formāta tehniskā uzziņu rokasgrāmata] (http://qzx.com/pc-gpe/pcx.txt)


