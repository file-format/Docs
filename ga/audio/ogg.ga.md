---
date: 2019-12-13
keywords: ogg, ogg file format, .ogg extension, ogg audio format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltuilleamh faoi fhormáid comhaid OGG agus APIs ar féidir leo comhad OGG a chruthú agus a oscailts.
title: OComhad GG - Ogg Vorbis Fuaime File
linktitle: OGG
menu:
  docs:
    parent: "audio"
lastmod: 2020-23-12
---

## Cad is comhad OGG ann?

Is Comhad Fuaime Comhbhrúite Ogg Vorbis é OGG a shábháiltear leis an síneadh .ogg. Úsáidtear comhaid OGG chun sonraí fuaime a stóráil agus is féidir faisnéis ealaíontóirí agus rianta agus meiteashonraí a áireamh freisin. Is formáid coimeádán oscailte agus saor in aisce é OGG atá á chothabháil ag Fondúireacht Xiph.Org.

## Stair Achomair ar Formáid Chomhaid OGG

Cuireadh tús le tionscadal Ogg mar chuid de thionscadal níos mó i 1993 agus tugadh Squish air ach mar gheall ar thrádmharc a bhí ann cheana, athainmníodh é go OggSquish. Cuireadh síos air mar iarracht chun formáid fuaime comhbhrúite solúbtha a chruthú le haghaidh feidhmchláir fuaime nua-aimseartha. Scaradh tagairt OGG ó Vorbis ar 2 Meán Fómhair, 2000.

OGM was created in 2002 due to the lack of formal video support in OGG. This allowed embedding video from the Microsoft DirectShow framework into an OGG-based wrapper. By 2006, OGG was supported by many video game engines and was commonly used to encode free content. The Free Software Foundation started a campaign on May 15, 2007, to increase the use of Vorbis as a superior alternative to MP3. Faoi 30 Meitheamh, 2009, ba é OGG an t-aon fhormáid coimeádáin a fuair tacaíocht ó chur i bhfeidhm HTML5 Firefox 3.5.

## Formáid Chomhaid OGG

Is éard atá i bhformáid OGG ná píosaí sonraí. Tugtar leathanach Ogg ar gach smután. Tosaíonn gach leathanach le OggS chun Formáid Ogg a shainaithint. Sa cheanntásc tá an tsraithuimhir agus uimhir an leathanaigh a shainaithníonn gach leathanach mar chuid de shraith. Tá na comhpháirteanna seo a leanas sa leathanach.

- **Ceanntásc Leathanaigh**
  - "**Patrún Gabhála (32 giotán)**: Úsáidtear é seo le haghaidh sioncrónaithe agus comhaid OGG á pharsáil."
  - "**Leagan(8 giotán)**: Léiríonn sé an leagan den sruth giotaí Ogg."
  - "**Cineál Ceanntásc(8 giotán)**: Léiríonn sé an cineál leathanaigh."

| Giotán | Luach | Cur Síos |
| --- | --- | --- |
| 0 | 0x01 | Léiríonn sé gurb é an chéad phaicéad den leathanach ná leanúint leis an bpaicéad roimhe sin sa sruth giotán loighciúil. |
| 1 | 0x02 | Léiríonn sé gurb é an leathanach seo an chéad leathanach sa sruth giotán loighciúil. |
| 2 | 0x04 | Léiríonn sé gurb é an leathanach seo an ceann deireanach sa sruth giotán loighciúil. |

  - "**Suíomh granule (64 giotán)**: Is é an marcóir ama a chinneann an CODEC a bhrí."
  - "**Sraithuimhir Bitstream(32 giotán)**: Is í an tsraithuimhir a shainaithníonn an leathanach a bhaineann le sruth giotán loighciúil ar leith."
  - "**Seicheamh leathanaigh (32 giotán)**: Léiríonn sé seicheamh an leathanaigh agus an chéad leathanach ag tosú ag 0."
  - "**Seic(32 giotán)**: Soláthraíonn sé seic CRC32 de shonraí iomlána an leathanaigh."
  - "**Deighleoga leathanaigh (8 ngiotán)**: Léiríonn sé líon na míreanna ar an leathanach."
  - "**Tábla deighleog**: Is sraith de luachanna 8 ngiotán é a léiríonn fad gach míre i gcorp an leathanaigh."
- **Meiteashonraí**: Is é VorbisComment an meicníocht is mó a dtacaítear leis chun meiteashonraí a stóráil. I measc meicníochtaí eile tá:
  - "Bloic meiteashonraí FLAC"
  - "Cnámharlach Ogg"
  - "Teanga Mharcála Meáin Leanúnach"

## Tagairtí ##

- [OGG - Wikipedia](https://en.wikipedia.org/wiki/Ogg)

