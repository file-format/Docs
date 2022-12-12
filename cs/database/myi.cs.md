---
date: 2020-11-11
keywords: myi, .myi, formát souboru myi, jak otevřít soubory myi, přípona .myi, přípona myi
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru MYI
linktitle: MYI
description: "Přečtěte si o formátu souboru MYI a rozhraních API, která mohou vytvářet a otevírat soubory MYI."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Co je soubor MYI? ##

MYI je také známý jako soubor MySQL MyISAM Index. Používá se k ukládání indexů pro tabulku MyISAM pomocí MySQL. Index databáze MySQL definuje strukturu tabulky a obsahuje kontrolní mechanismus pro kontrolu integrity tabulek.

## Formát souboru MYI ##

Soubor MYI má dvě části, záhlaví a hodnoty klíče.

### MYI záhlaví ###

Záhlaví obsahuje informace o možnostech, velikostech souborů a klíčích. Klíče v MySQL se vytvářejí pomocí příkazu jako

```sql
CREATE [UNIQUE] INDEX.
```

Soubory, které čtou a zapisují soubory MYI, jsou v adresáři ./myisam. Obsahuje následující soubory:

- mi_open.c: Tento soubor obsahuje rutiny, které zapisují jednotlivé části záhlaví.
- mi_create.c: Tento soubor obsahuje rutiny, které volají rutiny mi_open.c.
- myisamdef.h: Tento soubor má definice struktury.

Záhlaví má následující sekce:

- state: Stav je zapsán pomocí mi_open.c, mi_state_info_write(). Tato struktura se v souboru vyskytuje jednou.
- base: Báze je zapsána pomocí mi_open.c, mi_base_info_write(). MI_BASE_INFO je odpovídající struktura pro základ v myisamdef.h. Tato struktura se v souboru vyskytuje jednou.
- keydef: Keydef je zapsán pomocí mi_open.c, mi_keydef_write(). MI_KEYDEF je odpovídající struktura pro keydef v myisamdef.h. Je to struktura s více výskyty, která se objevuje pro každý index.
- recinfo: Recinfo je zapsáno mi_open.c, mi_recinfo_write(). MI_COLUMNDEF je odpovídající struktura pro recinfo v myisamdef.h. Je to struktura s více výskyty, která se objeví jednou v každém poli, které se objeví v klíči.

### Klíčové hodnoty ###

Stránky v MySQL se nazývají bloky. Klíčové hodnoty jsou v blocích. Blok obsahuje informace pouze z jednoho indexu. Každý klíč obsahuje celý obsah všech sloupců. Normální délka bloku je 0x0400 (1024) bajtů. Ukazatel má pevnou velikost (4 bajty) pro tabulky s pevnými řádky, které obsahují pořadové číslo řádku. Pokud je klíč null, pak je bajt 0x00. Normální blok je zaplněn alespoň z 65 % a obvykle z 80 %.

Soubor myisamdef.h obsahuje následující informace vyjádřené v konstantách. Maximální počet klíčů je 32 (MI_MAX_KEY) a maximální počet segmentů v klíči je 16 (MI_MAX_KEY_SEG). Maximální délka klíče je 500 (MI_MAX_KEY_LENGTH). Maximální délka bloku je 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Reference ##

- [Soubor .MYI](https://dev.mysql.com/doc/internals/en/the-myi-file.html)

