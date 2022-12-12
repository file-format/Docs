---
date: 2019-10-11
keywords: prc, .prc, prc fájlformátum, prc fájlok megnyitása, .prc kiterjesztése, prc kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC fájlformátum
linktitle: PRC
description: "Ismerje meg a PRC fájlformátumot és az API-kat, amelyek PRC fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## A KNK fájlformátumai
A ".prc" kiterjesztést a MobiPocket a Product Representation Compact 3D fájlformátumhoz és egy e-könyv fájlformátumhoz használja.

## Mi az a Product Representation Compact (PRC) fájl?

A PRC (Product Representation Compact) egy 3D-s fájlformátum, amelyet elsősorban a CAD (Computer-Aided Design) rendszerekből származó 3D adatok tárolására, betöltésére és megjelenítésére optimalizáltak. Ez egy szekvenciális bináris fájl, amelyet hordozható módon írnak. A PRC használható 3D adatok PDF-fájlba ágyazására. A PRC támogatja a CAD legtöbb fő konstrukcióját, mint például az összeállításokat és alkatrészeket, a 3D entitások fáit, a pontos geometriai ábrázolást, a háromszögletes ábrázolást és a jelölést. A PRC a .prc kiterjesztést használja, az internetes médiatípus pedig a *model/prc*.

A PRC egy többcélú fájlformátum, amely használatától függően vagy normál tömörítéssel tárolható a CAD-adatok közvetlen megjelenítéséhez, vagy nagy tömörítéssel tárolható a fájlméret csökkentése érdekében. A PRC formátumot használó PDF-ben tárolt 3D adatok együttműködnek a CAM és CAE alkalmazásokkal.

### Product Representation Compact (PRC) fájlformátum specifikáció

A PRC-fájlnak egy fő fejlécrésze van, amelyet egy vagy több fájlstruktúra követ, majd egy modellfájl a végén. A fájlszerkezetnek egy fejléce van, amelyet a következő adatrészek követnek:

- **Globálisok**: A hivatkozott fájlstruktúrákat és színeket, vonalstílusokat és koordinátarendszereket tartalmazza a fájlstruktúra minden egyes fa-entitásánál.
- **Fa**: Az elemek fájának leírását tartalmazza, mint például a termék előfordulásai, az alkatrészdefiníciók, a reprezentációs cikkek és a jelölések.
- **Tessellation**: A fa levélentitásaiban található összes tesszellált (háromszögletű) adatot tartalmazza (ábrázolási elemek és jelölések).
- **Geometria**: Tartalmazza a fa levélelemeinek (ábrázolási elemek) összes pontos geometriai és topológiai adatát.
- **Extra geometria**: A geometria összefoglaló adatait tartalmazza. Ez lehetővé teszi a fájl részleges betöltését a teljes geometria betöltése nélkül.

A következő egy tipikus PRC-fájl szerkezete látható.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Mi az a MobiPocket e-könyv fájl PRC kiterjesztéssel?
A **Mobipocket** nevű francia cég által bevezetett e-könyv fájlformátum szintén a „.prc” kiterjesztést használja. Kezdetben a Mobipocket ingyenes alkalmazást indított több intelligens eszközhöz, például táblagépekhez, PDA-khoz és okostelefonokhoz. A ".prc" kiterjesztés valójában megegyezik a .mobi kiterjesztéssel, de különösen olyan PDA-k esetében használják, amelyek csak a **.prc** vagy **.pdb** kiterjesztést támogatják.

### A Mobipocket PRC fájlformátum specifikációi
A MobiPocket PRC fájlformátum az Open eBook szabványon alapul, XHTML használatával, és JavaScriptet és kereteket is tartalmazhat. A beágyazott adatbázisokkal használható natív SQL-lekérdezések támogatása is elérhető.

A Mobipocket Readernek van egy kezdőlapkönyvtára. Az olvasók beszúrhatnak üres oldalakat a könyv bármely részébe, és változó rajzokat adhatnak hozzá. Az olyan objektumok, mint a megjegyzések, könyvjelzők, javítások, megjegyzések és rajzok, egyetlen helyről kezelhetők. A képeket GIF formátumba konvertálja a rendszer, és a maximális méretük 64K, ami elegendő kis képernyős mobiltelefonokhoz. A Mobipocket Reader rendelkezik elektronikus könyvjelzőkkel és beépített szótárral.

Az olvasó teljes képernyős móddal rendelkezik az olvasáshoz és számos PDA-hoz, kommunikátorhoz és okostelefonhoz való támogatáshoz. A Mobipocket termékek támogatják a legtöbb Palm operációs rendszert (Windows, Symbian, BlackBerry), az Androidot azonban nem. Az olvasó Linux vagy Mac OS X alatt WINE segítségével működik.

## Hivatkozások

- [KNK - Wikipédia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC formátumspecifikáció](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Az e-könyvformátumok összehasonlítása – a Wikipédia által](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

