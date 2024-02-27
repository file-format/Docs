---
date: 2020-11-11
keywords: myi, .myi, myi file format, how to open myi files, .myi extension, myi extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI-filformularat
linktitle: MYI
description: Ltjene om MYI filformat og API'er, der kan oprette og åbne MYI fils.
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Hvad er en MYI-fil? ##

MYI er også kendt som MySQL MyISAM Index-filen. Det bruges til at gemme indekser for MyISAM-tabellen af MySQL. MySQL-databaseindekset definerer tabellens struktur og indeholder kontrolmekanismen til at kontrollere tabellers integritet.

## MYI filformat ##

MYI-filen har to dele, headeren og nøgleværdierne.

### MYI Header ###

Overskriften indeholder oplysninger om muligheder, filstørrelser og nøgler. Nøglerne i MySQL oprettes med en kommando som f.eks

```sql
CREATE [UNIQUE] INDEX.
```

De filer, der læser og skriver MYI-filer, er i ./myisam-mappen. Den har følgende filer:

- mi_open.c: Denne fil indeholder de rutiner, der skriver hver sektion af headeren.
- mi_create.c: Denne fil har de rutiner, der kalder mi_open.c rutiner.
- myisamdef.h: Denne fil har strukturdefinitionerne.

Overskriften har følgende sektioner:

- tilstand: Tilstanden er skrevet af mi_open.c, mi_state_info_write(). Denne struktur forekommer én gang i filen.
- base: Basen er skrevet af mi_open.c, mi_base_info_write(). MI_BASE_INFO er den tilsvarende struktur for basen i myisamdef.h. Denne struktur forekommer én gang i filen.
- keydef: Keydef er skrevet af mi_open.c, mi_keydef_write(). MI_KEYDEF er den tilsvarende struktur for keydef i myisamdef.h. Det er en struktur med flere forekomster, der vises for hvert indeks.
- recinfo: Recinfo er skrevet af mi_open.c, mi_recinfo_write(). MI_COLUMNDEF er den tilsvarende struktur for recinfo i myisamdef.h. Det er en struktur med flere forekomster, der vises én gang for hvert felt, der vises i en nøgle.

### Nøgleværdier ###

Pages in MySQL are called blocks. Key values are in blocks. A block contains information from only one index. Each key contains the entire contents of all the columns. The normal block length is 0x0400 (1024) bytes. The pointer has a fixed size (4-byte) number for fixed-row tables that contains an ordinal row number. If the key is null then the byte is 0x00. En normal blok er mindst 65 % fuld og er typisk 80 % fuld.

Myisamdef.h-filen indeholder følgende information udtrykt i konstanter. Det maksimale antal nøgler er 32 (MI_MAX_KEY), og det maksimale antal segmenter i en nøgle er 16 (MI_MAX_KEY_SEG). Nøglens maksimale længde er 500 (MI_MAX_KEY_LENGTH). Den maksimale længde af blokken er 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Referencer ##

- [The .MYI File](https://dev.mysql.com/doc/dev/mysql-server/latest/)

