---
date: 2022-01-31
keywords: stp, .stp, stp-filformat, hur man öppnar stp-filer, .stp-tillägg, stp-tillägg
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP-filformat
linktitle: STP
description: "Lär dig om STP-filformat och API:er som kan skapa och öppna STP-filer."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Vad är en STP fil?

En STP-fil är en 3D CAD-fil som används för utbyte av produktdata mellan CAD- och CAM-applikationer. Den innehåller information om 3D-objekt och sparas på samma sätt som filformatet **STEP**. STP-filer underlättar utbyte av data mellan applikationer enligt [STEP](/sv/3d/step/) Application Protocols ISO 10303-2xx. Denna ISO definierar kodningsmekanismen för datarepresentation i EXPRESS datamodelleringsspråk. STP-filer kan öppnas i applikationer som till exempel **Autodesk Fusion 360**.

## STP-filformat - Mer information

STP-filer sparas på skiva i vanligt ASCII-filformat. Dessa innehåller information om 3D-modeller som vanlig text som kan läsas av CAD/CAM-applikationer för att ladda dessa modeller.

STP-filer sparas också med tillägget .step och består av en sekvens av poster. Framträdande funktioner för dessa filer inkluderar:

* Teckenuppsättningen definieras som kodpunkter enligt ISO 10646.
* "ISO-10303-21;" är de första tecknen i den första posten.
* Kommentarer är omgivna av "/*" och "*/" tecken.
* Den sista posten innehåller "END-ISO-10303-21;" om STEP-filen överensstämmer med 2002 års version.
* Om den överensstämmer med 2016 års version kan det finnas en eller flera digitala signaturer efter "END-ISO-10303-21;" terminator.
* Radbrytningar betecknas med "\N\" och sidbrytningar betecknas med "\F\".

## Öppna STP-filer

STP-filer kan öppnas i STP Viewers såväl som i textredigerare.

### Öppna STP-filer med STP Viewers

Olika CAD-applikationer kan öppna STP-filer för visning på Windows, MacOS och Linux. Dessa inkluderar:

* Autodesk Fusion 360 (plattformsoberoende)
* FreeCAD (plattformsoberoende)
* IMSI TurboCAD (Windows, Mac)
* Dassault Systems CATIA (Windows, Linux)

### Öppna STP-filer med textredigerare

STP-filer sparas som vanliga textfiler. Detta gör det möjligt att öppna STP-filer med textredigerare. Populära textredigerare som Notepad och Notepad++ på Windows OS och Apple TextEdit på MacOS kan öppna STP-filer. När den öppnats i en textredigerare kan användaren redigera egenskaperna för STP-filen. Det kan dock leda till korruption av filen i händelse av att egenskaperna uppdateras felaktigt.

## Hur man konverterar STP-filer

Det finns flera applikationer som kan konvertera STP-filer till andra filformat. CAD-applikationer som kan konvertera STP-filer inkluderar:

* Autodesk Fusion 360
* IMSI TurboCAD
* Siemens Solid Edge

Utöver dessa finns det flera onlineappar som kan konvertera STP-filer till andra filformat. Dessa onlineappar låter dig ladda upp din STP-fil till molnservrar där de konverteras till önskat format och returneras för nedladdning.

Autodesk Fusion 360 kan konvertera STP-filer till följande 3D- och CAD-filformat.

* [OBJ](/sv/3d/obj/)
* [3MF](/sv/3d/3mf/)
* [DWG](/sv/cad/dwg/)
* [DXF](/sv/cad/dxf/)
* [ASM](/sv/cad/asm/)
* [IGES](/sv/cad/iges/)
* [STL](/sv/cad/stl/)
* [FBX](/sv/3d/fbx/)
* F3D
* [USD](/sv/3d/usd/)

## Referenser

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

