---
date: 2019-10-11
keywords: prc, .prc, format de fișier prc, cum se deschide fișiere prc, extensia .prc, extensia prc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier PRC
linktitle: PRC
description: "Aflați despre formatul de fișier PRC și despre API-urile care pot crea și deschide fișiere PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Formatele de fișiere PRC
Extensiile „.prc” sunt folosite pentru formatul de fișier Product Representation Compact 3D și un format de fișier e-book de către MobiPocket.

## Ce este un fișier Product Representation Compact (PRC)?

PRC (Product Representation Compact) este un format de fișier 3D care este optimizat pentru a stoca, încărca și afișa date 3D care provin în special din sistemele CAD (Computer-Aided Design). Este un fișier binar secvenţial, scris într-un mod portabil. PRC poate fi folosit pentru a încorpora date 3D într-un fișier PDF. PRC acceptă majoritatea construcțiilor principale ale CAD, cum ar fi ansambluri și piese, arbori de entități 3D, reprezentare exactă a geometriei, reprezentare triangulată și marcare. PRC folosește extensia .prc, iar tipul media de internet utilizat este *model/prc*.

PRC este un format de fișier multifuncțional care, pe baza utilizării sale, poate fi fie stocat utilizând compresia obișnuită pentru a reprezenta direct datele CAD, fie stocat folosind compresie ridicată pentru a reduce dimensiunea fișierului. Datele 3D stocate într-un PDF utilizând formatul PRC sunt interoperabile cu aplicațiile CAM și CAE.

### Specificația formatului de fișiere pentru reprezentarea produsului compact (PRC).

Un fișier PRC are o secțiune de antet principală urmată de una sau mai multe structuri de fișiere urmate de un fișier model la sfârșit. O structură de fișiere are un antet urmat de următoarele secțiuni de date:

- **Globals**: conține structurile și culorile fișierelor la care se face referire, stilurile de linii și sistemele de coordonate pentru fiecare entitate arborescentă a structurii fișierului.
- **Arborele**: conține o descriere a arborelui de articole, cum ar fi aparițiile produselor, definițiile pieselor, elementele de reprezentare și marcajul.
- **Teselație**: conține toate datele teselate (triangulate) din entitățile frunze ale arborelui (articole de reprezentare și markupuri).
- **Geometrie**: conține toate datele exacte de geometrie și topologie ale entităților frunze ale arborelui (articole de reprezentare).
- **Geometrie suplimentară**: Conține datele rezumative ale geometriei. Acest lucru permite ca fișierul să fie încărcat parțial fără a încărca întreaga geometrie.

Următoarea este structura unui fișier PRC tipic.

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
## Ce este un fișier de carte electronică MobiPocket cu extensia PRC
Un format de fișier e-book care este introdus de o companie franceză numită **Mobipocket** folosește și extensia „.prc”. Inițial, Mobipocket a lansat o aplicație gratuită pentru mai multe dispozitive inteligente, cum ar fi tablete, PDA-uri și smartphone-uri. Extensia „.prc” este de fapt identică cu .mobi, dar este folosită în special pentru PDA-uri care acceptă doar extensiile **.prc** sau **.pdb**.

### Specificații de format de fișier Mobipocket PRC
Formatul de fișier MobiPocket PRC se bazează pe standardul Open eBook folosind XHTML și, de asemenea, poate include JavaScript și cadre. Este disponibil și suport pentru interogările SQL native care urmează să fie utilizate cu baze de date încorporate.

Mobipocket Reader are o bibliotecă de pagină de pornire. Cititorii pot introduce pagini goale în orice parte a unei cărți și pot adăuga desene variabile. Obiectele precum adnotări, marcaje, corecții, note și desene pot fi gestionate dintr-o singură locație. Imaginile sunt convertite în format GIF și au o dimensiune maximă de 64K, ceea ce este suficient pentru telefoanele mobile cu ecrane mici. Mobipocket Reader are marcaje electronice și un dicționar încorporat.

Cititorul are un mod ecran complet pentru citire și suport pentru multe PDA-uri, comunicatoare și telefoane inteligente. Produsele Mobipocket acceptă majoritatea sistemelor de operare Palm, Windows, Symbian, BlackBerry, dar nu și Android. Cititorul funcționează sub Linux sau Mac OS X folosind WINE.

## Referințe

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [Specificație format PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparație a formatelor de cărți electronice - De Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

