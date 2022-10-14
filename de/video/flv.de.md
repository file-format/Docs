---
date: 2019-10-11
keywords: "flv, .flv, flv-Dateiformat, .flv-Dateiformat, .flv-Erweiterung, flv-Erweiterung, flv-Videoformat"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Erfahren Sie mehr über das FLV-Dateiformat und APIs, die FLV-Dateien erstellen und öffnen können."
title: "FLV-Dateiformat"
linktitle: "FLV"
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Was ist eine FLV-Datei? ##

FLV (Flash Video) ist ein Containerdateiformat mit der Erweiterung .flv. FLV wird zur Bereitstellung von Audio-/Videoinhalten über das Internet mithilfe von Adobe Flash Player oder Adobe Air verwendet. Die Daten in FLV-Dateien sind genauso kodiert wie SWF-Dateien. Die direkte Unterstützung wurde Flash Player 7 im Jahr 2003 hinzugefügt. Adobe-Systeme erstellten F4V im Jahr 2007 aufgrund der Einschränkungen von FLV.

### Codierung ###

FLV-Dateien enthalten Video-Bitstreams von Sorenson Spark, einer proprietären Variante des H.263-Videostandards. Es ist das erforderliche Komprimierungsformat für Flash Player 6 und 7. Version 8 von Flash Player unterstützt On2 TrueMotion VP6-Videobitstreams. Es ist das empfohlene Komprimierungsformat für Flash Player 8 und höher. FLV unterstützt Audio in MP3, Nellymoser Asao Codec und den Open-Source-Speex-Codec. Es unterstützt auch unkomprimiertes Audio oder Audio im ADPCM-Format. AAC (HE-AAC/AAC SBR, AAC Main Profile und AAC-LC) werden von den aktuellen Versionen von Flash Player 9 unterstützt.

## Struktur ##

FLV-Dateien bestehen aus Header und Paketen. Eine FLV-Datei beginnt mit dem Header. Der Header hat die folgenden Felder.

- **Signatur**: Sein Wert ist FLV
- **Version**: Der Standardwert ist 1. Nur 0x01 ist gültig.
- **Flags**: 0x04 wird für Audio und 0x01 für Video verwendet, also wird 0x05 sowohl für Audio als auch für Video verwendet.
- **Kopfzeilengröße**: Der Standardwert ist 9. Er wird verwendet, um eine neuere erweiterte Kopfzeile zu überspringen.

Nach dem Header kommen die Pakete. Die FLV-Datei ist in mehrere Pakete aufgeteilt, die als FLV-Tags bezeichnet werden und 15-Byte-Header haben. Die Pakete enthalten die Metadaten für Audio, Video, Skripte, Verschlüsselungsinformationen und Nutzdaten. Die FLV-Pakete haben die folgenden Felder.

- **Reserviert**: Es ist für FMS reserviert und sollte 0 sein.
- **Filter**: Gibt an, ob die Pakete gefiltert werden oder nicht.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Pakettyp**: Dies definiert den Inhaltstyp im Paket.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Datengröße**: Dies bezeichnet die Länge der Nachricht.
- **Timestamp Lower**: Hier wird der Zeitstempel in Millisekunden gespeichert, zu dem die Tag-Daten gelten. Es wird für das erste Paket auf NULL gesetzt.
- **Timestamp Upper**: Erweiterung zum Erstellen eines uint32_be-Werts.
- **Stream-ID**: Diese wird für den ersten Stream auf NULL gesetzt.
- **Payload Data**: Dies sind die Daten basierend auf dem Pakettyp.

## Verweise ##

- [Flash-Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

