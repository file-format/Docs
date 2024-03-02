---
date: 2019-10-11
keywords: f4v, .f4v, f4v file format, .f4v file format, .f4v extension, f4v extension, f4v video format, how to open f4v files, what are f4v files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltuilleamh faoi fhormáid comhaid F4V agus APIs is féidir comhad F4V a chruthú agus a oscailtes
title: FFoirm Chomhaid 4Vat
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Cad is comhad F4V ann? ##

Is comhad físe é F4V (Flash MP4 Video File) a shábháiltear leis an síneadh .f4v. Tá sé bunaithe ar an fhormáid comhaid meán ISO bonn (MPEG-4 Cuid 12). Tá sé an-chosúil le [MP4](/video/mp4/) agus is é sin an fáth go dtugtar Flash MP4 air go neamhfhoirmiúil freisin. Bhí teorainneacha ag [FLV](/video/flv/) le linn inneachar H.264/ACC a shruthú, rud a d’fhág gur chruthaigh Adobe Systems an fhormáid nua F4V. Is féidir le Flash Player comhaid F4V a imirt ó scaoileadh Flash Player 9 Update 3.

## Struchtúr na gcomhad F4V ##

Tá formáid comhaid F4V bunaithe ar fhormáid comhaid meán bonn ISO (MPEG-4 Cuid 12) agus tá sé an-chosúil leis an bhformáid MP4. Le haghaidh sonraí maidir leis an struchtúr, féach ar an leathanach [MP4](/video/mp4/). Is é an difríocht mhór idir F4V agus MP4 na formáidí meiteashonraí is féidir le F4V a stóráil. Tugtar thíos liosta de na formáidí meiteashonraí a dtacaíonn an fhormáid F4V leo.

- **Tag box**: Additional four optional tag boxes (auth, title, dscp, cprt) within the Movie (moov) box.
- **Bosca Meiteashonraí XMP**: Tagann an bosca seo díreach i ndiaidh an bhosca Movie (moov). Leis seo, is féidir leis an gcomhad meiteashonraí XMP a chur in iúl do scannán SWF trí ActionScript.
- **ilstbox**: Tá an bosca seo taobh istigh den bhosca Meta (meta) agus is féidir roinnt clibeanna meiteashonraí a bheith ann. Tá na cineálacha sonraí tacaithe tugtha thíos.
  - "**0**: Sonraí Saincheaptha."
  - "**1**: Sonraí Téacs."
  - "**12, 14**: Sonraí Dénártha"
  - "**21**: Sonraí Cineálacha."
- **Bosca Meiteashonraí Track Téacs**: Na samplaí téacs (téacs nó tx3g) taobh istigh den Bosca Sonraí Meán (mdat). Féadfaidh na boscaí meiteashonraí seo a leanas a bheith ann.
  - "**Bosca stíle**: Sonraíochtaí stíl téacs."
  - "**Bosca Aibhsithe**: Sonraíonn an raon téacs atá le aibhsiú."
  - "**Bosca Dath Aibhsithe**: Sonraíonn an dath aibhsithe don téacs."
  - "**Bosca karaoke**: Sonraigh na meiteashonraí karaoke."
  - "**Bosca Moill Scrollaigh**: Sonraítear an mhoill scrollaithe."
  - "**Bosca Fritháireamh Scáth Buail**: Sonraíonn sé comhordanáidí fritháireamh an scáil titim don téacs."
  - "**Bosca Drop Scáth Alfa**: Sonraíonn sé an luach alfa scáile titim don téacs."
  - "**Bosca hipirtéacs**: Sonraítear an téacs hipirtéacs le téacs alt thar raon téacs."
  - "**Text Box Box**: Sainmhíníonn sé na comhordanáidí don bhosca téacs."
  - "**Bosca claonta**: Sonraítear caochadh do raon téacs."
  - "**Bosca Wrap Téacs**: Socraíonn sé an bhratach fillte don téacs."
  - "**Bosca Wrap Téacs**: Socraíonn sé an bhratach fillte don téacs."

## Tagairtí ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

