---
date: 2020-11-11
keywords: myi, .myi, myi-filformat, hur man öppnar myi-filer, .myi-tillägg, myi-tillägg
författare:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI filformat
linktitle: MYI
description: "Lär dig om MYI-filformat och API:er som kan skapa och öppna MYI-filer." 
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Vad är en MYI-fil? ##

MYI är också känd som MySQL MyISAM Index-fil. Den används för att lagra index för MyISAM-tabellen av MySQL. MySQL databasindex definierar tabellens struktur och innehåller kontrollmekanismen för att kontrollera tabellernas integritet.

## MYI filformat ##

MYI-filen har två delar, rubriken och nyckelvärdena.

### MYI Header ###

Rubriken innehåller information om alternativ, filstorlekar och nycklar. Nycklarna i MySQL skapas med ett kommando som

```sql
CREATE [UNIQUE] INDEX.
```

Filerna som läser och skriver MYI-filer finns i ./myisam-katalogen. Den har följande filer:

- mi_open.c: Den här filen innehåller rutinerna som skriver varje sektion av rubriken.
- mi_create.c: Den här filen har de rutiner som anropar mi_open.c-rutiner.
- myisamdef.h: Den här filen har strukturdefinitionerna.

Rubriken har följande avsnitt:

- tillstånd: Tillståndet är skrivet av mi_open.c, mi_state_info_write(). Denna struktur förekommer en gång i filen.
- bas: Basen är skriven av mi_open.c, mi_base_info_write(). MI_BASE_INFO är motsvarande struktur för basen i myisamdef.h. Denna struktur förekommer en gång i filen.
- keydef: Keydef är skrivet av mi_open.c, mi_keydef_write(). MI_KEYDEF är motsvarande struktur för keydef i myisamdef.h. Det är en struktur med flera förekomster som visas för varje index.
- recinfo: Recinfon är skriven av mi_open.c, mi_recinfo_write(). MI_COLUMNDEF är motsvarande struktur för recinfo i myisamdef.h. Det är en struktur med flera förekomster som visas en gång i varje fält som förekommer i en nyckel.

### Nyckelvärden ###

Sidor i MySQL kallas block. Nyckelvärden är i block. Ett block innehåller information från endast ett index. Varje nyckel innehåller hela innehållet i alla kolumner. Den normala blocklängden är 0x0400 (1024) byte. Pekaren har ett nummer med fast storlek (4-byte) för tabeller med fast rad som innehåller ett ordningsradnummer. Om nyckeln är null är byten 0x00. Ett normalt block är minst 65 % fullt och är vanligtvis 80 % fullt.

Myisamdef.h-filen innehåller följande information uttryckt i konstanter. Det maximala antalet nycklar är 32 (MI_MAX_KEY) och det maximala antalet segment i en nyckel är 16 (MI_MAX_KEY_SEG). Den maximala längden på nyckeln är 500 (MI_MAX_KEY_LENGTH). Den maximala längden på blocket är 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Referenser ##

- [.MYI-filen](https://dev.mysql.com/doc/dev/mysql-server/latest/)

