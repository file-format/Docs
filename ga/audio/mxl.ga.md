---
date: 2022-03-20
keywords: mxl, Musepack file format, .mxl extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
description: Ltuilleamh faoi fhormáid comhaid MXL agus APIs ar féidir leo comhad MXL a chruthú agus a oscailts.
title: MFormáid Comhaid XL - Ceol ComhbhrúiteXML File
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Cad is comhad MXL ann?

Is éard atá i gcomhad MXL an fhoirm chomhbhrúite d’fhormáid comhaid MusicXML atá ina fhormáid chaighdeánach oscailte chun bileoga ceoil dhigitigh a mhalartú. Gnáth-théacs Tá comhaid MusicXML mór i méid agus cuireadh isteach ar úsáid comhaid den sórt sin mar fhormáid dáileacháin leatháin leis an méid mór comhaid. Déileáladh leis an bhfadhb seo le [MusicXML](https://www.musicxml.com/) 2.0 trí fhormáid comhaid MXL a thabhairt isteach a chomhbhrúíonn na comhaid go leor chun méid comhaid a laghdú cosúil leis an mbunchomhaid MIDI. Is é an cineál meán molta do chomhaid MXL ná application/vnd.recordare.musicxml.

## Formáid Chomhaid MXL

Stóráiltear comhaid MXL mar chomhaid [ZIP](/compression/zip/) chomhbhrúite {{ HYPERLINK2}} le hiarmhír chomhaid .mxl. Comhbhrúitear comhaid MXL leis an algartam DEFLATE mar atá sonraithe san [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### Struchtúr Comhad MXL

Tá formáid XML ZIP-bhunaithe ag gach comhad MXL a chaithfidh comhad META-INF/container.xml a bheith ann a chuireann síos ar phointe tosaigh leagan MusicXML den chomhad. Níl aon chomhad .xsd comhfhreagrach sainithe don fhormáid comhaid MXL.

Seo a leanas an t-ábhar atá i gcomhad coimeádán.xml simplí. Tógtar an sampla seo ó chomhad Dichterliebe01.mxl atá ar fáil ar shuíomh Gréasáin MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Sa sampla seo, tá an<container> eilimint an doiciméid. Tá an<rootfiles> is féidir eilimint amháin nó níos mó a bheith ann<rootfile> eilimintí, leis an gcéad<rootfile> eilimint a chuireann síos ar fhréamh MusicXML. Comhad MusicXML a úsáidtear mar a<rootfile> D'fhéadfadh a bheith<score-partwise> ,<score-timewise> , nó<opus> mar eilimint doiciméad.

## Tagairtí

* [Comhaid MXL comhbhrúite]( https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)

* [RFC 1951]( https://www.ietf.org/rfc/rfc1951.txt)


