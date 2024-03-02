---
date: 2022-01-31
keywords: stp, .stp, stp file format, how to open stp files, .stp extension, stp extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP-tiedostolomakeat
linktitle: STP
description: Ltienaa STP-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata STP-tiedostons.
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Mikä on STP-tiedosto?

STP-tiedosto on 3D-CAD-tiedosto, jota käytetään tuotetietojen vaihtamiseen CAD- ja CAM-sovellusten välillä. Se sisältää tietoja 3D-objekteista ja tallennetaan samalla tavalla kuin **STEP**-tiedostomuoto. STP-tiedostot helpottavat tietojen vaihtoa sovellusten välillä [STEP](/3d/step/) Application Protocols ISO 10303-2xx -standardin mukaisesti. Tämä ISO määrittelee koodausmekanismin tietojen esittämiselle EXPRESS-datamallinnuskielellä. STP-tiedostoja voidaan avata sovelluksissa, kuten **Autodesk Fusion 360**.

## STP-tiedostomuoto - lisätietoja

STP-tiedostot tallennetaan levylle tavallisessa ASCII-tiedostomuodossa. Nämä sisältävät 3D-mallien tietoja pelkkänä tekstinä, jonka CAD/CAM-sovellukset voivat lukea näiden mallien lataamista varten.

STP-tiedostot tallennetaan myös .step-tunnisteella, ja ne koostuvat tietueiden sarjasta. Näiden tiedostojen tärkeimpiä ominaisuuksia ovat:

 * Merkistö on määritelty ISO 10646:n koodipisteinä.
 * ISO-10303-21; ovat ensimmäisen tietueen ensimmäiset merkit.
 * Kommentit on ympäröity /*- ja */-merkeillä.
 * Viimeinen tietue sisältää END-ISO-10303-21; jos STEP-tiedosto on vuoden 2002 version mukainen.
 * Jos se on vuoden 2016 version mukainen, END-ISO-10303-21;:n jälkeen voi olla yksi tai useampi digitaalinen allekirjoitus. terminaattori.
 * Rivinvaihdot on merkitty \N\ ja sivunvaihdot on merkitty \F\.

## Avaa STP-tiedostot

STP-tiedostoja voidaan avata STP-katseluohjelmissa sekä tekstieditoreissa.

### Avaa STP-tiedostot STP-katseluohjelmilla

Useat CAD-sovellukset voivat avata STP-tiedostoja katseltavaksi Windowsissa, MacOS:ssa ja Linuxissa. Nämä sisältävät:

 * Autodesk Fusion 360 (monialustaiset)
 * FreeCAD (alustojen välinen)
 * IMSI TurboCAD (Windows, Mac)
 * Dassault Systems CATIA (Windows, Linux)

### Avaa STP-tiedostot tekstieditorilla

STP-tiedostot tallennetaan tekstitiedostoina. Tämä mahdollistaa STP-tiedostojen avaamisen tekstieditoreilla. Suositut tekstieditorit, kuten Notepad ja Notepad++ Windows-käyttöjärjestelmässä ja Apple TextEdit MacOS-käyttöjärjestelmässä, voivat avata STP-tiedostoja. Kun se on avattu tekstieditorissa, käyttäjä voi muokata STP-tiedoston ominaisuuksia. Se voi kuitenkin johtaa tiedoston vioittumiseen, jos ominaisuuksia päivitetään väärin.

## Kuinka muuntaa STP-tiedostoja

On olemassa useita sovelluksia, jotka voivat muuntaa STP-tiedostoja muihin tiedostomuotoihin. CAD-sovelluksia, jotka voivat muuntaa STP-tiedostoja, ovat:

 * Autodesk Fusion 360
 * IMSI TurboCAD
 * Siemens Solid Edge

Näiden lisäksi on olemassa useita online-sovelluksia, jotka voivat muuntaa STP-tiedostoja muihin tiedostomuotoihin. Näiden verkkosovellusten avulla voit ladata STP-tiedostosi pilvipalvelimille, joissa ne muunnetaan haluamaasi muotoon ja palautetaan takaisin ladattavaksi.

Autodesk Fusion 360 voi muuntaa STP-tiedostoja seuraaviin 3D- ja CAD-tiedostomuotoihin.

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

## Viitteet

 * [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
 * [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

