---
date: 2022-01-31
keywords: stp, .stp, stp fájlformátum, stp fájlok megnyitása, .stp kiterjesztések, stp kiterjesztések
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP fájlformátum
linktitle: STP
description: "Ismerje meg az STP fájlformátumot és az API-kat, amelyek STP-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Mi az STP fájl?

Az STP-fájl egy 3D-s CAD-fájl, amelyet a termékadatok CAD- és CAM-alkalmazások közötti cseréjére használnak. Információkat tartalmaz a 3D objektumokról, és a **STEP** fájlformátumhoz hasonlóan kerül mentésre. Az STP-fájlok megkönnyítik az alkalmazások közötti adatcserét az ISO 10303-2xx [STEP](/hu/3d/step/) Application Protocols szerint. Ez az ISO meghatározza az adatok EXPRESS adatmodellező nyelven történő megjelenítésének kódolási mechanizmusát. Az STP-fájlok megnyithatók olyan alkalmazásokban, mint például az **Autodesk Fusion 360**.

## STP fájlformátum - További információ

Az STP-fájlokat a rendszer egyszerű ASCII-fájlformátumban menti a lemezre. Ezek egyszerű szövegként tartalmazzák a 3D modellekre vonatkozó információkat, amelyeket a CAD/CAM alkalmazások elolvashatnak a modellek betöltéséhez.

Az STP-fájlok szintén .step kiterjesztéssel kerülnek mentésre, és rekordok sorozatából állnak. Ezeknek a fájloknak a legfontosabb jellemzői a következők:

* A karakterkészlet az ISO 10646 kódpontjaiként van definiálva.
* "ISO-10303-21;" ezek az első karakterek az első rekordban.
* A megjegyzéseket „/*” és „*/” karakter veszi körül.
* Az utolsó rekord a következőt tartalmazza: "END-ISO-10303-21;" ha a STEP-fájl megfelel a 2002-es verziónak.
* Abban az esetben, ha megfelel a 2016-os verziónak, egy vagy több digitális aláírás szerepelhet az "END-ISO-10303-21;" után. Végrehajtó.
* A sortöréseket "\N\", az oldaltöréseket pedig "\F\" jelöli.

## Nyissa meg az STP-fájlokat

Az STP fájlok az STP Viewerben és a szövegszerkesztőben is megnyithatók.

### Nyissa meg az STP-fájlokat az STP-nézőkkel

Különféle CAD-alkalmazások nyithatnak meg STP-fájlokat Windows, MacOS és Linux rendszereken való megtekintéshez. Ezek tartalmazzák:

* Autodesk Fusion 360 (platformok közötti)
* FreeCAD (platformok közötti)
* IMSI TurboCAD (Windows, Mac)
* Dassault Systems CATIA (Windows, Linux)

### Nyissa meg az STP-fájlokat szövegszerkesztőkkel

Az STP-fájlok egyszerű szöveges fájlokként kerülnek mentésre. Ez lehetővé teszi az STP-fájlok megnyitását szövegszerkesztőkkel. Az olyan népszerű szövegszerkesztők, mint a Notepad és a Notepad++ Windows operációs rendszeren, illetve az Apple TextEdit MacOS rendszeren, képesek megnyitni az STP-fájlokat. Szövegszerkesztőben megnyitva a felhasználó szerkesztheti az STP fájl tulajdonságait. A tulajdonságok helytelen frissítése esetén azonban ez a fájl sérüléséhez vezethet.

## STP fájlok konvertálása

Számos alkalmazás képes az STP-fájlokat más fájlformátumokká konvertálni. Az STP-fájlok konvertálására alkalmas CAD-alkalmazások a következők:

* Autodesk Fusion 360
* IMSI TurboCAD
* Siemens Solid Edge

Ezeken kívül számos online alkalmazás létezik, amelyek az STP-fájlokat más fájlformátumokká konvertálhatják. Ezek az online alkalmazások lehetővé teszik az STP-fájl feltöltését felhőszerverekre, ahol azokat a kívánt formátumra konvertálják, és visszaküldik letöltésre.

Az Autodesk Fusion 360 az STP fájlokat a következő 3D és CAD fájlformátumokba tudja konvertálni.

* [OBJ](/hu/3d/obj/)
* [3MF](/hu/3d/3mf/)
* [DWG](/hu/cad/dwg/)
* [DXF](/hu/cad/dxf/)
* [ASM](/hu/cad/asm/)
* [IGES](/hu/cad/iges/)
* [STL](/hu/cad/stl/)
* [FBX](/hu/3d/fbx/)
* F3D
* [USD](/hu/3d/usd/)

## Hivatkozások

* [ISO 10303-21 – Wikipédia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

