---
date: 2022-01-31
keywords: stp, .stp, formát souboru stp, jak otevřít soubory stp, přípona .stp, přípona stp
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formát souboru STP
linktitle: STP
description: "Přečtěte si o formátu souboru STP a rozhraních API, která mohou vytvářet a otevírat soubory STP."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Co je soubor STP?

Soubor STP je 3D CAD soubor používaný pro výměnu produktových dat mezi CAD a CAM aplikacemi. Obsahuje informace o 3D objektech a ukládá se podobně jako soubor ve formátu **STEP**. Soubory STP usnadňují výměnu dat mezi aplikacemi podle [STEP](/cs/3d/step/) aplikačních protokolů ISO 10303-2xx. Tato ISO definuje kódovací mechanismus pro reprezentaci dat v jazyce EXPRESS pro modelování dat. Soubory STP lze otevřít v aplikacích, jako je **Autodesk Fusion 360**.

## Formát souboru STP – Další informace

Soubory STP se ukládají na disk ve formátu prostého souboru ASCII. Tyto obsahují informace o 3D modelech jako prostý text, který lze číst aplikacemi CAD/CAM pro načítání těchto modelů.

Soubory STP se také ukládají s příponou .step a sestávají ze sekvence záznamů. Mezi hlavní funkce těchto souborů patří:

* Sada znaků je definována jako kódové body normy ISO 10646.
* "ISO-10303-21;" jsou první znaky v prvním záznamu.
* Komentáře jsou obklopeny znaky "/*" a "*/".
* Poslední záznam obsahuje "END-ISO-10303-21;" pokud je soubor STEP v souladu s verzí z roku 2002.
* V případě, že odpovídá verzi z roku 2016, může být za „END-ISO-10303-21;“ jeden nebo více digitálních podpisů; terminátor.
* Konce řádků jsou označeny "\N\" a konce stránek jsou označeny "\F\".

## Otevřete soubory STP

Soubory STP lze otevřít v prohlížečích STP i v textových editorech.

### Otevřít soubory STP pomocí prohlížečů STP

Různé CAD aplikace mohou otevřít soubory STP pro prohlížení v systémech Windows, MacOS a Linux. Tyto zahrnují:

* Autodesk Fusion 360 (multiplatformní)
* FreeCAD (multiplatformní)
* IMSI TurboCAD (Windows, Mac)
* Dassault Systems CATIA (Windows, Linux)

### Otevřít soubory STP pomocí textových editorů

Soubory STP se ukládají jako soubory ve formátu prostého textu. To umožňuje otevírat soubory STP pomocí textových editorů. Oblíbené textové editory, jako je Notepad a Notepad++ v operačním systému Windows a Apple TextEdit v systému MacOS, mohou otevírat soubory STP. Po otevření v textovém editoru může uživatel upravit vlastnosti souboru STP. V případě nesprávné aktualizace vlastností však může dojít k poškození souboru.

## Jak převést soubory STP

Existuje několik aplikací, které mohou převádět soubory STP do jiných formátů souborů. Mezi aplikace CAD, které mohou převádět soubory STP, patří:

* Autodesk Fusion 360
* IMSI TurboCAD
* Siemens Solid Edge

Kromě toho existuje několik online aplikací, které mohou převádět soubory STP do jiných formátů souborů. Tyto online aplikace vám umožňují nahrát soubor STP na cloudové servery, kde jsou převedeny do požadovaného formátu a vráceny zpět ke stažení.

Autodesk Fusion 360 dokáže převádět soubory STP do následujících 3D a CAD formátů souborů.

* [OBJ](/cs/3d/obj/)
* [3MF](/cs/3d/3mf/)
* [DWG](/cs/cad/dwg/)
* [DXF](/cs/cad/dxf/)
* [ASM](/cs/cad/asm/)
* [IGES](/cs/cad/iges/)
* [STL](/cs/cad/stl/)
* [FBX] (/cs/3d/fbx/)
* F3D
* [USD](/cs/3d/usd/)

## Reference

* [ISO 10303-21 – Wikipedie](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

