---
date: 2020-11-11
keywords: "myi, .myi, myi-Dateiformat, wie man myi-Dateien öffnet, .myi-Erweiterung, myi-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "MYI-Dateiformat"
linktitle: "MYI"
description: "Erfahren Sie mehr über das MYI-Dateiformat und APIs, die MYI-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Was ist eine MYI-Datei? ##

MYI ist auch als MySQL-MyISAM-Indexdatei bekannt. Es wird verwendet, um Indizes für die MyISAM-Tabelle von MySQL zu speichern. Der MySQL-Datenbankindex definiert die Struktur der Tabelle und enthält den Kontrollmechanismus zur Überprüfung der Integrität von Tabellen.

## MYI-Dateiformat ##

Die MYI-Datei besteht aus zwei Teilen, dem Header und den Schlüsselwerten.

### MYI-Header ###

Der Header enthält Informationen zu Optionen, Dateigrößen und Schlüsseln. Die Schlüssel in MySQL werden mit einem Befehl wie erstellt

```sql
CREATE [UNIQUE] INDEX.
```

Die Dateien, die MYI-Dateien lesen und schreiben, befinden sich im Verzeichnis ./myisam. Es hat die folgenden Dateien:

- mi_open.c: Diese Datei enthält die Routinen, die jeden Abschnitt des Headers schreiben.
- mi_create.c: Diese Datei enthält die Routinen, die mi_open.c-Routinen aufrufen.
- myisamdef.h: Diese Datei enthält die Strukturdefinitionen.

Die Kopfzeile hat die folgenden Abschnitte:

- state: Der Zustand wird von mi_open.c, mi_state_info_write() geschrieben. Diese Struktur kommt einmal in der Datei vor.
- base: Die Basis wird von mi_open.c, mi_base_info_write() geschrieben. Die MI_BASE_INFO ist die entsprechende Struktur für die Basis in myisamdef.h. Diese Struktur kommt einmal in der Datei vor.
- keydef: Die Keydef wird von mi_open.c, mi_keydef_write() geschrieben. Die MI_KEYDEF ist die entsprechende Struktur für die keydef in myisamdef.h. Es handelt sich um eine mehrfach vorkommende Struktur, die für jeden Index erscheint.
- Recinfo: Die Recinfo wird von mi_open.c, mi_recinfo_write() geschrieben. Die MI_COLUMNDEF ist die entsprechende Struktur für die recinfo in myisamdef.h. Es handelt sich um eine mehrfach vorkommende Struktur, die einmal für jedes Feld erscheint, das in einem Schlüssel vorkommt.

### Schlüsselwerte ###

Seiten werden in MySQL Blöcke genannt. Schlüsselwerte sind in Blöcken. Ein Block enthält Informationen aus nur einem Index. Jeder Schlüssel enthält den gesamten Inhalt aller Spalten. Die normale Blocklänge beträgt 0x0400 (1024) Bytes. Der Zeiger hat eine Zahl fester Größe (4 Byte) für Tabellen mit festen Zeilen, die eine Ordnungszeilennummer enthalten. Wenn der Schlüssel null ist, ist das Byte 0x00. Ein normaler Block ist mindestens zu 65 % und typischerweise zu 80 % gefüllt.

Die Datei myisamdef.h enthält die folgenden Informationen, ausgedrückt in Konstanten. Die maximale Anzahl von Schlüsseln ist 32 (MI_MAX_KEY) und die maximale Anzahl von Segmenten in einem Schlüssel ist 16 (MI_MAX_KEY_SEG). Die maximale Länge des Schlüssels beträgt 500 (MI_MAX_KEY_LENGTH). Die maximale Länge des Blocks beträgt 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Verweise ##

- [Die .MYI-Datei](https://dev.mysql.com/doc/dev/mysql-server/latest/)

