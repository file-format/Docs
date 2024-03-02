---
date: 2019-12-09
keywords: arj, .arj, arj file format, how to open arj files, .arj extension, arj extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: AFoirm RJ Comhadat
linktitle: ARJ
description: Ltuilleamh faoi fhormáid comhaid ARJ agus APIs ar féidir leo comhad ARJ a chruthú agus a oscailts.
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Cad is comhad ARJ ann? ##

Is comhad cartlainne comhbhrúite ardéifeachtúlachta é ARJ (Cartlannaithe ag Robert Jung) arna fhorbairt ag Robert K. Jung. Forbraíodh ARJ le haghaidh DOS agus leaganacha luatha de Windows go luath sna 1990idí. Tá comhaid ARJ úsáideach chun líon mór comhad a thacú nó a roinnt mar ní gá duit súil a choinneáil ar na comhaid sin go léir agus níl ach comhad amháin le láimhseáil. Úsáidtear an síneadh .arj do na comhaid cartlainne ARJ.

## Formáid Chomhaid ARJ ##

Tá dhá chineál ceanntásca i gcomhad ARJ:

- Príomhcheannteideal: Tá príomhcheanntásc amháin ag tús na cartlainne.
- Ceanntásca áitiúla: Tá ceanntásca áitiúla i láthair roimh gach comhad.

|Fritháireamh|Cineál|Cuntas|Cur Síos|
|---|---|---|---|
|0000h|focal|1|ID=0EA60h|
|0002h|focal|1|bunmhéid ceanntásca|
|0004h|beart|1|Méid an cheanntásca |
|0005h|beart|1|Uimhir leagain an chartlainne|
|0006h|beart|1|Uimhir leagain íosta ag teastáil|
|0007h|beart|1|Óstaigh OS:</br> 0 - MS-DOS</br> 1 - PRIMOS</br> 2 - UNIX</br> 3 - AMIGA</br> 4 - MAC-OS (Córas xx)</br> 5 - OS/2</br> 6 - Úll GS</br> 7 - ATARI ST</br> 8 - Ar Aghaidh</br> 9 - VAX VMS|
|0008h|beart|1|Bratacha Inmheánacha, giotánmapped:</br> 0 - gan focal faire / pasfhocal</br> 1 - in áirithe</br> 2 - leanann an comhad ar an gcéad diosca eile</br> 3 - Tá réimse comhad tús seasamh ar fáil</br> 4 - aistriúchán conair ( \ go / )|
|0009h|beart|1|Modh comhbhrúite:</br> 0 - stóráilte</br> 1 - comhbhrúite an chuid is mó</br> 2 - comhbhrúite</br> 3 - comhbhrúite níos tapúla</br> 4 - comhbhrúite is tapúla |
|000Ah|beart|1|Cineál comhaid:</br> 0 - dénártha</br> Téacs 1 - 7-giotán</br> 2 - ceanntásc tráchta</br> 3 - eolaire</br> 4 - lipéad toirte |
|000Bh|beart|1|curtha in áirithe|
|000Ch|dword|1|Dáta/Am an bhunchomhaid i bhformáid MS-DOS|
|0010h|dword|1|Méid an chomhaid chomhbhrúite|
|0014h|dword|1|Méid an bhunchomhaid |
|0018h|dword|1|CRC-32 den bhunchomhad|
|001Ah|focal|1|Suíomh sonra an chomhaid in ainm an chomhaid|
|001Ch|focal|1|Aitreabúidí comhaid|
|001Eh|focal|1|Sonraí óstaigh|
|?|dword|1|Ionad tosaithe an chomhaid leathnaithe|
|????h|dword|1|CRC-32 den bhuncheannteideal|
|????h|focal|1|Méid an chéad cheannteidil sínte|
|????h+SIZ+2|dword|1|CRC-32 den cheannteideal sínte |
|????h+SIZ+6|beart|?|Comhad comhbhrúite|

## Tagairtí ##

- [ARJ - Wikipedia](https://en.wikipedia.org/wiki/ARJ)

