---
date: 2019-10-11
keywords: flv, .flv, flv file format, .flv file format, .flv extension, flv extension, flv video format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Lthuilleamh faoi fhormáid comhaid flv agus APIs is féidir a chruthú agus a oscailt comhad flvs.
title: FFoirm Comhad LVat
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Cad is comhad flv ann? ##

FLV (Flash Video) is a container file format with the .flv extension. FLV is used to deliver audio/video content over the internet by using the Adobe Flash Player or Adobe Air. The data in FLV files are encoded in the same way as SWF files. The direct support was added to Flash Player 7 in 2003. Chruthaigh córais Adobe F4V in 2007 mar gheall ar shrianta FLV.

### Ionchódú ###

FLV files contain video bitstreams of Sorenson Spark which are a proprietary variant of the H.263 video standard. It is the required compression format for Flash Player 6 and 7. Leagan 8 de thacaíocht Flash Player le haghaidh sruthanna giotán físe On2 TrueMotion VP6. Is é an fhormáid comhbhrú molta do Flash Player 8 agus níos airde. Tacaíonn FLV le fuaim i MP3, Nellymoser Asao Codec, agus an CODEC foinse oscailte Speex. Tacaíonn sé freisin le fuaime neamh-chomhbhrúite nó fuaime formáid ADPCM. Tacaíonn na leaganacha is déanaí de Flash Player 9 le AAC (HE-AAC/AAC SBR, AAC Main Profile, agus AAC-LC).

## Struchtúr ##

Comhaid FLV comhdhéanta de Ceanntásc agus Paicéid. Tosaíonn comhad flv leis an gCeanntásc. Tá na réimsí seo a leanas ag an gceanntásc.

- **Síniú**: Is é an luach FLV
- **Version**: Its default value is 1. Níl ach 0x01 bailí.
- **Bratacha**: úsáidtear 0x04 le haghaidh fuaime agus 0x01 le haghaidh físeáin agus mar sin úsáidtear 0x05 le haghaidh fuaime agus físe araon.
- **Header Size**: The default value is 9. Úsáidtear é chun ceanntásc leathnaithe níos nuaí a scipeáil.

Tar éis an ceanntásc tagann na Paicéid. Roinntear an comhad FLV ina ilphaicéid ar a dtugtar clibeanna FLV a bhfuil ceanntásca 15 beart acu. Sna paicéid tá na meiteashonraí le haghaidh fuaime, físeáin, scripteanna, faisnéis criptithe agus pálasta. Tá na réimsí seo a leanas ag na paicéid FLV.

- **Forchoimeádta**: Tá sé curtha in áirithe do FMS agus ba cheart go mbeadh 0 ann.
- **Scagaire**: Léiríonn an bhfuil na paicéid scagtha nó nach bhfuil.
  - "**0**: Níl gá le réamhphróiseáil. Úsáidtear é seo le haghaidh comhaid neamhchriptithe."
  - "**1**: Réamhphróiseáil riachtanach. Úsáidtear é seo le haghaidh comhaid criptithe"
- **Cineál Paicéad**: Sainmhíníonn sé seo an cineál ábhair sa phaicéad.
  - "**8**: Fuaim"
  - "**9**: Físeán"
  - "**18**: Sonraí Scripte"
- **Méid Sonraí**: Seasann sé seo fad na teachtaireachta.
- **Stampa Ama Íochtarach**: Stórálann sé seo an stampa ama ina milleasoicindí ag a bhfuil feidhm ag sonraí na gclibeanna. Tá sé socraithe go NULLComment don chéad phaicéad.
- **Stampa Ama Uachtarach**: Síneadh chun luach uint32_be a chruthú.
- **Aitheantas an tSrutha**: Tá sé seo socraithe go NULLComment don chéad sruth.
- **Sonraí Pá-Ualach**: Seo na sonraí atá bunaithe ar an gcineál paicéad.

## Tagairtí ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

