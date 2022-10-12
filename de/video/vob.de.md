---
date: 2019-10-11
keywords: "vob, .vob, vob-Dateiformat, .vob-Dateiformat, .vob-Erweiterung, vob-Erweiterung, vob-Videoformat, vob-DVD-Dateien"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Erfahren Sie mehr über das VOB-Dateiformat und APIs, die VOB-Dateien erstellen und öffnen können."
title: "VOB-Dateiformat"
linktitle: "VOB"
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Was ist eine VOB-Datei? ##

VOB-Dateien werden normalerweise im Verzeichnis VIDEO_TS auf einer DVD mit der Erweiterung .vob gespeichert. VOB-Dateien enthalten Video- und Audiodaten sowie andere Daten wie Menüs und Untertitel. VOB basiert auf dem MPEG-2-Programmstreamformat, weist jedoch zusätzliche Einschränkungen und Spezifikationen für private Streams auf. VOB-Dateien sind eine strenge Teilmenge von MPEG-Programmstreams, daher sind alle VOB-Dateien MPEG-Programmstreams, aber alle MPEG-Programmstreams sind nicht VOB-kompatibel.

## Struktur des DVD-Videos ##

Wenn eine DVD auf einem Computer geöffnet wird, ist VIDEO_TS das oberste Verzeichnis mit AUDIO_TS. AUDIO_TS ist leer und wird nicht verwendet. Im Verzeichnis VIDEO_TS befinden sich VOB-, BUP- und IFO-Dateien. VOB-Dateien enthalten den MPEG-Inhalt. Diese werden in Stücke von 1 GB oder weniger Größe aufgeteilt, damit diese mit allen Betriebssystemen kompatibel sind. Die IFO-Dateien enthalten Informationen zu den Menüs und der Titelstruktur. Die BUK-Dateien sind Sicherungsdateien der gleichnamigen IFO-Dateien. Diese Dateien sollen physisch in einem separaten Bereich aufbewahrt werden, damit im Falle einer Beschädigung der IFO-Datei aufgrund einer physischen Beschädigung der DVD die BUK-Datei dieselben Informationen liefern kann.

### Physisches Layout ###

- Alle Dateien auf der Festplatte müssen zusammenhängend sein.
- Die zugehörigen Dateien sollten nebeneinander liegen (VOB, IFO, BUP).
- Die nummerierten Dateien sollten in aufsteigender Reihenfolge sein.

## Kopierschutz ##

Viele Video-DVDs sind verschlüsselt und verhindern das Kopieren von Daten von der DVD. Authentifizierungs- und Entschlüsselungsschlüssel werden benötigt, um die Dateien abzuspielen, die sich im nicht zugänglichen Lead-In-Bereich der DVD befinden. Diese Schlüssel werden von der CSS-Entschlüsselungssoftware verwendet, die im DVD-Player oder im Software-Player vorhanden ist. Ohne die Schlüssel können die Videodateien nicht abgespielt werden, da die Schlüssel beim Öffnen der Dateien angefordert werden.

## Verweise ##

- [VOB - Wikipedia](https://en.wikipedia.org/wiki/VOB)
- [Inside DVD-Video/Verzeichnisstruktur](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

