---
date: 2019-10-11
keywords: "WEBM, Was ist eine WEBM-Datei, WEBM-Dateiformat"
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Erfahren Sie mehr über das WEBM-Dateiformat und APIs, die WEBM-Dateien erstellen und öffnen können."
title: "WEBM - WebM-Videodateiformat"
linktitle: "WEBM"
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Was ist eine WEBM-Datei?

Eine Datei mit der Erweiterung .webm ist eine Videodatei, die auf dem offenen, lizenzfreien WebM-Dateiformat basiert. Es wurde für die gemeinsame Nutzung von Videos im Internet entwickelt und definiert die Dateicontainerstruktur einschließlich Video- und Audioformaten. WebM ist 100 % kostenlos und implementiert qualitativ hochwertige Lösungen basierend auf offenen Technologien wie HTML, HTTP und TCP/IP, die für jedermann zur Implementierung offen stehen. WebM wurde speziell für die Bereitstellung von Videos im Web entwickelt, wodurch es für das Streaming mit geringem Rechenaufwand optimiert ist. Dadurch eignet es sich für die Videowiedergabe auf jedem Gerät, insbesondere auf stromsparenden Netbooks, Handhelds und Tablets.

## WEBM-Dateiformat

Die WebM-Dateistruktur basiert auf einer Teilmenge des Containerdateiformats Matroska [MKV](/de/video/mkv/). Die in einer WebM-Datei verfügbaren Videostreams werden mit den hocheffizienten VP8- oder VP9-Komprimierungstechnologien komprimiert. Ebenso werden die Audiostreams in einer WebM-Datei mit den von der [Xiph Foundation](https://www.xiph.org/) entwickelten Vorbis- oder Opus-Codecs komprimiert. Alle diese Videos und Audio-Codecs sind lizenzfrei und können kostenlos verwendet werden.

Im Folgenden finden Sie die zusammengefassten Spezifikationen für das WebM-Dateiformat.

|Feld|Beschreibung|
---|---|
|MIME-Typ |video/webm|
|Nur-Audio-MIME-Typ |audio/webm|
|Einheitliche Typkennung| org.webmproject.webm|
|Video-Codec-Name| VP8 oder VP9|
|Audio-Codec-Name| Vorbis oder Opus|

### WebM-Elemente

WebM ist eine Teilmenge der Matroska-Spezifikationen und bietet Unterstützung für einige der Matroska-Funktionen. Es folgt eine Beschreibung der unterstützten Elemente.

####EBML

|Name |Beschreibung|
---|---|
|EBML|Stellen Sie die EBML-Merkmale der folgenden Daten ein. Jedes EBML-Dokument muss damit beginnen.|
|EBMLVersion |Die Version des EBML-Parsers, der zum Erstellen der Datei verwendet wurde.|
|EBMLReadVersion|Die minimale EBML-Version, die ein Parser unterstützen muss, um diese Datei zu lesen.|
|EBMLMaxIDLength |Die maximale Länge der IDs, die Sie in dieser Datei finden (4 oder weniger in Matroska).|
|EBMLMaxSizeLength|Die maximale Länge der Größen, die Sie in dieser Datei finden (8 oder weniger in Matroska). Die am Anfang eines Elements angegebene Elementgröße wird dadurch nicht überschrieben. Elemente mit einer angegebenen Größe, die größer ist als die von EBMLMaxSizeLength zugelassene Größe, gelten als ungültig.|
|DocType|Ein String, der den Dokumenttyp beschreibt, der diesem EBML-Header folgt (in unserem Fall "webm").|
|DocTypeVersion|Die Version des DocType-Interpreters, die zum Erstellen der Datei verwendet wurde.|
|DocTypeReadVersion|Die minimale DocType-Version, die ein Interpreter unterstützen muss, um diese Datei zu lesen.|

#### Globale Elemente

Momentan wird nur das „Void“-Element unterstützt, das zum Annullieren beschädigter Daten verwendet wird, um unerwartetes Verhalten bei der Verwendung beschädigter Daten zu vermeiden. Der Inhalt wird verworfen. Wird auch verwendet, um Platz in einem Unterelement für die spätere Verwendung zu reservieren.

#### Segment
Dieses Element enthält alle anderen Elemente der obersten Ebene (Ebene 1). Typischerweise besteht eine Matroska-Datei aus 1 Segment.

#### Informationen zur Metasuche

Die folgende Suche nach Informationen wird unterstützt.

|Elementname |Beschreibung|
---|---|
|SeekHead |Enthält die Position eines anderen Elements der Ebene 1.|
|Suchen |Enthält einen einzelnen Sucheintrag für ein EBML-Element.|
|SeekID |Die dem Elementnamen entsprechende binäre ID.|
|SeekPosition |Die Position des Elements im Segment in Oktetten (0 = erstes Element der Ebene 1).|

## Verweise

* [WebM](https://www.webmproject.org/)
* [WebM-Code-Repositories](https://www.webmproject.org/code/#webp-repositories)

