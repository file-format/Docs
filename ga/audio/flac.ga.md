---
date: 2019-12-13
keywords: flac, flac file format, .flac extension, flac file, flac vs mp3
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lthuilleamh faoi fhormáid comhaid FLAC agus APIs is féidir a chruthú agus a oscailt comhad FLACs.
title: FFoirm Comhad LACat
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Cad is comhad FLAC ann?

Is formáid chódú fuaime comhbhrú gan chailliúint é FLAC (Codc Fuaime Gan Chailleadh) arna forbairt ag Fondúireacht Xiph.Org. Is formáid oscailte saor ó ríchíosa é FLAC a shábháiltear leis an síneadh .flac. Is gnách go laghdaítear fuaime digiteach comhbhrúite ag baint úsáide as an algartam FLAC go 50 go 70 faoin gcéad i méid. Is féidir comhaid FLAC a dhí-chomhbhrú go dtí cóip chomhionann de na comhaid fuaime bunaidh.

## Formáid comhaid FLAC saor in aisce,

Seo forbhreathnú ar an sruth giotán FLAC.

- **marcóir fLaC**: Cuirtear an marcóir seo le tús an tsrutha. Ina dhiaidh sin tá bloc meiteashonraí amháin nó níos mó.
- **Blocanna Meiteashonraí**: tacaíonn FLAC le 128 cineál bloic meiteashonraí; faoi láthair sainmhínítear iad seo a leanas.
  - "**STREAMINFO**: Tá an fhaisnéis faoin sruth iomlán ann."
  - "**IARRATAS**: Úsáideann feidhmchláir aitheantais tríú páirtí é seo."
  - "**PADING**: Úsáidtear é chun spás a chur in áirithe do mheiteashonraí más rud é go gcuirfear na meiteashonraí in eagar tar éis iad a ionchódú. Nuair a chuirtear na meiteashonraí in eagar, cuirtear na meiteashonraí iarbhír in ionad an stuála."
  - "** TÁBLA**: Tábla roghnach chun pointí a lorg a stóráil."
  - "**VORBIS_COMMENT**: Úsáidtear é chun péirí eochair/luacha inléite daonna a stóráil."
  - "**BILEOG CUSPÓIRÍ**: Úsáidtear é chun faisnéis bileog leideanna a stóráil."
  - "**PICTIÚR**: Úsáidtear é chun pictiúir a stóráil."
- **FRAME**: Tá na sonraí fuaime comhdhéanta de fhráma fuaime amháin nó níos mó.
  - "**FRAME_HEADER**: Tá an fhaisnéis bhunúsach faoin sruth ann."
  - "**FOFRAME**: Chun an chastacht a laghdú, déantar fo-fhrámaí aonair a chódú ar leithligh laistigh de fhráma (fráma amháin in aghaidh an chainéil)."
  - "**FRAME_FOOTER**: Tá CRC an fhráma iomlán ann."

## Stair Achomair ar Fhormáid Chomhaid FLAC

Josh Coalson began the development of FLAC in 2000. Eisíodh an chéad leagan de FLAC ar 20 Iúil 2001. Corpraíodh FLAC faoi bhratach Xiph.Org ar 20 Eanáir 2003. Aistríodh forbairt FLAC chuig stór Xiph.Org git nuair a scaoileadh leagan 1.3.0 ar 26 Márta 2013.

## Comhdhéanamh Tionscadal FLAC

Tá na nithe seo a leanas i dtionscadal FLAC:

- Formáidí sruth.
- Formáid coimeádán simplí don sruth (FLAC).
- libFLAC: Leabharlann de ionchódóirí tagartha, díchódaithe, agus comhéadan meiteashonraí.
- libFLAC++: Fillteán réad-dhírithe do libFLAC.
- flac: Clár ordú-líne chun sruthanna FLAC a ionchódú agus a dhíchódú.
- metaflac: Eagarthóir meiteashonraí ordú-líne do FLAC.
- Breiseáin ionchuir le haghaidh seinnteoirí ceoil mar Winamp, XMMX, etc.
- Formáid coimeádán Ogg (Ogg FLAC).

## Dearadh FLAC

Ag brath ar dhlús agus aimplitiúid an cheoil, is féidir méid an chomhaid chomhbhrúite a bheith 80% níos lú ná an comhad bunaidh.

### Ionchódóir Foinse ###

- Ní thacaíonn sé ach le samplaí slánuimhir agus ní thacaíonn sé le snámhphointe. Is féidir leis réiteach giotán PCM a láimhseáil ó 4 go 32 giotán in aghaidh an tsampla agus ráta samplála ó 1Hz go 65,535 Hz. Tá ionchódú FLAC teoranta do 24 giotán in aghaidh an tsampla.
- Is féidir cainéil a ghrúpáil chun leas a bhaint as comhghaolta idirchainéil chun comhbhrú a mhéadú.
- Úsáidtear seiceálacha CRC chun frámaí truaillithe a aithint.
- Chun samplaí fuaime a chomhshó, úsáideann FLAC tuar líneach.

### Meiteashonraí ###

- Tacaíonn FLAC le ReplayGain (a úsáidtear chun treise fuaime a bhrath agus a normalú).
- Úsáideann FLAC an córas céanna a úsáidtear i dtuairimí Vorbis le haghaidh clibeála.
- úsáideann formhór na bhfeidhmchlár FLAC libFLAC le haghaidh ionchódú/díchódaithe.
- Eagraítear libFLAC API i sruthanna, sruthanna iniarraidh, agus comhaid chun astarraingt ó bhunsruth giotán FLAC a mhéadú.

### Comhbhrú ###

Úsáideann libFLAC leibhéil chomhbhrú ó 0 go 8 áit arb é 0 an leibhéal is tapúla agus is é 8 an leibhéal comhbhrú is moille. Bíonn na comhaid chomhbhrúite gan chailliúint i gcónaí cé go bhfuil an trádáil idir luas agus méid.

## FLAC vs MP3
Is formáid chomhbhrú chaillte é an MP3 a chiallaíonn go bhféadfadh sé cuid den fhuaim a ghearradh chun a méid a laghdú tar éis comhbhrú a chur i bhfeidhm. De bharr an méid, is formáid comhaid gan chailliúint é FLAC a chiallaíonn go bhfuil tú in ann an fhuaim a chloisteáil ina fhoirm ghlan. Ba iad na formáidí comhaid gan chailliúint níos luaithe ná CDA nó WAV nach raibh mórán spáis-éifeachtach mar FLAC. Léireoidh an tábla seo a leanas an chomparáid idir an dá fhormáid seo do roinnt téarmaí tábhachtacha:

|Téarma|FLAC|MP3|
---|---|---|
|**Cáilíocht Sonraí**|Níl aon chailliúint ar shonraí fuaime| Seans go gcaillfear roinnt sonraí agus sonraí fuaime á gcomhbhrú|
|**Méid**|Méid comhaid níos mó i gcomparáid le formáidí caillte. Mar sin teastaíonn toilleadh stórála níos mó| Méid comhaid níos lú, oiriúnach le himirt ar ghléasanna dlúth fuaime gan mórán spáis stórála |
||**Ceanglais chrua-earraí** | Fearas fuaime ardcháilíochta agus toilleadh stórála ollmhór de dhíth | Is féidir leabharlanna fuaime ollmhóra a shábháil i spás stórála níos lú. Oiriúnach do ghléasanna boise, amhail seinnteoirí fuaime nó fóin phóca|
|**Dáilte ar an idirlíon**|Ní féidir é a dháileadh go héasca ar an idirlíon mar gheall ar mhéid ollmhór na gcomhad |Déanann dlúthmhéid comhaid é a dháileadh thar an idirlíon|
|**Comhoiriúnacht**|An CODEC éisteachta ceoil agus fuaime is coitianta atá comhoiriúnach beagnach i bhfad le gach feiste ar an phláinéid Ag luí le ríomhairí pearsanta glúine nua, fóin, glacadóirí AV, seinnteoirí blu-ray, gléasanna sruthú cosúil le Roku nó Fire TV|

## Tagairtí ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

