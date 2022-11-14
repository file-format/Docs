---
date: 2022-01-31
keywords: stp, .stp, formato file stp, come aprire file stp, estensione .stp, estensione stp
autore:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formato file STP
linktitle: STP
description: "Scopri il formato di file STP e le API che possono creare e aprire file STP."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Che cos'è un file STP?

Un file STP è un file CAD 3D utilizzato per lo scambio di dati di prodotto tra applicazioni CAD e CAM. Contiene informazioni sugli oggetti 3D e viene salvato in modo simile al formato file **STEP**. I file STP facilitano lo scambio di dati tra le applicazioni secondo i protocolli applicativi [STEP](/it/3d/step/) ISO 10303-2xx. Questa ISO definisce il meccanismo di codifica per la rappresentazione dei dati nel linguaggio di modellazione dei dati EXPRESS. I file STP possono essere aperti in applicazioni come **Autodesk Fusion 360**.

## Formato file STP - Ulteriori informazioni

I file STP vengono salvati su disco in un semplice formato di file ASCII. Questi contengono informazioni sui modelli 3D come testo normale che possono essere letti dalle applicazioni CAD/CAM per caricare questi modelli.

Anche i file STP vengono salvati con estensione .step e sono costituiti da una sequenza di record. Le caratteristiche salienti di questi file includono:

* Il set di caratteri è definito come punti di codice della ISO 10646.
* "ISO-10303-21;" sono i primi caratteri nel primo record.
* I commenti sono racchiusi tra i caratteri "/*" e "*/".
* L'ultimo record contiene "END-ISO-10303-21;" se il file STEP è conforme alla versione 2002.
* Nel caso sia conforme alla versione 2016, potrebbero esserci una o più firme digitali dopo "END-ISO-10303-21;" terminatore.
* Le interruzioni di riga sono indicate con "\N\" e le interruzioni di pagina con "\F\".

## Apri file STP

I file STP possono essere aperti nei visualizzatori STP e negli editor di testo.

### Apri i file STP con i visualizzatori STP

Varie applicazioni CAD possono aprire file STP per la visualizzazione su Windows, MacOS e Linux. Questi includono:

* Autodesk Fusion 360 (multipiattaforma)
* FreeCAD (multipiattaforma)
* IMSI TurboCAD (Windows, Mac)
* Dassault Systems CATIA (Windows, Linux)

### Apri file STP con editor di testo

I file STP vengono salvati come file di testo normale. Ciò consente di aprire file STP con editor di testo. Editor di testo popolari come Notepad e Notepad++ su Windows OS e Apple TextEdit su MacOS possono aprire file STP. Una volta aperto in un editor di testo, l'utente può modificare le proprietà del file STP. Tuttavia, può portare alla corruzione del file in caso di aggiornamento errato delle proprietà.

## Come convertire i file STP

Esistono diverse applicazioni in grado di convertire i file STP in altri formati di file. Le applicazioni CAD in grado di convertire file STP includono:

*Autodesk Fusion 360
* IMSI TurboCAD
* Siemens Solid Edge

Oltre a queste, ci sono diverse app online che possono convertire i file STP in altri formati di file. Queste app online ti consentono di caricare il tuo file STP su server cloud dove vengono convertiti nel formato desiderato e restituiti per il download.

Autodesk Fusion 360 può convertire file STP nei seguenti formati di file 3D e CAD.

* [OBJ](/it/3d/oggetto/)
* [3MF](/it/3d/3mf/)
* [DWG](/it/cad/dwg/)
* [DXF](/it/cad/dxf/)
* [ASM](/it/cad/asm/)
* [IGES](/it/cad/iges/)
* [STL](/it/cad/stl/)
* [FBX](/it/3d/fbx/)
* F3D
* [USD](/it/3d/USD/)

## Riferimenti

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

