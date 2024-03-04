---
date: 2022-01-31
keywords: stp, .stp, stp file format, how to open stp files, .stp extension, stp extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP failo formaat
linktitle: STP
description: Luždirbti apie STP failo formatą ir API, kurios gali sukurti ir atidaryti STP failąs.
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Kas yra STP failas?

STP failas yra 3D CAD failas, naudojamas produkto duomenims keistis tarp CAD ir CAM programų. Jame yra informacijos apie 3D objektus ir jis išsaugomas panašiai kaip **STEP** failo formatas. STP failai palengvina keitimąsi duomenimis tarp programų pagal [STEP](/3d/step/) taikomųjų programų protokolus ISO 10303-2xx. Šis ISO apibrėžia duomenų pateikimo EXPRESS duomenų modeliavimo kalba kodavimo mechanizmą. STP failus galima atidaryti tokiose programose kaip **Autodesk Fusion 360**.

## STP failo formatas – daugiau informacijos

STP failai išsaugomi diske paprastu ASCII failo formatu. Juose pateikiama 3D modelių informacija kaip paprastas tekstas, kurį gali perskaityti CAD/CAM programos, skirtos šiems modeliams įkelti.

STP failai taip pat išsaugomi su plėtiniu .step ir susideda iš įrašų sekos. Svarbiausios šių failų savybės:

 * Simbolių rinkinys apibrėžiamas kaip ISO 10646 kodo taškai.
 * ISO-10303-21; yra pirmieji pirmojo įrašo simboliai.
 * Komentarai yra apsupti /* ir */ simboliais.
 * Paskutiniame įraše yra END-ISO-10303-21; jei STEP failas atitinka 2002 m. versiją.
 * Jei jis atitinka 2016 m. versiją, po END-ISO-10303-21; gali būti vienas ar daugiau skaitmeninių parašų. terminatorius.
 * Eilučių lūžiai žymimi \N\, o puslapių lūžiai – \F\.

## Atidarykite STP failus

STP failus galima atidaryti STP peržiūros priemonėse ir teksto rengyklėse.

### Atidarykite STP failus naudodami STP peržiūros priemones

Įvairios CAD programos gali atidaryti STP failus, kad juos būtų galima peržiūrėti Windows, MacOS ir Linux. Jie apima:

 * Autodesk Fusion 360. (keli platforma)
 * FreeCAD (keli platforma)
 * IMSI TurboCAD (Windows, Mac)
 * Dassault Systems CATIA (Windows, Linux)

### Atidarykite STP failus naudodami teksto redaktorius

STP failai išsaugomi kaip paprasto teksto failai. Tai leidžia atidaryti STP failus naudojant teksto redaktorius. Populiarūs teksto rengyklės, pvz., Notepad ir Notepad++ Windows OS ir Apple TextEdit MacOS gali atidaryti STP failus. Atidarius teksto rengyklėje, vartotojas gali redaguoti STP failo ypatybes. Tačiau netinkamai atnaujinus ypatybes, failas gali būti sugadintas.

## Kaip konvertuoti STP failus

Yra keletas programų, kurios gali konvertuoti STP failus į kitus failų formatus. CAD programos, kurios gali konvertuoti STP failus, apima:

 * Autodesk Fusion 360.
 * IMSI TurboCAD
 * Siemens Solid Edge

Be šių, yra keletas internetinių programų, kurios gali konvertuoti STP failus į kitus failų formatus. Šios internetinės programos leidžia įkelti STP failą į debesies serverius, kur jie konvertuojami į norimą formatą ir grąžinami atsisiųsti.

Autodesk Fusion 360 gali konvertuoti STP failus į šiuos 3D ir CAD failų formatus.

 * [OBJ](/3d/obj/)
 * [3MF](/3d/3mf/)
 * [DWG](/cad/dwg/)
 * [DXF](/cad/dxf/)
 * [ASM](/cad/asm/)
 * [IGES](/cad/iges/)
 * [STL](/cad/stl/)
 * [FBX](/3d/fbx/)
 * F3D
 * [USD](/3d/usd/)

## Nuorodos

 * [ISO 10303-21 – Vikipedija](https://en.wikipedia.org/wiki/ISO_10303-21)
 * [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

