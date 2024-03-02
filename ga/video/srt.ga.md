---
date: 2019-10-11
keywords: srt, .srt, srt file format, .srt file format, .srt extension, srt extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Ltuilleamh faoi fhormáid comhaid SRT agus APIs ar féidir leo comhad SRT a chruthú agus a oscailts.
title: SFoirm Chomhaid RTat
linktitle: SRT
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Cad is comhad SRT ann? ##

Is comhad fotheideal simplí é SRT (formáid comhaid SubRip) a shábháiltear i bhformáid comhaid SubRip leis an síneadh .srt. Tá líon seicheamhach fotheidil ann, stampaí ama tosaigh agus deiridh, agus téacs fotheideal. Fágann comhaid SRT gur féidir fotheidil a chur le hábhar físeáin tar éis é a tháirgeadh.

## Struchtúr an chomhaid SRT ##

Tá ceithre chuid ag gach fotheideal sa chomhad SRT.

1. Áiritheoir uimhriúil a léiríonn uimhir nó suíomh an fhotheidil.
1. Am tosaithe agus deiridh an fhotheideal scartha le --> carachtair
1. Téacs fotheideal i líne amháin nó níos mó.
1. Líne bhán a léiríonn deireadh an fhotheideal.

### Sampla de SRT ###

```
1
00:05:00,400 --> 00:05:15,300
This is an example of
a subtitle.

2
00:05:16,400 --> 00:05:25,300
This is an example of
a subtitle - 2nd subtitle.
```

Chun an t-am a shonrú *uaireanta:nóiméid:soicindí,milleasoicindí (00:00:00,000)* úsáidtear formáid.

## Formáidiú na gcomhad SRT ##

Díorthaítear formáidiú comhaid SRT ó chlibeanna HTML. Tá na clibeanna formáidithe don chomhad SRT liostaithe thíos.

| Éifeacht | Clibeanna |
| --- | --- |
|Trom|**\ <b>...\</b> ** nó {b}...{/b}|
|Iodálach|**\ <i>...\</i> ** nó **{i}...{/i}**|
|Folíne|**\ <u>...\</u> ** nó **{u}...{/u}**|
|Dath Cló|**\ <font color=white>...\</font> **|
|Suíomh Líne|**{\a3}** (le fios gur cheart go dtosódh an téacs ar líne 3)

## Bogearraí SubRip ##

Is clár bogearraí saor in aisce é SubRip a ritheann ar Windows. Sleachta sé fotheidil agus a n-amanna ó bhformáidí éagsúla físeáin agus sábhálann sé na fotheidil i bhformáid SRT. Úsáideann SubRip aitheantas optúil carachtar chun fotheidil a bhaint as físeáin bheo, comhaid físe eile, agus DVDanna.

## Tagairtí ##

- [SRT - Wikipedia](https://en.wikipedia.org/wiki/SubRip)
