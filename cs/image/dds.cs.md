{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru DDS - DirectDraw Surface Image File",
  "description":"Další informace o formátu souborů DDS a rozhraních API, která mohou vytvářet a otevírat soubory DDS.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## Co je soubor DDS?

Soubor DDS je soubor rastrového obrázku, který využívá formát kontejneru DirectDraw Surface (DDS). Ukládá nekomprimované a komprimované (DXTn) textury a implementuje různé typy pro ukládání různých typů dat. Podporuje také několik různých typů dat, jako jsou jednovrstvé textury, textury s mipmapami, krychlové mapy, objemové mapy a texturová pole. To umožňuje souborům DDS ukládat kromě digitálních fotografií a pozadí plochy Windows i modely texturových jednotek videoher. Formát souboru DDS byl vyvinut společností Microsoft pro použití s DirectX SDK.

## Formát souboru DDS

Soubory DDS se ukládají jako binární soubory a lze je použít s DirectX SDK. Využívá sílu DirectX k vývoji aplikací pro vykreslování v reálném čase, jako jsou 3D hry.

### Rozložení souboru DDS

[Rozvržení souboru DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) bylo podrobně zdokumentováno společností Microsoft. Binární soubor DDS obsahuje následující informace.

* DWORD (magické číslo) obsahující čtyřznakovou hodnotu kódu 'DDS' (0x20534444).
* Popis dat v souboru.

DDS_HEADER popisuje data a DDS_PIXELFORMAT popisuje formát pixelů. Oba nahrazují zastaralé struktury DDSURFACEDESC2, DDSCAPS2 a DDPIXELFORMAT DirectDraw 7.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[Průvodce programováním formátu souboru DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) dále rozvádí technické podrobnosti tohoto formátu souboru.

## Reference

* [DDS – z Wikipedie](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [Technická referenční příručka formátu souborů ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)

