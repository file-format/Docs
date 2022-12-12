---
date: 2020-11-11
keywords: myi, .myi, format de fișier myi, cum se deschide fișierele myi, extensia .myi, extensia myi
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier MYI
linktitle: MYI
description: "Aflați despre formatul de fișier MYI și despre API-urile care pot crea și deschide fișiere MYI."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Ce este un fișier MYI? ##

MYI este cunoscut și ca fișierul MySQL MyISAM Index. Este folosit pentru a stoca indecși pentru tabelul MyISAM de către MySQL. Indexul bazei de date MySQL definește structura tabelului și conține mecanismul de control pentru a verifica integritatea tabelelor.

## Format de fișier MYI ##

Fișierul MYI are două părți, antetul și valorile cheie.

### Antet MYI ###

Antetul conține informații despre opțiuni, dimensiunile fișierelor și chei. Cheile din MySQL sunt create cu o comandă de genul

```sql
CREATE [UNIQUE] INDEX.
```

Fișierele care citesc și scriu fișiere MYI se află în directorul ./myisam. Are urmatoarele fisiere:

- mi_open.c: Acest fișier conține rutinele care scriu fiecare secțiune a antetului.
- mi_create.c: Acest fișier are rutinele care numesc rutine mi_open.c.
- myisamdef.h: Acest fișier are definițiile structurii.

Antetul are următoarele secțiuni:

- stare: starea este scrisă de mi_open.c, mi_state_info_write(). Această structură apare o dată în fișier.
- bază: baza este scrisă de mi_open.c, mi_base_info_write(). MI_BASE_INFO este structura corespunzătoare pentru baza din myisamdef.h. Această structură apare o dată în fișier.
- keydef: Keydef este scris de mi_open.c, mi_keydef_write(). MI_KEYDEF este structura corespunzătoare pentru keydef în myisamdef.h. Este o structură cu apariții multiple care apare pentru fiecare indice.
- reciinfo: Recinfo este scris de mi_open.c, mi_recinfo_write(). MI_COLUMNDEF este structura corespunzătoare pentru reciinfo din myisamdef.h. Este o structură cu apariții multiple care apare o dată din fiecare câmp care apare într-o cheie.

### Valori cheie ###

Paginile din MySQL se numesc blocuri. Valorile cheie sunt în blocuri. Un bloc conține informații dintr-un singur index. Fiecare cheie conține întregul conținut al tuturor coloanelor. Lungimea normală a blocului este de 0x0400 (1024) octeți. Indicatorul are un număr de dimensiune fixă (4 octeți) pentru tabelele cu rânduri fixe care conține un număr de rând ordinal. Dacă cheia este nulă, atunci octetul este 0x00. Un bloc normal este plin cu cel puțin 65% și este de obicei plin cu 80%.

Fișierul myisamdef.h conține următoarele informații exprimate în constante. Numărul maxim de chei este 32 (MI_MAX_KEY), iar numărul maxim de segmente dintr-o cheie este 16 (MI_MAX_KEY_SEG). Lungimea maximă a cheii este de 500 (MI_MAX_KEY_LENGTH). Lungimea maximă a blocului este 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Referințe ##

- [Fișierul .MYI](https://dev.mysql.com/doc/internals/en/the-myi-file.html)

