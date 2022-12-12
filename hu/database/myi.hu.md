---
date: 2020-11-11
keywords: myi, .myi, myi fájlformátum, myi fájlok megnyitása, .myi kiterjesztése, myi kiterjesztése
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI fájlformátum
linktitle: MYI
description: "Ismerje meg a MYI fájlformátumot és az API-kat, amelyek MYI-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Mi az a MYI fájl? ##

A MYI MySQL MyISAM Index fájlként is ismert. A MySQL által a MyISAM tábla indexeinek tárolására szolgál. A MySQL adatbázis-index határozza meg a tábla szerkezetét, és tartalmazza a vezérlő mechanizmust a táblák integritásának ellenőrzéséhez.

## MYI fájlformátum ##

A MYI fájl két részből áll, a fejlécből és a kulcsértékekből.

### MYI fejléc ###

A fejléc információkat tartalmaz a beállításokról, a fájlméretekről és a kulcsokról. A MySQL kulcsai olyan paranccsal jönnek létre, mint

```sql
CREATE [UNIQUE] INDEX.
```

A MYI-fájlokat olvasó és író fájlok a ./myisam könyvtárban találhatók. A következő fájlokat tartalmazza:

- mi_open.c: Ez a fájl tartalmazza azokat a rutinokat, amelyek a fejléc egyes szakaszait írják.
- mi_create.c: Ez a fájl tartalmazza a mi_open.c rutinokat hívó rutinokat.
- myisamdef.h: Ez a fájl tartalmazza a szerkezet definícióit.

A fejléc a következő szakaszokat tartalmazza:

- állapot: Az állapotot a mi_open.c írja, mi_state_info_write(). Ez a struktúra egyszer fordul elő a fájlban.
- base: Az alapot a mi_open.c írja, mi_base_info_write(). A MI_BASE_INFO a myisamdef.h bázisának megfelelő struktúra. Ez a struktúra egyszer fordul elő a fájlban.
- keydef: A keydef-et a mi_open.c, mi_keydef_write() írja. A MI_KEYDEF a myisamdef.h kulcsdef megfelelő szerkezete. Ez egy többszörös előfordulású struktúra, amely minden indexnél megjelenik.
- recinfo: A recinfo-t a mi_open.c, mi_recinfo_write() írja. A MI_COLUMNDEF a myisamdef.h recinfo megfelelő struktúrája. Ez egy többszörös előfordulású struktúra, amely a kulcsban megjelenő minden mezőből egyszer jelenik meg.

### Kulcsértékek ###

A MySQL oldalait blokknak nevezzük. A kulcsértékek blokkokban vannak megadva. Egy blokk csak egy indexből tartalmaz információt. Mindegyik kulcs tartalmazza az összes oszlop teljes tartalmát. A normál blokkhossz 0x0400 (1024) bájt. A mutató fix méretű (4 bájtos) számmal rendelkezik a sorszámot tartalmazó fix soros táblázatokhoz. Ha a kulcs nulla, akkor a bájt 0x00. Egy normál blokk legalább 65%-ban, és általában 80%-ban tele van.

A myisamdef.h fájl a következő információkat tartalmazza konstansokban kifejezve. A kulcsok maximális száma 32 (MI_MAX_KEY), és a szegmensek maximális száma egy kulcsban 16 (MI_MAX_KEY_SEG). A kulcs maximális hossza 500 (MI_MAX_KEY_LENGTH). A blokk maximális hossza 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Referenciák ##

- [A .MYI fájl](https://dev.mysql.com/doc/internals/en/the-myi-file.html)

