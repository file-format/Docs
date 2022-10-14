---
date: 2019-10-11
keywords: "srt, .srt, srt-Dateiformat, .srt-Dateiformat, .srt-Erweiterung, srt-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Erfahren Sie mehr über das SRT-Dateiformat und APIs, die SRT-Dateien erstellen und öffnen können."
title: "SRT-Dateiformat"
linktitle: "SRT"
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Was ist eine SRT-Datei? ##

SRT (SubRip-Dateiformat) ist eine einfache Untertiteldatei, die im SubRip-Dateiformat mit der Erweiterung .srt gespeichert wird. Es enthält eine fortlaufende Anzahl von Untertiteln, Start- und Endzeitstempel und Untertiteltext. SRT-Dateien ermöglichen das Hinzufügen von Untertiteln zu Videoinhalten nach der Produktion.

## Struktur der SRT-Datei ##

Jeder Untertitel besteht aus vier Teilen in der SRT-Datei.

1. Ein numerischer Zähler, der die Nummer oder Position des Untertitels anzeigt.
1. Start- und Endzeit des Untertitels getrennt durch --> Zeichen
1. Untertiteltext in einer oder mehreren Zeilen.
1. Eine Leerzeile, die das Ende des Untertitels anzeigt.

### Beispiel für SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Zur Angabe der Uhrzeit wird das Format *Stunden:Minuten:Sekunden,Millisekunden (00:00:00.000)* verwendet.

## Formatierung von SRT-Dateien ##

Die Formatierung von SRT-Dateien wird von HTML-Tags abgeleitet. Die Formatierungs-Tags für die SRT-Datei sind unten aufgeführt.

| Wirkung | Stichworte |
| --- | --- |
|Fett|**\ <b>...\</b> ** oder {b}...{/b}|
|Kursiv|**\ <i>...\</i> ** oder **{i}...{/i}**|
|Unterstrichen|**\ <u>...\</u> ** oder **{u}...{/u}**|
|Schriftfarbe|**\ <font color="white">...\</font> **|
|Zeilenposition|**{\a3}** (gibt an, dass der Text ab Zeile 3 erscheinen soll)

## SubRip-Software ##

SubRip ist ein kostenloses Softwareprogramm, das unter Windows läuft. Es extrahiert Untertitel und deren Timings aus verschiedenen Videoformaten und speichert die Untertitel im SRT-Format. SubRip verwendet optische Zeichenerkennung, um Untertitel aus Live-Videos, anderen Videodateien und DVDs zu extrahieren.

## Verweise ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
