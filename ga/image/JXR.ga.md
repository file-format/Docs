---
date: 2020-08-12
keywords: jxr, .jxr, jxr file format, how to open jxr files, .jxr extension, jxr extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFoirm XR Comhadat
linktitle: JXR
description: Ltuilleamh faoi fhormáid comhaid JXR agus APIs ar féidir leo comhad JXR a chruthú agus a oscailts.
menu:
  docs:
    parent: "image"
lastmod: 2021-19-01
---

## Cad is comhad JXR ann? ##

Is formáid comhaid é JPEG XR (raon leathnaithe JPEG) le haghaidh íomhánna grianghrafadóireachta ton leanúnach. Is caighdeán comhbhrú fós-íomhá é atá bunaithe ar HD Photo forbartha ag Microsoft. Tacaíonn sé le comhbhrú lossy agus lossless araon.

## Stair Ghearr ##

Windows Media Photo was first announced by Microsoft at WinHEC 2006. Athainmníodh HD Photo é i mí na Samhna 2006. Faomhadh JPEG XR mar Chaighdeán Idirnáisiúnta ISO/IEC 29199-2 ar 19 Meitheamh 2009. D'fhoilsigh an ITU-T agus ISO/IEC sonraíocht formáid tairiscinte (ITU-T T.833 | ISO/ IEC 29199-3), tacar tástála comhlíonta (ITU-T T.834 | ISO/IEC 29199-4), agus bogearraí tagartha (ITU-T T.835 | ISO/IEC 29199-5) le haghaidh JPEG XR tar éis iad a bheith críochnaithe den tsonraíocht códaithe íomhá in 2010. In 2011 foilsíodh tuarascáil theicniúil ag cur síos ar ailtireacht an tsreafa oibre do JPEG XR.

## Dearadh JPEG XR ##

I gcomparáid le JPEG, cuireann JPEG XR roinnt feabhsuithe lena n-áirítear:

- ** Comhbhrú Níos Fearr **: Tairgeann JPEG XR cóimheasa comhbhrú níos airde.
- ** Comhbhrú Gan Chaillteanas **: Tacaíonn JPEG XR le comhbhrú gan chailliúint.
- ** Struchtúr Tíleanna**: Is féidir íomhá JPEG XR a dheighilt ina réigiúin tíl inar féidir gach réigiún a dhíchódú ar leithligh.
- **Níos mó cruinnis datha**: Áirítear le JPEG XR tiontú inmheánach go spás datha YCoCg chun tacú le híomhánna ag baint úsáide as spás datha RGB. Tacaíonn JPEG XR freisin le samhail slánuimhir dath CMYK 16-giotán in aghaidh an chomhpháirt (64-giotán in aghaidh an picteilín). Tacaíonn JPEG XR le formáid dathanna snámhphointe comhroinnte easpónantóra RGBE le haghaidh íomhánna HDR. Tacaíonn JPEG XR le hionchóduithe datha liathscála agus ilchainéil freisin.
- **Léarscáil Trédhearcachta**: Tacaíonn JPEG XR leis an gcainéal alfa le haghaidh trédhearcachta.
- **Mionathrú íomhá fearainn chomhbhrúite**: Is féidir íomhánna JPEG XR a thiontú go ionchódú caillte, iad a laghdú i dtaifeach, bearrtha, iompaithe, rothlú, agus is féidir struchtúr na tíl a athrú go léir gan an comhad a dhíchódú go hiomlán.
- **Tacaíocht Meiteashonraí**: D’fhéadfadh próifíl datha ICC a bheith i gcomhad íomhá JPEG XR le haghaidh léiriú comhsheasmhach datha thar ilfheistí. Tacaíonn an fhormáid le formáidí meiteashonraí Exif agus XMP freisin.

## Formáid Coimeádán ##

Is féidir sonraí íomhá JPEG XR a stóráil i bhformáid coimeádán cosúil le TIFF trí úsáid a bhaint as tábla de chlibeanna Eolaire Comhad Íomhá (IFT). Tá na nithe seo a leanas i gcomhad JXR i gclibeanna IFD:

- Sonraí íomhá: Is sonraí íomhá féinchuimsitheacha tadhlach é.
- Sonraí roghnacha cainéal alfa: Má tá sé seo i láthair, is féidir na sonraí íomhá a chomhbhrú ar leithligh rud a chumasaíonn tacaíocht d'fheidhmchláir nach dtacaíonn le trédhearcacht.
- Meiteashonraí
- meiteashonraí roghnacha XMP
- meiteashonraí Roghnacha Exif

Toisc go bhfuil sé bunaithe ar fhormáid TIFF, faigheann sé gach ceann de na teorainneacha formáid TIFF cosúil leis an teorainn méid comhaid 4 GB.

## Tagairtí ##

- [JPEG XR - Wikipedia](https://en.wikipedia.org/wiki/JPEG_XR)

