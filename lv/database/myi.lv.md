---
date: 2020-11-11
keywords: myi, .myi, myi file format, how to open myi files, .myi extension, myi extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI faila veidlapaat
linktitle: MYI
description: Lnopelniet par MYI faila formātu un API, kas var izveidot un atvērt MYI failus.
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Kas ir MYI fails? ##

MYI ir pazīstams arī kā MySQL MyISAM indeksa fails. To izmanto MySQL tabulas MyISAM indeksu glabāšanai. MySQL datu bāzes indekss nosaka tabulas struktūru un satur kontroles mehānismu, lai pārbaudītu tabulu integritāti.

## MYI faila formāts ##

MYI failam ir divas daļas — galvene un galvenās vērtības.

### MYI galvene ###

Galvenē ir informācija par opcijām, failu izmēriem un taustiņiem. MySQL atslēgas tiek izveidotas ar komandu, piemēram

```sql
CREATE [UNIQUE] INDEX.
```

Faili, kas lasa un raksta MYI failus, atrodas direktorijā ./myisam. Tam ir šādi faili:

- mi_open.c: šajā failā ir rutīnas, kas raksta katru galvenes sadaļu.
- mi_create.c: šim failam ir rutīnas, kas izsauc mi_open.c rutīnas.
- myisamdef.h: šim failam ir struktūras definīcijas.

Galvenē ir šādas sadaļas:

- stāvoklis: stāvokli raksta mi_open.c, mi_state_info_write(). Šī struktūra failā parādās vienreiz.
- bāze: bāzi raksta mi_open.c, mi_base_info_write(). MI_BASE_INFO ir atbilstošā struktūra myisamdef.h bāzei. Šī struktūra failā parādās vienreiz.
- keydef: Keydef raksta mi_open.c, mi_keydef_write(). MI_KEYDEF ir atbilstošā struktūra myisamdef.h keydef. Tā ir vairāku gadījumu struktūra, kas tiek parādīta katram rādītājam.
- recinfo: Recinfo ieraksta mi_open.c, mi_recinfo_write(). MI_COLUMNDEF ir atbilstošā struktūra recinfo failā myisamdef.h. Tā ir vairāku gadījumu struktūra, kas parādās vienu reizi katrā laukā, kas parādās atslēgā.

### Galvenās vērtības ###

Pages in MySQL are called blocks. Key values are in blocks. A block contains information from only one index. Each key contains the entire contents of all the columns. The normal block length is 0x0400 (1024) bytes. The pointer has a fixed size (4-byte) number for fixed-row tables that contains an ordinal row number. If the key is null then the byte is 0x00. Parasts bloks ir vismaz 65% piepildīts un parasti ir 80%.

Fails myisamdef.h satur šādu informāciju, kas izteikta konstantēs. Maksimālais taustiņu skaits ir 32 (MI_MAX_KEY), un maksimālais segmentu skaits atslēgā ir 16 (MI_MAX_KEY_SEG). Maksimālais atslēgas garums ir 500 (MI_MAX_KEY_LENGTH). Bloka maksimālais garums ir 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Atsauces Nr.

- [The .MYI File](https://dev.mysql.com/doc/dev/mysql-server/latest/)

