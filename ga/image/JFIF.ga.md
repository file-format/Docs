---
date: 2020-08-12
keywords: jfif, .jfif, jfif file format, how to open jfif files, .jfif extension, jfif extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JComhad FIF - Cad is fil .jfife?
linktitle: JFIF
description: Ltuilleamh faoi fhormáid comhaid JFIF agus APIs ar féidir leo comhad JFIF a chruthú agus a oscailts.
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## Cad is comhad JFIF ann?

Is comhad formáide íomhá é JFIF (Formáid Idirmhalartaithe Comhad JPEG (JFIF)) a úsáideann an síneadh .jfif. Tógann JFIF breis agus JIF (Formáid Idirmhalartaithe JPEG) trí chastacht a laghdú agus a theorainneacha a réiteach.

## Stair ghearr JFIF

JFIF document development was led by Eric Hamilton and an agreement on the first version was established in late 1991. Foilsíodh leagan 1.02 ar 7 Meán Fómhair, 1992. Sonraíodh RFC 2046 go n-úsáidtear an fhormáid JFIF chun íomhánna JPEG a tharchur thar an idirlíon. D’fhoilsigh ECMA JFIF in 2009 agus rinne ITU-T é a chaighdeánú in 2011 mar Mholadh T.871 agus ag ISO/IEC in 2013 mar ISO/IEC 10918-5

## Formáid Chomhaid JFIF ##

Is éard atá i gcomhad JFIF ná seicheamh marcóirí mar atá sainmhínithe i gcuid 1 den Chaighdeán JPEG. Tá dhá bheart i ngach marcóir (FF agus beart ina dhiaidh sin a shonraíonn an cineál marcóra). Is féidir le marcóirí a bheith neamhspleách nó tús le teascán marcóra a chur in iúl.

Ligeann JFIF do ilchodanna cosúil le Y, Cb, Cr, réitigh dhifriúla a bheith acu ach níl a n-ailíniú sainithe. Murab ionann agus JPEG, is féidir le JFIF faisnéis réitigh agus cóimheasa gné a sholáthar. Sainmhíníonn JFIF freisin an tsamhail datha atá le húsáid.

### Struchtúr Comhaid ##

|Deighleog|Cód|Cur Síos|
|---|---|---|
|SOI|FF D8|Tosaigh na hÍomhá|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|deighleoga marcála breise |
|SOS|FF DA|Tosú an Scan|
||sonraí íomhá comhbhrúite||
|EOI|FF D9|Deireadh na hÍomhá|

Sainmhíníonn Caighdeán JFIF na codanna seo a leanas:

### Deighleog marcála JFIF APP0 ###

Is teascán éigeantach é ina bhfuil paraiméadair íomhá. Féadfaidh mionsamhail neamh-chomhbhrúite leabaithe a bheith ann freisin.

|Réimse|Méid (bearta)|Cur Síos|
|---|---|---|
|Marcóir APP0|2|FF E0|
|Fad|2|Fad na míre gan marcóir APP0 a áireamh |
|Aitheantóir|5|JFIF (4A 46 49 46 00) in ASCII arna fhoirceannadh le beart nialasach |
|Leagan JFIF|2|Leagan den JFIF|
|Aonaid dlúis|1|Aonad do na réimsí dlús picteilín seo a leanas</br> 00 : Gan aonad; leithead:airde tá cóimheas gné picteilín cothrom le Ydensity:Xdensity</br> 01 : picteilíní an orlach</br> 02 : picteilíní in aghaidh an ceintiméadar |
|Xdlús|2|Dlús cothrománach picteilín níos mó ná nialas|
|Comhdhlúthacht|2|Dlús picteilín ingearach níos mó ná nialas|
|Xthumbnail|1|Comhaireamh cothrománach picteilín den mhionsamhail RGB leabaithe. D'fhéadfadh a bheith nialas|
|Ythumbnail|1|Comhaireamh picteilín ingearach den mhionsamhail RGB leabaithe. D'fhéadfadh a bheith nialas|
|Sonraí mionsamhla|3 × n|Sonraí mionsamhlacha raster RGB 24 giotán neamh-chomhbhrúite|

### Mírín marcála síneadh JFIF APP0 ###

Is roinn roghnach í seo nach mór, má shainítear í, mír mharcála JFIF APP0 a leanúint láithreach. Tá an chuid seo tacaithe ag JFIF leagan 1.02 agus os a chionn agus ceadaíonn sé mionsamhlacha a leabú i dtrí fhormáid éagsúla.

|Réimse|Méid (bearta)|Cur Síos|
|---|---|---|
|Marcóir APP0|2|FF E0|
|Fad|2|Fad na míre gan marcóir APP0 a áireamh |
|Aitheantóir|5|JFXX (4A 46 58 58 00) in ASCII arna fhoirceannadh le beart nialasach |
|Formáid mionsamhlacha|1|Sonraíonn sé cén fhormáid sonraí a úsáidtear don mhionsamhail leabaithe seo a leanas:</br> 10 : Formáid JPEG</br> 11 : 1 beart in aghaidh an fhormáid phailéadaithe picteilín</br> 13 : 3 beart in aghaidh an fhormáid RGB picteilín |
|Sonraí mionsamhlacha|athróg||

## Comhshó JFIF go Formáidí Comhaid Íomhá Eile

Is féidir JFIF a thiontú go formáidí comhaid íomhá móréilimh ar nós [PNG](/image/png/), [JPG](/image/jpeg/), agus [PDF](/pdf/).

## Tagairtí ##

- [JFIF - Wikipedia](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)

