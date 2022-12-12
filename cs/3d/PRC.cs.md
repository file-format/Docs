---
date: 2019-10-11
keywords: prc, .prc, formát souboru prc, jak otevřít soubory prc, přípona .prc, přípona prc
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru PRC
linktitle: PRC
description: "Přečtěte si o formátu souboru PRC a rozhraních API, která mohou vytvářet a otevírat soubory PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Formáty souborů PRC
Přípony „.prc“ se používají pro formát souboru Product Representation Compact 3D a formát souboru e-knihy od společnosti MobiPocket.

## Co je soubor Product Representation Compact (PRC)?

PRC (Product Representation Compact) je 3D formát souboru, který je optimalizován pro ukládání, načítání a zobrazování 3D dat, zejména pocházejících ze systémů CAD (Computer-Aided Design). Jedná se o sekvenční binární soubor napsaný přenosným způsobem. PRC lze použít k vložení 3D dat do souboru PDF. PRC podporuje většinu hlavních konstrukcí CAD, jako jsou sestavy a díly, stromy 3D entit, přesné zobrazení geometrie, triangulované zobrazení a označení. PRC používá příponu .prc a použitý typ internetového média je *model/prc*.

PRC je víceúčelový formát souborů, který lze na základě jeho použití ukládat buď pomocí běžné komprese pro přímou reprezentaci CAD dat, nebo ukládat pomocí vysoké komprese pro zmenšení velikosti souboru. 3D data uložená ve formátu PDF ve formátu PRC jsou interoperabilní s aplikacemi CAM a CAE.

### Specifikace formátu souboru reprezentace produktu Compact (PRC).

Soubor PRC má jednu hlavní sekci záhlaví, za níž následuje jedna nebo více struktur souborů, za kterými na konci následuje jeden modelový soubor. Struktura souboru má jednu hlavičku, za kterou následují následující datové sekce:

- **Globals**: Obsahuje odkazované struktury souborů a barvy, styly čar a souřadnicové systémy pro každou entitu stromu struktury souboru.
- **Strom**: Obsahuje popis stromu položek, jako jsou výskyty produktů, definice součástí, položky reprezentace a označení.
- **Tessellation**: Obsahuje všechna mozaiková (triangulovaná) data v listových entitách stromu (reprezentační položky a značky).
- **Geometrie**: Obsahuje všechny přesné údaje o geometrii a topologii listových entit stromu (položky reprezentace).
- **Extra geometrie**: Obsahuje souhrnná data geometrie. To umožňuje částečné načtení souboru bez načtení celé geometrie.

Následuje struktura typického souboru PRC.

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
## Co je soubor elektronické knihy MobiPocket s příponou PRC
Formát souboru e-knihy, který zavedla francouzská společnost s názvem **Mobipocket**, také používá příponu „.prc“. Zpočátku Mobipocket spustil bezplatnou aplikaci pro více chytrých zařízení, jako jsou tablety, PDA a smartphony. Přípona ".prc" je ve skutečnosti totožná s příponou .mobi, ale používá se zejména pro PDA, která podporují pouze přípony **.prc** nebo **.pdb**.

### Specifikace formátu souboru Mobipocket PRC
Formát souboru MobiPocket PRC je založen na standardu Open eBook pomocí XHTML a také může obsahovat JavaScript a rámce. K dispozici je také podpora nativních SQL dotazů pro použití s vestavěnými databázemi.

Mobipocket Reader má knihovnu domovských stránek. Čtenáři mohou vkládat prázdné stránky do jakékoli části knihy a přidávat variabilní kresby. Objekty jako anotace, záložky, opravy, poznámky a kresby lze spravovat z jednoho místa. Obrázky jsou převedeny do formátu GIF a mají maximální velikost 64 kB, což je dostatečné pro mobilní telefony s malou obrazovkou. Mobipocket Reader má elektronické záložky a vestavěný slovník.

Čtečka má režim celé obrazovky pro čtení a podporu mnoha PDA, komunikátorů a chytrých telefonů. Produkty Mobipocket podporují většinu operačních systémů Palm, Windows, Symbian, BlackBerry, ale ne Android. Čtečka funguje pod Linuxem nebo Mac OS X pomocí WINE.

## Reference

– [PRC – Wikipedia](https://en.wikipedia.org/wiki/PRC_(formát_souboru))
- [Specifikace formátu PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
– [Porovnání formátů e-knih – Wikipedie](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

