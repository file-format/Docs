---
date: 2022-01-31
keywords: stp, .stp, format de fișier stp, cum se deschide fișierele stp, extensia .stp, extensia stp
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format de fișier STP
linktitle: STP
description: "Aflați despre formatul de fișier STP și despre API-urile care pot crea și deschide fișiere STP."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Ce este un fișier STP?

Un fișier STP este un fișier CAD 3D utilizat pentru schimbul de date despre produse între aplicațiile CAD și CAM. Conține informații despre obiectele 3D și este salvat similar cu formatul de fișier **STEP**. Fișierele STP facilitează schimbul de date între aplicații conform [STEP](/ro/3d/step/) Protocoale de aplicație ISO 10303-2xx. Acest ISO definește mecanismul de codificare pentru reprezentarea datelor în limbajul de modelare a datelor EXPRESS. Fișierele STP pot fi deschise în aplicații precum **Autodesk Fusion 360**.

## Format de fișier STP - Mai multe informații

Fișierele STP sunt salvate pe disc în format simplu de fișier ASCII. Acestea conțin informații despre modele 3D sub formă de text simplu, care pot fi citite de aplicațiile CAD/CAM pentru încărcarea acestor modele.

Fișierele STP sunt, de asemenea, salvate cu extensia .step și constă dintr-o secvență de înregistrări. Caracteristicile importante ale acestor fișiere includ:

* Setul de caractere este definit ca puncte de cod ale ISO 10646.
* „ISO-10303-21;” sunt primele caractere din prima înregistrare.
* Comentariile sunt înconjurate de caractere „/*” și „*/”.
* Ultima înregistrare conține „END-ISO-10303-21;” dacă fișierul STEP este conform versiunii 2002.
* În cazul în care este conform versiunii 2016, pot exista una sau mai multe semnături digitale după „END-ISO-10303-21;” terminator.
* Întreruperile de linie sunt notate cu „\N\”, iar întreruperile de pagină sunt notate cu „\F\”.

## Deschideți fișierele STP

Fișierele STP pot fi deschise în STP Viewers, precum și în Text Editors.

### Deschideți fișierele STP cu vizualizatoare STP

Diverse aplicații CAD pot deschide fișiere STP pentru vizualizare pe Windows, MacOS și Linux. Acestea includ:

* Autodesk Fusion 360 (multiplatformă)
* FreeCAD (multplatform)
* IMSI TurboCAD (Windows, Mac)
* Dassault Systems CATIA (WINdows, Linux)

### Deschideți fișierele STP cu editori de text

Fișierele STP sunt salvate ca fișiere text simplu. Acest lucru face posibilă deschiderea fișierelor STP cu editori de text. Editorii de text populari, cum ar fi Notepad și Notepad++ pe sistemul de operare Windows și Apple TextEdit pe MacOS pot deschide fișiere STP. Odată deschis într-un editor de text, utilizatorul poate edita proprietățile fișierului STP. Cu toate acestea, poate duce la coruperea fișierului în cazul actualizării incorect a proprietăților.

## Cum se convertesc fișiere STP

Există mai multe aplicații care pot converti fișierele STP în alte formate de fișiere. Aplicațiile CAD care pot converti fișiere STP includ:

* Autodesk Fusion 360
* IMSI TurboCAD
* Siemens Solid Edge

În plus față de acestea, există mai multe aplicații online care pot converti fișiere STP în alte formate de fișiere. Aceste aplicații online vă permit să încărcați fișierul STP pe serverele cloud, unde sunt convertite în formatul dorit și returnate înapoi pentru descărcare.

Autodesk Fusion 360 poate converti fișierele STP în următoarele formate de fișiere 3D și CAD.

* [OBJ](/ro/3d/obj/)
* [3MF](/ro/3d/3mf/)
* [DWG](/ro/cad/dwg/)
* [DXF](/ro/cad/dxf/)
* [ASM](/ro/cad/asm/)
* [IGES](/ro/cad/iges/)
* [STL](/ro/cad/stl/)
* [FBX](/ro/3d/fbx/)
* F3D
* [USD](/ro/3d/usd/)

## Referințe

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

