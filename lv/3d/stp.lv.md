---
date: 2022-01-31
keywords: stp, .stp, stp file format, how to open stp files, .stp extension, stp extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP faila veidlapaat
linktitle: STP
description: Lnopelniet par STP faila formātu un API, kas var izveidot un atvērt STP failus.
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Kas ir STP fails?

STP fails ir 3D CAD fails, ko izmanto produkta datu apmaiņai starp CAD un CAM lietojumprogrammām. Tas satur informāciju par 3D objektiem un tiek saglabāts līdzīgi kā **STEP** faila formātā. STP faili atvieglo datu apmaiņu starp lietojumprogrammām saskaņā ar [STEP](/3d/step/) lietojumprogrammu protokoliem ISO 10303-2xx. Šis ISO nosaka kodēšanas mehānismu datu attēlošanai EXPRESS datu modelēšanas valodā. STP failus var atvērt tādās lietojumprogrammās kā **Autodesk Fusion 360**.

## STP faila formāts — vairāk informācijas

STP faili tiek saglabāti diskā vienkāršā ASCII faila formātā. Tie satur 3D modeļu informāciju kā vienkāršu tekstu, ko var nolasīt CAD/CAM lietojumprogrammas, lai ielādētu šos modeļus.

STP faili tiek saglabāti arī ar paplašinājumu .step, un tie sastāv no ierakstu secības. Šo failu svarīgākās funkcijas ietver:

 * Rakstzīmju kopa ir definēta kā ISO 10646 koda punkti.
 * ISO-10303-21; ir pirmās rakstzīmes pirmajā ierakstā.
 * Komentārus ieskauj rakstzīmes /* un */.
 * Pēdējais ieraksts satur END-ISO-10303-21; ja STEP fails atbilst 2002. gada versijai.
 * Ja tas atbilst 2016. gada versijai, aiz END-ISO-10303-21; var būt viens vai vairāki ciparparaksti. terminators.
 * Rindas pārtraukumi ir apzīmēti ar \N\ un lappušu pārtraukumi ir apzīmēti ar \F\.

## Atveriet STP failus

STP failus var atvērt STP skatītājos, kā arī teksta redaktoros.

### Atveriet STP failus ar STP skatītājiem

Dažādas CAD lietojumprogrammas var atvērt STP failus, lai tos skatītu operētājsistēmās Windows, MacOS un Linux. Tie ietver:

 * Autodesk Fusion 360 (vairāku platformu)
 * FreeCAD (vairāku platformu)
 * IMSI TurboCAD (Windows, Mac)
 * Dassault Systems CATIA (Windows, Linux)

### Atveriet STP failus ar teksta redaktoriem

STP faili tiek saglabāti kā vienkārša teksta faili. Tas ļauj atvērt STP failus ar teksta redaktoriem. Populāri teksta redaktori, piemēram, Notepad un Notepad++ operētājsistēmā Windows, un Apple TextEdit operētājsistēmā MacOS var atvērt STP failus. Pēc atvēršanas teksta redaktorā lietotājs var rediģēt STP faila rekvizītus. Tomēr nepareizas rekvizītu atjaunināšanas gadījumā tas var izraisīt faila bojājumus.

## Kā konvertēt STP failus

Ir vairākas lietojumprogrammas, kas var konvertēt STP failus citos failu formātos. CAD lietojumprogrammas, kas var konvertēt STP failus, ietver:

 * Autodesk Fusion 360
 * IMSI TurboCAD
 * Siemens Solid Edge

Papildus tām ir vairākas tiešsaistes lietotnes, kas var konvertēt STP failus citos failu formātos. Šīs tiešsaistes lietotnes ļauj augšupielādēt STP failu mākoņserveros, kur tie tiek pārveidoti vēlamajā formātā un atgriezti lejupielādei.

Autodesk Fusion 360 var konvertēt STP failus šādos 3D un CAD failu formātos.

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

## Atsauces

 * [ISO 10303-21 — Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
 * [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

