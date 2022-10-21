---
date: 2019-10-11
keywords: "step, .step, Step-Dateiformat, Schritt-Dateien öffnen, .step-Erweiterung, Step-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "STEP-Dateiformat"
linktitle: "SCHRITT"
description: "Erfahren Sie mehr über das STEP-Dateiformat und APIs, die STEP-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Was ist eine STEP-Datei?

Die STEP-Datei ist ein weit verbreitetes Datenaustauschformat für Computer Aided Design (CAD). Sie wurde 1994 vom ISO-Komitee unter dem Namen „ISO 10303-21“ standardisiert. ISO 10303-21 definiert den Kodierungsmechanismus zur Darstellung von Daten in der EXPRESS-Datenmodellierungssprache. Eine STEP-Datei wird auch als p21-Datei und STEP Physical File bezeichnet. Die für die STEP-Datei verwendeten Dateierweiterungen sind .stp und .step.

## Grundlegende Geschichte

1994 wurde die ursprüngliche Teil-21-Spezifikation herausgegeben. Es enthält einige Fehler, die durch die technische Berichtigung von 1996 korrigiert wurden. Die zweite Ausgabe wurde 2002 veröffentlicht und enthielt die Berichtigung und Erweiterungen für mehrere Datenabschnitte. Die dritte Ausgabe wurde 2016 veröffentlicht und fügte Anker- und Referenzabschnitte hinzu, die es ermöglichten, Entitäten und Werte in externen Dateien zu speichern. UTF-8-Unterstützung wurde von Zeichenfolgen hinzugefügt. Digitale Signaturen wurden hinzugefügt, um den Inhalt der Datei zu überprüfen und Anmeldeinformationen zu validieren. Die Unterstützung für das Komprimieren und Speichern der Austauschstruktur mit ZIP wurde ebenfalls hinzugefügt.

## STEP-Dateiformat

Das Klartextformat für eine STEP-Datei besteht aus einer Folge von Datensätzen. Der Zeichensatz ist als Codepunkte von ISO 10646 definiert. „ISO-10303-21;“ sind die ersten Zeichen im ersten Datensatz. Kommentare sind von den Zeichen „/*“ und „*/“ umgeben. Der letzte Datensatz enthält "END-ISO-10303-21;" wenn die STEP-Datei der Version 2002 entspricht. Falls es der Version 2016 entspricht, können nach dem „END-ISO-10303-21;“ eine oder mehrere digitale Signaturen stehen; Terminator. Zeilenumbrüche werden mit „\N\“ und Seitenumbrüche mit „\F\“ gekennzeichnet.

Die STEP-Datei ist in Abschnitte unterteilt und ihre Namen sind reservierte Begriffe. Alle Abschnitte enden mit dem „ENDSEC“-Record und müssen in der unten gezeigten Reihenfolge stehen.

- **HEADER**: Dies ist ein obligatorischer und nicht wiederholbarer Abschnitt. Es besteht aus den folgenden Einheiten:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: Dies ist ein optionaler, sich nicht wiederholender Abschnitt, der in der Version 2016 eingeführt wurde. Es definiert die externen Namen für Instanzen, damit sie referenziert werden können.
- **REFERENZ**: Dies ist ein optionaler, sich nicht wiederholender Abschnitt, der auch in der Version 2016 eingeführt wurde. Jeder Eintrag in diesem Abschnitt ordnet einen Eintrag/Wert-Instanznamen einer Instanz/einem Wert in einer externen Datei zu.
- **DATA**: Dies ist ein optionaler, wiederholbarer Abschnitt, der den Kerninhalt der Modellinstanz enthält.
- **SIGNATURE**: Dies ist ein optionaler wiederholbarer Abschnitt, der in der Version 2016 eingeführt wurde. Es enthält die digitale Signatur, um den Inhalt der Datei zu überprüfen oder Anmeldeinformationen zu validieren.

## Verweise

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

