---
date: 2019-10-11
keywords: WEBM, What is a WEBM file, WEBM File Format
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Ltuilleamh faoi fhormáid comhaid WEBM agus APIs ar féidir leo comhad WEBM a chruthú agus a oscailts.
title: WEBM - WebM Foirm Chomhaid Físeat
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Cad is comhad WEBM ann?

Is comhad físe é comhad a bhfuil síneadh .webm aige bunaithe ar fhormáid an chomhaid WebM oscailte, saor ó ríchíosa. Tá sé deartha chun físeáin a roinnt ar an ngréasán agus sainmhíníonn sé struchtúr an choimeádáin comhaid lena n-áirítear formáidí físe agus fuaime. Tá WebM 100% saor in aisce, ag cur i bhfeidhm ardchaighdeáin bunaithe ar theicneolaíochtaí oscailte mar HTML, HTTP, agus TCP/IP atá oscailte do dhuine ar bith lena gcur i bhfeidhm. Tá WebM deartha go sonrach chun físeáin a sheirbheáil ar an ngréasán, rud a fhágann go bhfuil sé optamaithe le haghaidh sruthú le lorg ríomhaireachtúil íseal. Mar sin, tá sé oiriúnach d'athsheinm físeáin ar aon fheiste, go háirithe ríomhairí glúine ísealchumhachta, ríomhairí boise agus táibléad.

## Formáid Chomhaid WEBM

Tá struchtúr comhaid WebM bunaithe ar fho-thacar d'fhormáid chomhaid coimeádáin Matroska [MKV](/video/mkv/). Déantar na sruthanna físeáin atá ar fáil i gcomhad WebM a chomhbhrú ag baint úsáide as na teicneolaíochtaí comhbhrú VP8 nó VP9 atá an-éifeachtach ó thaobh comhbhrú. Mar an gcéanna, déantar na sruthanna fuaime i gcomhad WebM a chomhbhrú trí úsáid a bhaint as na codecs Vorbis nó Opus a d'fhorbair [Xiph Foundation](https://www.xiph.org/). Tá na físeáin agus na codecs fuaime seo go léir saor ó ríchíosanna agus is féidir iad a úsáid gan aon táille.

Seo a leanas na sonraíochtaí achoimre maidir le formáid comhaid WebM.

| Réimse | Cur síos |
---|---|
|Cineál MIME |físeán/gréasán|
|Cineál MIME fuaime amháin | fuaime/webm|
|Aitheantóir Cineál Éide| org.webmproject.webm|
|Ainm an Codec Físeáin| VP8 nó VP9|
|Ainm an Codec Fuaime| Vorbis nó Opus|

### Eilimintí WebM

WebM, being a subset of the Matroska specifications, provides support for some of the Matroska functionality. Following is a description of the supported elements.

#### EBML

|Ainm |Cur síos|
---|---|
|EBML|Socraigh tréithe EBML na sonraí atá le leanúint. Caithfidh gach doiciméad EBML tosú leis seo.|
|EBMLVersion |An leagan den pharsálaí EBML a úsáideadh chun an comhad a chruthú.|
|EBMLReadVersion|An leagan íosta EBML a chaithfidh parsálaí a thacú chun an comhad seo a léamh.|
|EBMLMaxIDLength |Uasfhad na n-aitheantas a gheobhaidh tú sa chomhad seo (4 nó níos lú i Matroska).|
|EBMLMaxSizeLength|Uasfhad na méideanna a gheobhaidh tú sa chomhad seo (8 nó níos lú i Matroska). Ní sháraíonn sé seo méid na heiliminte a léirítear ag tús eiliminte. Measfar eilimintí a bhfuil méid sonraithe acu atá níos mó ná an méid a cheadaítear le EBMLMaxSizeLength neamhbhailí.
|Type|Teaghrán a chuireann síos ar an gcineál doiciméid a leanann an ceanntásc EBML seo (webm inár gcás).|
|DocTypeVersion|An leagan den ateangaire DocType a úsáideadh chun an comhad a chruthú.|
|DocTypeReadVersion|An leagan DocType íosta a chaithfidh ateangaire a thacú chun an comhad seo a léamh.|

#### Eilimintí Domhanda

I láthair na huaire, ní thacaítear ach leis an eilimint `Folamh` a úsáidtear chun sonraí damáiste a chur ar neamhní, chun iompar gan choinne a sheachaint agus sonraí damáiste á n-úsáid. Cuirtear an t-ábhar i leataobh. Úsáidtear é freisin chun spás a chur in áirithe i bhfo-eilimint le húsáid níos déanaí.

#### Deighleog
Tá gach eilimint eile barrleibhéil (leibhéal 1) san eilimint seo. Go hiondúil bíonn comhad Matroska comhdhéanta de mhír 1.

#### Meta Lorg Faisnéise

Tugtar tacaíocht dóibh seo a leanas atá ag lorg faisnéise.

|Ainm na hEilime |Cur síos|
---|---|
|SeekHead |Tá suíomh eilimint eile leibhéal 1 ann.|
|Iarracht |Tá iontráil aoniarrachta ar eilimint EBML ann.|
|SeekID|An Aitheantas Dénártha a fhreagraíonn d'ainm na heiliminte.|
|SeekPosition |Suíomh na heile sa teascán in octets (0 = eilimint chéad leibhéal 1). ||

## Tagairtí

* [WebM](https://www.webmproject.org/)

* [Stórtha Cód WebM](https://www.webmproject.org/code/#webp-repositories)


