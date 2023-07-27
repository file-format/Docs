---
date: 2020-11-11
keywords: myi, .myi, myi-bestandsindeling, hoe myi-bestanden te openen, .myi-extensie, myi-extensie
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI-bestandsindeling
linktitle: MYI
description: "Meer informatie over MYI-bestandsindeling en API's die MYI-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Wat is een MYI-bestand? ##

MYI is ook bekend als het MySQL MyISAM Index-bestand. Het wordt gebruikt om indexen voor de MyISAM-tabel op te slaan door MySQL. MySQL-database-index definieert de structuur van de tabel en bevat het controlemechanisme om de integriteit van tabellen te controleren.

## MYI-bestandsindeling ##

MYI-bestand bestaat uit twee delen, de koptekst en de sleutelwaarden.

### MIJN Koptekst ###

De kop bevat informatie over opties, bestandsgroottes en sleutels. De sleutels in MySQL worden gemaakt met een commando als

```sql
CREATE [UNIQUE] INDEX.
```

De bestanden die MYI-bestanden lezen en schrijven, bevinden zich in de map ./myisam. Het heeft de volgende bestanden:

- mi_open.c: dit bestand bevat de routines die elke sectie van de koptekst schrijven.
- mi_create.c: dit bestand heeft de routines die mi_open.c routines aanroepen.
- myisamdef.h: Dit bestand heeft de structuurdefinities.

De kop heeft de volgende secties:

- staat: de staat is geschreven door mi_open.c, mi_state_info_write(). Deze structuur komt één keer voor in het bestand.
- basis: de basis is geschreven door mi_open.c, mi_base_info_write(). De MI_BASE_INFO is de corresponderende structuur voor de basis in myisamdef.h. Deze structuur komt één keer voor in het bestand.
- keydef: De keydef is geschreven door mi_open.c, mi_keydef_write(). De MI_KEYDEF is de corresponderende structuur voor de keydef in myisamdef.h. Het is een meervoudige structuur die voor elke index wordt weergegeven.
- recinfo: De recinfo is geschreven door mi_open.c, mi_recinfo_write(). De MI_COLUMNDEF is de corresponderende structuur voor de recinfo in myisamdef.h. Het is een structuur met meerdere exemplaren die één keer voorkomt van elk veld dat in een sleutel voorkomt.

### Sleutelwaarden ###

Pagina's in MySQL worden blokken genoemd. Sleutelwaarden zijn in blokken. Een blok bevat informatie uit slechts één index. Elke sleutel bevat de volledige inhoud van alle kolommen. De normale bloklengte is 0x0400 (1024) bytes. De aanwijzer heeft een getal van vaste grootte (4-byte) voor tabellen met een vaste rij die een ordinaal rijnummer bevatten. Als de sleutel null is, is de byte 0x00. Een normaal blok is minimaal 65% vol en is typisch 80% vol.

Het bestand myisamdef.h bevat de volgende informatie uitgedrukt in constanten. Het maximum aantal sleutels is 32 (MI_MAX_KEY) en het maximum aantal segmenten in een sleutel is 16 (MI_MAX_KEY_SEG). De maximale lengte van de sleutel is 500 (MI_MAX_KEY_LENGTH). De maximale lengte van het blok is 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Referenties ##

- [Het .MYI-bestand](https://dev.mysql.com/doc/dev/mysql-server/latest/)

