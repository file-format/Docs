---
date: 2022-01-31
keywords: stp, .stp, stp file format, how to open stp files, .stp extension, stp extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP fil formularat
linktitle: STP
description: Ltjene om STP-filformat og API'er, der kan oprette og åbne STP-fils.
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Hvad er en STP fil?

En STP-fil er en 3D CAD-fil, der bruges til udveksling af produktdata mellem CAD- og CAM-applikationer. Den indeholder oplysninger om 3D-objekter og gemmes svarende til filformatet **STEP**. STP-filer letter udvekslingen af data mellem applikationer i henhold til [STEP](/3d/step/) Application Protocols ISO 10303-2xx. Denne ISO definerer kodningsmekanismen for datarepræsentation i EXPRESS datamodelleringssprog. STP-filer kan åbnes i programmer som f.eks. **Autodesk Fusion 360**.

## STP-filformat - flere oplysninger

STP-filer gemmes på disken i almindeligt ASCII-filformat. Disse indeholder oplysninger om 3D-modeller som almindelig tekst, der kan læses af CAD/CAM-applikationer til indlæsning af disse modeller.

STP-filer gemmes også med filtypenavnet .step og består af en række poster. Fremtrædende funktioner om disse filer omfatter:

 * Tegnsættet er defineret som kodepunkter i ISO 10646.
 * ISO-10303-21; er de første tegn i den første post.
 * Kommentarer er omgivet af /* og */ tegn.
 * Den sidste post indeholder END-ISO-10303-21; hvis STEP-filen er i overensstemmelse med 2002-versionen.
 * Hvis det er i overensstemmelse med 2016-versionen, kan der være en eller flere digitale signaturer efter END-ISO-10303-21; terminator.
 * Linjeskift er angivet med \N\ og sideskift er angivet med \F\.

## Åbn STP-filer

STP-filer kan åbnes i STP Viewers såvel som teksteditorer.

### Åbn STP-filer med STP Viewers

Forskellige CAD-applikationer kan åbne STP-filer til visning på Windows, MacOS og Linux. Disse omfatter:

 * Autodesk Fusion 360 (cross-platform)
 * FreeCAD (cross-platform)
 * IMSI TurboCAD (Windows, Mac)
 * Dassault Systems CATIA (Windows, Linux)

### Åbn STP-filer med teksteditorer

STP-filer gemmes som almindelige tekstfiler. Dette gør det muligt at åbne STP-filer med teksteditorer. Populære teksteditorer som Notepad og Notepad++ på Windows OS og Apple TextEdit på MacOS kan åbne STP-filer. Når den er åbnet i en teksteditor, kan brugeren redigere egenskaberne for STP-filen. Det kan dog føre til korruption af filen i tilfælde af opdatering af egenskaberne forkert.

## Sådan konverteres STP-filer

Der er flere programmer, der kan konvertere STP-filer til andre filformater. CAD-applikationer, der kan konvertere STP-filer inkluderer:

 * Autodesk Fusion 360
 * IMSI TurboCAD
 * Siemens Solid Edge

Ud over disse er der flere online apps, der kan konvertere STP-filer til andre filformater. Disse online apps giver dig mulighed for at uploade din STP-fil til cloud-servere, hvor de konverteres til dit ønskede format og returneres til download.

Autodesk Fusion 360 kan konvertere STP-filer til følgende 3D- og CAD-filformater.

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

## Referencer

 * [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
 * [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

