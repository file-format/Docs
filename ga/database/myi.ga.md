---
date: 2020-11-11
keywords: myi, .myi, myi file format, how to open myi files, .myi extension, myi extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MFoirm Chomhaid YIat
linktitle: MYI
description: Ltuilleamh faoi fhormáid comhaid MYI agus APIs ar féidir leo comhad MYI a chruthú agus a oscailts.
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Cad is Comhad MYI ann? ##

Tugtar an comhad Innéacs MySQL MyISAM ar MYI freisin. Úsáidtear é chun innéacsanna don tábla MyISAM a stóráil ag MySQL. Sainmhíníonn innéacs bunachar sonraí MySQL struchtúr an tábla agus tá an mheicníocht rialaithe ann chun sláine táblaí a sheiceáil.

## Formáid Chomhaid MYI ##

Tá dhá chuid i gcomhad MYI, an ceanntásc, agus na príomhluachanna.

### Ceanntásc MYI ###

Tá faisnéis sa cheanntásc faoi roghanna, méideanna comhaid, agus eochracha. Cruthaítear na heochracha i MySQL le hordú cosúil le

```sql
CREATE [UNIQUE] INDEX.
```

Tá na comhaid a léann agus a scríobhann comhaid MYI san eolaire ./myisam. Tá na comhaid seo a leanas aige:

- mi_open.c: Tá na gnáthaimh a scríobhann gach cuid den cheanntásc sa chomhad seo.
- mi_create.c: Tá na gnáthaimh a ghlaonn gnáthaimh mi_open.c orthu sa chomhad seo.
- myisamdef.h: Tá na sainmhínithe struchtúir ag an gcomhad seo.

Tá na hailt seo a leanas ag an gceanntásc:

- luaigh: Tá an stát scríofa ag mi_open.c, mi_state_info_write(). Tarlaíonn an struchtúr seo uair amháin sa chomhad.
- bonn: Tá an bonn scríofa ag mi_open.c, mi_base_info_write(). Is é an MI_BASE_INFO an struchtúr comhfhreagrach don bhonn i myisamdef.h. Tarlaíonn an struchtúr seo uair amháin sa chomhad.
- keydef: Tá an eochair-def scríofa ag mi_open.c, mi_keydef_write(). Is é an MI_KEYDEF an struchtúr comhfhreagrach don eochairchosaint i myisamdef.h. Is struchtúr il-tarlaithe é atá le feiceáil do gach innéacs.
- recinfo: Tá an recinfo scríofa ag mi_open.c, mi_recinfo_write(). Is é an MI_COLUMNDEF an struchtúr comhfhreagrach don recinfo i myisamdef.h. Is struchtúr tarluithe iolracha é a fheictear uair amháin de gach réimse a fheictear in eochair.

### Príomhluachanna ###

Pages in MySQL are called blocks. Key values are in blocks. A block contains information from only one index. Each key contains the entire contents of all the columns. The normal block length is 0x0400 (1024) bytes. The pointer has a fixed size (4-byte) number for fixed-row tables that contains an ordinal row number. If the key is null then the byte is 0x00. Bíonn gnáthbhloc 65% ar a laghad lán agus 80% lán go hiondúil.

Tá an fhaisnéis seo a leanas curtha in iúl i dtairisigh sa chomhad myisamdef.h. Is é 32 (MI_MAX_KEY) uaslíon na n-eochracha agus is é 16 (MI_MAX_KEY_SEG) uaslíon na míreanna in eochair. Is é 500 (MI_MAX_KEY_LENGTH) uasfhad na heochrach. Is é 16384 (MI_MAX_KEY_BLOCK_LENGTH) uasfhad an bhloic.

## Tagairtí ##

- [The .MYI File](https://dev.mysql.com/doc/dev/mysql-server/latest/)

