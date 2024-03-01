---
date: 2020-11-11
keywords: myi, .myi, myi file format, how to open myi files, .myi extension, myi extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI-tiedostolomakeat
linktitle: MYI
description: Lansaitse MYI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MYI-tiedostons.
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Mikä on MYI-tiedosto? ##

MYI tunnetaan myös nimellä MySQL MyISAM Index -tiedosto. Sitä käytetään MySQL:n MyISAM-taulukon indeksien tallentamiseen. MySQL-tietokantaindeksi määrittelee taulukon rakenteen ja sisältää ohjausmekanismin taulukoiden eheyden tarkistamiseksi.

## MYI-tiedostomuoto ##

MYI-tiedostossa on kaksi osaa, otsikko ja avainarvot.

### MYI-otsikko ###

Otsikko sisältää tietoja vaihtoehdoista, tiedostokoosta ja avaimista. MySQL:n avaimet luodaan esim. komennolla

```sql
CREATE [UNIQUE] INDEX.
```

MYI-tiedostoja lukevat ja kirjoittavat tiedostot ovat ./myisam-hakemistossa. Siinä on seuraavat tiedostot:

- mi_open.c: Tämä tiedosto sisältää rutiinit, jotka kirjoittavat otsikon jokaisen osan.
- mi_create.c: Tässä tiedostossa on rutiinit, jotka kutsuvat mi_open.c-rutiineja.
- myisamdef.h: Tällä tiedostolla on rakenteen määritelmät.

Otsikossa on seuraavat osiot:

- tila: Tilan kirjoittaa mi_open.c, mi_state_info_write(). Tämä rakenne esiintyy tiedostossa kerran.
- base: Kanta on kirjoittanut mi_open.c, mi_base_info_write(). MI_BASE_INFO on vastaava rakenne tiedostossa myisamdef.h. Tämä rakenne esiintyy tiedostossa kerran.
- keydef: Keydef on kirjoittanut mi_open.c, mi_keydef_write(). MI_KEYDEF on vastaava rakenne myisamdef.h:n keydefille. Se on usean esiintymisen rakenne, joka näkyy jokaiselle indeksille.
- recinfo: Recinfo on kirjoittanut mi_open.c, mi_recinfo_write(). MI_COLUMNDEF on vastaava rakenne myisamdef.h:n recinfolle. Se on usean esiintymän rakenne, joka esiintyy kerran kustakin avaimessa esiintyvästä kentästä.

### Avainarvot ###

Pages in MySQL are called blocks. Key values are in blocks. A block contains information from only one index. Each key contains the entire contents of all the columns. The normal block length is 0x0400 (1024) bytes. The pointer has a fixed size (4-byte) number for fixed-row tables that contains an ordinal row number. If the key is null then the byte is 0x00. Normaali lohko on vähintään 65 % täynnä ja tyypillisesti 80 % täynnä.

Myisamdef.h-tiedosto sisältää seuraavat tiedot vakioina ilmaistuna. Avainten enimmäismäärä on 32 (MI_MAX_KEY) ja segmenttien enimmäismäärä avaimessa on 16 (MI_MAX_KEY_SEG). Avaimen enimmäispituus on 500 (MI_MAX_KEY_LENGTH). Lohkon enimmäispituus on 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Viitteet ##

- {{HYPERLINKKI1}}

