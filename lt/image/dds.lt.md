{
  "date": "2022-04-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DDS failo formatas - „DirectDraw“ paviršiaus vaizdo failas",
  "description": "Sužinokite apie DDS failo formatą ir API, kurios gali kurti ir atidaryti DDS failus.",
  "linktitle": "DDS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dd-lts"
}
},
  "lastmod": "2022-04-02"
}

## Kas yra DDS failas?

DDS failas yra rastrinio vaizdo failas, kuriame naudojamas DirectDraw Surface (DDS) konteinerio formatas. Jis saugo nesuspaustas ir suspaustas (DXTn) tekstūras ir įgyvendina skirtingus tipus, skirtus įvairių tipų duomenims saugoti. Ji taip pat palaiko kelių skirtingų tipų duomenis, tokius kaip vieno sluoksnio tekstūros, tekstūros su mipmaps, kubo žemėlapiai, tūrio žemėlapiai ir tekstūrų matricos. Tai leidžia DDS failuose saugoti vaizdo žaidimų tekstūros vienetų modelius, be skaitmeninių nuotraukų ir Windows darbalaukio fonų. DDS failo formatą sukūrė Microsoft, kad būtų galima naudoti su DirectX SDK.

## DDS failo formatas

DDS failai išsaugomi kaip dvejetainiai failai ir gali būti naudojami su DirectX SDK. Jis naudoja DirectX galią, kad sukurtų realaus laiko atvaizdavimo programas, pvz., 3D žaidimus.

### DDS failo išdėstymas

Microsoft išsamiai dokumentavo [DDS file layout](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout). Dvejetainiame DDS faile yra ši informacija.

 * DWORD (stebuklingas skaičius), kuriame yra keturių simbolių kodo reikšmė DDS (0x20534444).
 * A description of the data in the file.

DDS_HEADER aprašo duomenis, o DDS_PIXELFORMAT – pikselių formatą. Jie abu pakeičia pasenusias DDSURFACEDESC2, DDSCAPS2 ir DDPIXELFORMAT DirectDraw 7 struktūras.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[programming guide of DDS file format](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) išsamiau paaiškina šio failo formato techninę informaciją.

## Nuorodos

* [DDS – pateikė Vikipedija](https://en.wikipedia.org/wiki/DirectDraw_Surface)

* [ZSoft PCX failo formato techninis informacinis vadovas] (http://qzx.com/pc-gpe/pcx.txt)


