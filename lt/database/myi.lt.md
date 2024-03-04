---
date: 2020-11-11
keywords: myi, .myi, myi file format, how to open myi files, .myi extension, myi extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI failo formaat
linktitle: MYI
description: Luždirbkite apie MYI failo formatą ir API, kurios gali sukurti ir atidaryti MYI failąs.
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Kas yra MYI failas? ##

MYI taip pat žinomas kaip MySQL MyISAM indekso failas. Jis naudojamas MySQL lentelės MyISAM indeksams saugoti. MySQL duomenų bazės indeksas apibrėžia lentelės struktūrą ir apima valdymo mechanizmą lentelių vientisumui patikrinti.

## MYI failo formatas ##

MYI failą sudaro dvi dalys: antraštė ir pagrindinės reikšmės.

### MYI antraštė ###

Antraštėje pateikiama informacija apie parinktis, failų dydžius ir raktus. MySQL raktai sukuriami tokia komanda kaip

```sql
CREATE [UNIQUE] INDEX.
```

Failai, kurie skaito ir rašo MYI failus, yra ./myisam kataloge. Jame yra šie failai:

- mi_open.c: šiame faile yra tvarka, kuri rašo kiekvieną antraštės skyrių.
- mi_create.c: šiame faile yra veiksmų, kurie iškviečia mi_open.c procedūras.
- myisamdef.h: šis failas turi struktūros apibrėžimus.

Antraštėje yra šie skyriai:

- būsena: būseną parašė mi_open.c, mi_state_info_write(). Ši struktūra faile atsiranda vieną kartą.
- bazė: bazę parašė mi_open.c, mi_base_info_write(). MI_BASE_INFO yra atitinkama myisamdef.h bazės struktūra. Ši struktūra faile atsiranda vieną kartą.
- keydef: Keydef yra parašytas mi_open.c, mi_keydef_write(). MI_KEYDEF yra atitinkama myisamdef.h keydef struktūra. Tai daugkartinė struktūra, kuri rodoma kiekvienam indeksui.
- recinfo: recinfo parašė mi_open.c, mi_recinfo_write(). MI_COLUMNDEF yra atitinkama recinfo struktūra myisamdef.h. Tai kelių įvykių struktūra, kuri pasirodo vieną kartą kiekviename rakte rodomame lauke.

### Pagrindinės reikšmės ###

Pages in MySQL are called blocks. Key values are in blocks. A block contains information from only one index. Each key contains the entire contents of all the columns. The normal block length is 0x0400 (1024) bytes. The pointer has a fixed size (4-byte) number for fixed-row tables that contains an ordinal row number. If the key is null then the byte is 0x00. Įprastas blokas yra užpildytas mažiausiai 65% ir paprastai yra 80%.

Faile myisamdef.h yra ši informacija, išreikšta konstantomis. Maksimalus raktų skaičius yra 32 (MI_MAX_KEY), o maksimalus segmentų skaičius rakte yra 16 (MI_MAX_KEY_SEG). Maksimalus rakto ilgis yra 500 (MI_MAX_KEY_LENGTH). Maksimalus bloko ilgis yra 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Nuorodos Nr.

- [The .MYI File](https://dev.mysql.com/doc/dev/mysql-server/latest/)

