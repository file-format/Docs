---
date: 2019-10-11
keywords: prc, .prc, prc file format, how to open prc files, .prc extension, prc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC failo formaat
linktitle: PRC
description: Luždirbti apie PRC failo formatą ir API, kurios gali sukurti ir atidaryti PRC failąs.
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## KLR failų formatai
Plėtiniai .prc naudojami MobiPocket produkto atstovavimo kompaktiškam 3D formatui ir el. knygos failo formatui.

## Kas yra Product Representation Compact (PRC) failas?

PRC (Product Representation Compact) yra 3D failo formatas, optimizuotas saugoti, įkelti ir rodyti 3D duomenis, ypač gaunamus iš CAD (kompiuterinio projektavimo) sistemų. Tai nuoseklus dvejetainis failas, parašytas nešiojamu būdu. KLR gali būti naudojamas 3D duomenims įterpti į PDF failą. KLR palaiko daugumą pagrindinių CAD konstrukcijų, tokių kaip mazgai ir dalys, 3D objektų medžiai, tikslus geometrijos atvaizdavimas, trikampis vaizdas ir žymėjimas. KLR naudoja plėtinį .prc, o naudojamas interneto medijos tipas yra *modelis/prc*.

PRC yra daugiafunkcis failo formatas, kuris, atsižvelgiant į jo naudojimą, gali būti saugomas naudojant įprastą glaudinimą, kad būtų tiesiogiai atvaizduojami CAD duomenys, arba saugomas naudojant didelį glaudinimą, kad būtų sumažintas failo dydis. 3D duomenys, saugomi PDF formatu naudojant PRC formatą, yra suderinami su CAM ir CAE programomis.

### Kompaktiško produkto atstovavimo (PRC) failo formato specifikacija

KLR faile yra viena pagrindinė antraštės dalis, po kurios yra viena ar daugiau failų struktūrų, o pabaigoje – vienas modelio failas. Failo struktūroje yra viena antraštė, po kurios yra šie duomenų skyriai:

- **Globalai**: jame yra nurodytos failų struktūros ir spalvos, linijų stiliai ir koordinačių sistemos kiekvienam failo struktūros medžio objektui.
- **Tree**: It contains a description of the tree of items like product occurrences, part definitions, representation items, and markup.
- **Tesselation**: jame yra visi teseliuoti (trikampiai) duomenys medžio lapų objektuose (reprezentaciniai elementai ir žymėjimai).
- **Geometrija**: jame yra visi tikslūs medžio lapų objektų geometrijos ir topologijos duomenys (reprezentaciniai elementai).
- **Papildoma geometrija**: joje yra suvestinės geometrijos duomenys. Tai leidžia iš dalies įkelti failą neįkeliant visos geometrijos.

Toliau pateikiama tipinio KLR failo struktūra.

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
## Kas yra MobiPocket e-knygos failas su PRC plėtiniu
El. knygos failo formatas, kurį pristatė prancūzų kompanija **Mobipocket**, taip pat naudoja plėtinį .prc. Iš pradžių Mobipocket pristatė nemokamą programą keliems išmaniesiems įrenginiams, pvz., planšetiniams kompiuteriams, delniniams kompiuteriams ir išmaniesiems telefonams. Plėtinys .prc iš tikrųjų yra identiškas .mobi, bet ypač naudojamas PDA, kurie palaiko tik **.prc** arba **.pdb** plėtinius.

### Mobipocket PRC failo formato specifikacijos
MobiPocket PRC failo formatas yra pagrįstas Open eBook standartu, naudojant XHTML, taip pat gali apimti JavaScript ir rėmelius. Taip pat galimas vietinių SQL užklausų, naudojamų su įterptomis duomenų bazėmis, palaikymas.

Mobipocket Reader turi pagrindinio puslapio biblioteką. Skaitytojai gali įterpti tuščius puslapius į bet kurią knygos dalį ir pridėti kintamų brėžinių. Tokie objektai kaip komentarai, žymės, pataisymai, pastabos ir brėžiniai yra valdomi vienoje vietoje. Vaizdai konvertuojami į GIF formatą ir jų maksimalus dydis yra 64K, to pakanka mobiliesiems telefonams su mažais ekranais. Mobipocket Reader turi elektronines žymes ir integruotą žodyną.

Skaitytuvas turi viso ekrano režimą, leidžiantį skaityti ir palaikyti daugelį PDA, komunikatorių ir išmaniųjų telefonų. Mobipocket produktai palaiko daugumą Palm operacinių sistemų, Windows, Symbian, BlackBerry, bet ne Android. Skaitytuvas veikia Linux arba Mac OS X sistemoje, naudodamas WINE.

## Nuorodos

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparison of e-book formats - By Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

