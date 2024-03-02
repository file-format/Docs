---
date: 2019-12-09
keywords: arc, .arc, arc file format, how to open arc files, .arc extension, arc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: AFoirm Comhad RCat
linktitle: ARC
description: Ltuilleamh faoi fhormáid comhaid ARC agus APIs ar féidir leo comhad ARC a chruthú agus a oscailts.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Cad is comhad ARC ann?

Is formáid chomhbhrú sonraí agus chartlainne gan chailliúint é ARC arna fhorbairt ag System Enhancement Associates (SEA). Tugtar ARC ar fhormáid an chomhaid agus ar an bhfeidhmchlár a chruthaíonn é. Bhí an-tóir ar ARC le linn laethanta tosaigh an BBS diailithe toisc gur chomhcheangail sé gnéithe comhbhrú agus cartlannú iolrach comhad sa chomhad céanna. Cuireadh [ZIP](/compression/zip/) in ionad ARC níos déanaí, rud a chuir cóimheasa comhbhrú níos fearr ar fáil.

Úsáideann roinnt cineálacha comhaid cartlainne neamhghaolmhara an síneadh comhad .arc mar an fhormáid ARC a úsáideann an Chartlann Idirlín chun acmhainní iomadúla gréasáin a stóráil, formáid ARC éagsúil a úsáideann cartlannaí FreeArc, formáid dhifriúil a úsáideann Nintendo le haghaidh acmhainní, etc. .

## Stair Achomair ar Fhormáid Chomhaid ARC

The ARC program was written by Thom Henderson of System Enhancement Associates in 1985. Rinne an clár seo comhaid a ghrúpáil isteach i gcomhad cartlainne amháin agus comhbhrúite freisin iad. Bhain na comhaid a ghin an clár ARC úsáid as an síneadh .arc. D’eisigh SEA an cód foinse do ARC i 1986 agus d’aistrigh Howard Chu ARC chuig Unix agus Atari ST i 1987.

D’fhorbair Phil Katz PKARC agus PKXARC chun comhaid a chartlannú agus a bhaint. D'oibrigh na comhaid le formáid comhaid ARC agus bhí siad i bhfad níos tapúla. Murab ionann agus ARC, roinn Katz na feidhmeanna comhbhrú agus cartlannaithe idir dhá chomhad dhifriúla rud a laghdaigh an riachtanas cuimhne chun iad a rith.

Tar éis an dlí idir SEA agus Katz, tharraing SEA siar ón margadh earraí scaireanna agus d'fhorbair ARC+Plus le comhéadan úsáideora lánscáileáin. Níl an fhormáid ARC coitianta ar ríomhaire níos mó.

## Formáid Chomhaid ARC

Is éard atá sa chomhad ARC ná seicheamh ceanntásc comhaid agus comhad ina dhiaidh sin marcóir deireadh na cartlainne mar a thaispeántar thíos.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### Ceanntásc Comhad ARC ###

|Fritháireamh|Lipéad|Cineál|Luach|Cur Síos|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Modh|
|02|ARCFNT|DS|12|ainm an chomhaid|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Méid comhbhrúite|
|13|ARCDAT|DW|0000|Dáta an chomhaid (MSDOS) |
|15|ARCTIM|DW|0000|Am comhaid (MSDOS) |
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Méid neamh-chomhbhrúite|
|1D|ARCFIL|DS|ARCNSZ| |

### Modhanna Comhbhrú ###

Léiríonn beart an mhodha comhbhrú an modh comhbhrú a úsáidtear. Seo a leanas na modhanna comhbhrú a úsáidtear don chomhad ARC.

|Modh|Ainm|Cur Síos|
|---|---|---|
|0|Stóráilte|Ní úsáidtear comhbhrú|
|1|Pacáilte|Ionchódú arís agus arís eile ar fhad reatha (RLE)|
|2|Fáscadh|Ionchódú Huffman|
|3|Crúite|LZW le maolán 4K, cóid 12 ghiotán|
|4|Crunched|An chéad phacáil, ansin maolán LZW 4K le 12 ghiotán|
|5|Crúite|Pacáil, LZW, maolán 4K, fad athraitheach (9-12 giotán)|
|6|Squashed|LZW, maolán 8K, fad athraitheach (9-13 giotán) |
|7|Brúite|Pacáil, ansin maolán LZW 8K, 2-13 giotán (PAK 1.0)|
|8| Driogaire | Huffman dinimiciúil le maolán 8K (PAK 2.0) |

## Tagairtí

- [ARC (file format) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

