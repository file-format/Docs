---
date: 2022-01-31
keywords: stp, .stp, stp-bestandsindeling, hoe stp-bestanden te openen, .stp-extensie, stp-extensie
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP-bestandsindeling
linktitle: STP
description: "Meer informatie over STP-bestandsindelingen en API's die STP-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Wat is een STP-bestand?

Een STP-bestand is een 3D CAD-bestand dat wordt gebruikt voor de uitwisseling van productgegevens tussen CAD- en CAM-toepassingen. Het bevat informatie over 3D-objecten en wordt opgeslagen op dezelfde manier als het **STEP**-bestandsformaat. STP-bestanden vergemakkelijken de uitwisseling van gegevens tussen applicaties volgens de [STEP](/nl/3d/step/) Application Protocols ISO 10303-2xx. Deze ISO definieert het coderingsmechanisme voor datarepresentatie in EXPRESS datamodelleringstaal. STP-bestanden kunnen worden geopend in toepassingen zoals **Autodesk Fusion 360**.

## STP-bestandsindeling - Meer informatie

STP-bestanden worden op schijf opgeslagen in gewoon ASCII-bestandsformaat. Deze bevatten informatie over 3D-modellen als platte tekst die kan worden gelezen door CAD/CAM-toepassingen om deze modellen te laden.

STP-bestanden worden ook opgeslagen met de extensie .step en bestaan uit een reeks records. Opvallende kenmerken van deze bestanden zijn onder meer:

* De tekenset is gedefinieerd als codepunten van ISO 10646.
* "ISO-10303-21;" zijn de eerste tekens in de eerste record.
* Opmerkingen zijn omgeven door "/*" en "*/" tekens.
* Het laatste record bevat "END-ISO-10303-21;" als het STEP-bestand overeenkomt met de 2002-versie.
* Als het overeenkomt met de 2016-versie, kunnen er een of meer digitale handtekeningen staan na de "END-ISO-10303-21;" terminator.
* Regeleinden worden aangegeven met "\N\" en pagina-einden worden aangegeven met "\F\".

## STP-bestanden openen

STP-bestanden kunnen zowel in STP-viewers als in teksteditors worden geopend.

### Open STP-bestanden met STP-viewers

Verschillende CAD-applicaties kunnen STP-bestanden openen voor weergave op Windows, MacOS en Linux. Waaronder:

* Autodesk Fusion 360 (platformoverschrijdend)
* FreeCAD (platformoverschrijdend)
* IMSI TurboCAD (Windows, Mac)
* Dassault-systemen CATIA (WIndows, Linux)

### Open STP-bestanden met teksteditors

STP-bestanden worden opgeslagen als platte tekstbestanden. Dit maakt het mogelijk om STP-bestanden te openen met teksteditors. Populaire teksteditors zoals Notepad en Notepad++ op Windows OS, en Apple TextEdit op MacOS kunnen STP-bestanden openen. Eenmaal geopend in een teksteditor, kan de gebruiker de eigenschappen van het STP-bestand bewerken. Het kan echter leiden tot corruptie van het bestand als de eigenschappen onjuist worden bijgewerkt.

## Hoe STP-bestanden te converteren

Er zijn verschillende toepassingen die STP-bestanden naar andere bestandsindelingen kunnen converteren. CAD-toepassingen die STP-bestanden kunnen converteren, zijn onder meer:

* Autodesk Fusion 360
* IMSI TurboCAD
* Siemens Solid Edge

Daarnaast zijn er verschillende online apps die STP-bestanden naar andere bestandsindelingen kunnen converteren. Met deze online apps kun je je STP-bestand uploaden naar cloudservers waar ze worden geconverteerd naar het gewenste formaat en teruggestuurd om te downloaden.

De Autodesk Fusion 360 kan STP-bestanden converteren naar de volgende 3D- en CAD-bestandsindelingen.

* [OBJ](/nl/3d/obj/)
* [3MF](/nl/3d/3mf/)
* [DWG](/nl/cad/dwg/)
* [DXF](/nl/cad/dxf/)
* [ASM](/nl/cad/asm/)
* [IGES](/nl/cad/iges/)
* [STL](/nl/cad/stl/)
* [FBX](/nl/3d/fbx/)
* F3D
* [USD](/nl/3d/usd/)

## Referenties

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

