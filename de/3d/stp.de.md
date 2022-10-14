---
date: 2022-01-31
keywords: "stp, .stp, stp-Dateiformat, wie man stp-Dateien öffnet, .stp-Erweiterung, stp-Erweiterung"
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "STP-Dateiformat"
linktitle: "STP"
description: "Erfahren Sie mehr über das STP-Dateiformat und APIs, die STP-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Was ist eine STP-Datei?

Eine STP-Datei ist eine 3D-CAD-Datei, die für den Austausch von Produktdaten zwischen CAD- und CAM-Anwendungen verwendet wird. Es enthält Informationen über 3D-Objekte und wird ähnlich wie das Dateiformat **STEP** gespeichert. STP-Dateien erleichtern den Datenaustausch zwischen Anwendungen gemäß [STEP](/de/3d/step/) Application Protocols ISO 10303-2xx. Diese ISO definiert den Kodierungsmechanismus für die Datendarstellung in der EXPRESS-Datenmodellierungssprache. STP-Dateien können in Anwendungen wie **Autodesk Fusion 360** geöffnet werden.

## STP-Dateiformat – Weitere Informationen

STP-Dateien werden im reinen ASCII-Dateiformat auf der Disc gespeichert. Diese enthalten 3D-Modellinformationen als Klartext, die von CAD/CAM-Anwendungen zum Laden dieser Modelle gelesen werden können.

STP-Dateien werden auch mit der Erweiterung .step gespeichert und bestehen aus einer Folge von Datensätzen. Zu den hervorstechenden Merkmalen dieser Dateien gehören:

* Der Zeichensatz ist als Codepunkte von ISO 10646 definiert.
* "ISO-10303-21;" sind die ersten Zeichen im ersten Datensatz.
* Kommentare sind von den Zeichen „/*“ und „*/“ umgeben.
* Der letzte Datensatz enthält "END-ISO-10303-21;" wenn die STEP-Datei der Version 2002 entspricht.
* Falls es der Version 2016 entspricht, können nach dem „END-ISO-10303-21;“ eine oder mehrere digitale Signaturen stehen; Terminator.
* Zeilenumbrüche werden mit "\N\" und Seitenumbrüche mit "\F\" gekennzeichnet.

## Öffnen Sie STP-Dateien

STP-Dateien können sowohl in STP-Viewern als auch in Texteditoren geöffnet werden.

### Öffnen Sie STP-Dateien mit STP-Viewern

Verschiedene CAD-Anwendungen können STP-Dateien zur Anzeige unter Windows, MacOS und Linux öffnen. Diese beinhalten:

* Autodesk Fusion 360 (plattformübergreifend)
* FreeCAD (plattformübergreifend)
* IMSI-TurboCAD (Windows, Mac)
* Dassault Systems CATIA (Windows, Linux)

### STP-Dateien mit Texteditoren öffnen

STP-Dateien werden als Nur-Text-Dateien gespeichert. Dadurch ist es möglich, STP-Dateien mit Texteditoren zu öffnen. Gängige Texteditoren wie Notepad und Notepad++ unter Windows OS und Apple TextEdit unter MacOS können STP-Dateien öffnen. Nach dem Öffnen in einem Texteditor kann der Benutzer die Eigenschaften der STP-Datei bearbeiten. Es kann jedoch zu einer Beschädigung der Datei führen, wenn die Eigenschaften falsch aktualisiert werden.

## So konvertieren Sie STP-Dateien

Es gibt mehrere Anwendungen, die STP-Dateien in andere Dateiformate konvertieren können. Zu den CAD-Anwendungen, die STP-Dateien konvertieren können, gehören:

* Autodesk-Fusion 360
* IMSI-TurboCAD
* Solid Edge von Siemens

Darüber hinaus gibt es mehrere Online-Apps, die STP-Dateien in andere Dateiformate konvertieren können. Mit diesen Online-Apps können Sie Ihre STP-Datei auf Cloud-Server hochladen, wo sie in Ihr gewünschtes Format konvertiert und zum Herunterladen zurückgegeben werden.

Autodesk Fusion 360 kann STP-Dateien in die folgenden 3D- und CAD-Dateiformate konvertieren.

* [OBJ](/de/3d/obj/)
* [3MF](/de/3d/3mf/)
* [DWG](/de/cad/dwg/)
* [DXF](/de/cad/dxf/)
* [ASM](/de/cad/asm/)
* [IGES](/de/cad/iges/)
* [STL](/de/cad/stl/)
* [FBX](/de/3d/fbx/)
*F3D
* [USD](/de/3d/usd/)

## Verweise

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360] (https://www.autodesk.com/products/fusion-360/overview)

