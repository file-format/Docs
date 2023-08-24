---
date: 2020-08-12
keywords: jfif, .jfif, formato file jfif, come aprire file jfif, estensione .jfif, estensione jfif
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: File JFIF - Che cos'è un file .jfif?
linktitle: JFIF
description: "Ulteriori informazioni sul formato di file JFIF e sulle API che possono creare e aprire file JFIF."
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Che cos'è un file JFIF?

JFIF (JPEG File Interchange Format (JFIF)) è un file in formato immagine che utilizza l'estensione .jfif. JFIF si basa su JIF (JPEG Interchange Format) riducendo la complessità e risolvendone i limiti.

## Breve storia di JFIF

Lo sviluppo del documento JFIF è stato guidato da Eric Hamilton e alla fine del 1991 è stato stabilito un accordo sulla prima versione. La versione 1.02 è stata pubblicata il 7 settembre 1992. RFC 2046 ha specificato che il formato JFIF viene utilizzato per trasmettere immagini JPEG su Internet. JFIF è stato pubblicato da ECMA nel 2009 ed è stato standardizzato da ITU-T nel 2011 come Raccomandazione T.871 e da ISO/IEC nel 2013 come ISO/IEC 10918-5

## Formato file JFIF ##

Un file JFIF è costituito da una sequenza di marcatori come definito nella parte 1 dello standard JPEG. Ogni marker è composto da due byte (FF seguito da un byte che specifica il tipo di marker). I marker possono essere indipendenti o indicare l'inizio di un segmento di marker.

JFIF consente a più componenti come Y, Cb, Cr, di avere risoluzioni diverse ma il loro allineamento non è definito. A differenza di JPEG, JFIF può fornire informazioni su risoluzione e proporzioni. JFIF definisce anche il modello di colore da utilizzare.

### Struttura del file ##

|Segmento|Codice|Descrizione|
|---|---|---|
|SOI|FF D8|Inizio dell'immagine|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|segmenti marker aggiuntivi|
|SOS|FF DA|Inizio della scansione|
||dati immagine compressi||
|EOI|FF D9|Fine immagine|

Lo standard JFIF definisce i seguenti segmenti:

### Segmento marker JFIF APP0 ###

È un segmento obbligatorio che contiene i parametri dell'immagine. Può anche contenere una miniatura incorporata non compressa.

|Campo|Dimensione (byte)|Descrizione|
|---|---|---|
|indicatore APP0|2|FF E0|
|Lunghezza|2|Lunghezza del segmento escluso il marker APP0|
|Identificatore|5|JFIF (4A 46 49 46 00) in ASCII terminato da un byte null|
|Versione JFIF|2|Versione di JFIF|
|Unità di densità|1|Unità per i seguenti campi di densità di pixel</br> 00 : Nessuna unità; il rapporto di aspetto larghezza:altezza pixel è uguale a Ydensity:Xdensity</br> 01 : Pixel per pollice</br> 02 : Pixel per centimetro|
|Xdensity|2|Densità pixel orizzontale maggiore di zero|
|Ydensity|2|Densità pixel verticali maggiore di zero|
|Xthumbnail|1|Conteggio pixel orizzontali della miniatura RGB incorporata. Può essere zero|
|Ythumbnail|1|Conteggio pixel verticali della miniatura RGB incorporata. Può essere zero|
|Dati miniatura|3 × n|Dati miniatura raster RGB a 24 bit non compressi|

### Estensione JFIF Segmento marker APP0 ###

Questa è una sezione facoltativa che, se definita, deve seguire immediatamente il segmento del marker JFIF APP0. Questa sezione è supportata da JFIF versione 1.02 e successive e consente l'incorporamento di miniature in tre diversi formati.

|Campo|Dimensione (byte)|Descrizione|
|---|---|---|
|indicatore APP0|2|FF E0|
|Lunghezza|2|Lunghezza del segmento escluso il marker APP0|
|Identificatore|5|JFXX (4A 46 58 58 00) in ASCII terminato da un byte null|
|Formato miniatura|1|Specifica il formato dati utilizzato per la seguente miniatura incorporata:</br> 10 : formato JPEG</br> 11 : 1 byte per pixel formato palettizzato</br> 13 : 3 byte per pixel formato RGB|
|Dati miniatura|variabile||

## Conversione di JFIF in altri formati di file immagine

JFIF può essere convertito nei formati di file immagine più diffusi come [PNG](/it/image/png/), [JPG](/it/image/jpeg/) e [PDF](/it/pdf/).

## Riferimenti ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

