---
date: 2019-10-11
keywords: step, .step, step file format, how to open step files, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SFoirm Comhad TEPat
linktitle: STEP
description: Ltuilleamh faoi fhormáid comhaid CÉIM agus APIs ar féidir leo comhad CÉIM a chruthú agus a oscailts.
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Cad is comhad CÉIM ann?

Is formáid malartaithe sonraí é comhad CÉIM a úsáidtear go forleathan le haghaidh dearadh ríomhchuidithe (CAD). Caighdeánaigh an coiste ISO é i 1994 faoin ainm ISO 10303-21. Sainíonn ISO 10303-21 an mheicníocht ionchódaithe chun sonraí a léiriú i dteanga samhaltaithe sonraí EXPRESS. Tugtar Comhad P21-Comhad agus Comhad Fisiciúil CÉIM ar chomhad CÉIM freisin. Is iad na síntí comhad a úsáidtear le haghaidh CÉIM-chomhad ná .stp agus .step.

## Stair Bunúsach

In 1994, the original Part 21 specification was issued. It has some bugs which were corrected by the technical corrigendum issued in 1996. Foilsíodh an dara heagrán in 2002 a chuimsigh an ceartúchán agus síntí le haghaidh roinnt ranna sonraí. Foilsíodh an tríú eagrán in 2016 a chuir ancaire agus ailt tagartha leis a cheadaigh aonáin agus luachanna a stóráil i gcomhaid sheachtracha. Cuireadh teaghráin leis an tacaíocht UTF-8. Cuireadh sínithe digiteacha leis chun inneachar an chomhaid a fhíorú agus chun dintiúir a bhailíochtú. Cuireadh leis an tacaíocht chun an struchtúr malartaithe a chomhbhrú agus a stóráil ag baint úsáide as ZIP freisin.

## Formáid Comhaid STEP

The plain text format for a STEP-file consists of a sequence of records. The character set is defined as code points of ISO 10646. msgstr ISO-10303-21; iad na chéad charachtair sa chéad taifead. Tá carachtair /* agus */ timpeall ar nótaí tráchta. Tá END-ISO-10303-21; sa taifead deireanach má tá an comhad CÉIM ag teacht le leagan 2002. I gcás go gcloíonn sé le leagan 2016, d'fhéadfadh síniú digiteach amháin nó níos mó a bheith ann tar éis an END-ISO-10303-21; Críochnaitheoir. Cuirtear sosanna líne in iúl le \N\ agus cuirtear \F\ in iúl do bhriseadh leathanaigh.

Tá an comhad CÉIM roinnte ina rannóga agus is téarmaí forchoimeádta a n-ainmneacha. Críochnaíonn gach cuid leis an taifead ENDSEC agus caithfidh sé a bheith san ord a thaispeántar thíos.

- **HEADER**: Is roinn éigeantach í seo nach féidir athrá a dhéanamh. Tá sé comhdhéanta de na heintitis seo a leanas:
  - file_description (mandatory)
  - "ainm_comhad (éigeantach)"
  - "file_schema (éigeantach)"
  - "schema_population (roghnach)"
  - "comhad_daonra (roghnach)"
  - "roinn_teanga (roghnach)"
  - "alt_comhthéacs (roghnach)"
- **ANCHOR**: Is rannán roghnach neamh-athdhéanta í a tugadh isteach i leagan 2016. Sainmhíníonn sé na hainmneacha seachtracha le haghaidh cásanna ionas gur féidir tagairt a dhéanamh dóibh.
- **TAGAIRT**: Is roinn roghnach neamh-athdhéanta í a tugadh isteach freisin i leagan 2016. Comhcheanglaíonn gach iontráil sa chuid seo ainm shampla iontrála/luacha le háis/luach i gcomhad seachtrach.
- **SONRAÍ**: Is roinn roghnach í atá in-athdhéanta ina bhfuil bunábhar an tsampla.
- **SIGNATURE**: It is an optional repeatable section that was introduced in the 2016 version. It holds the digital signature to verify the file's content or to validate credentials.

## Tagairtí

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

