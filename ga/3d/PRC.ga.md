---
date: 2019-10-11
keywords: prc, .prc, prc file format, how to open prc files, .prc extension, prc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PFoirm Comhad RCat
linktitle: PRC
description: Ltuilleamh faoi fhormáid comhaid PRC agus APIs ar féidir leo comhad PRC a chruthú agus a oscailts.
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Formáidí comhaid PRC
Tá na síntí .prc á n-úsáid le haghaidh Dlúth formáid 3D Léirithe Táirge agus formáid comhaid r-leabhar ag MobiPocket.

## Cad is comhad Comhdhlúite Léiriúcháin Táirge (PRC) ann?

Is formáid comhaid 3D é PRC (Dlúth Léiriúcháin Táirge) atá optamaithe chun sonraí 3D a stóráil, a luchtú agus a thaispeáint go háirithe ag teacht ó chórais CAD (Dearadh Ríomhchuidithe). Is comhad dénártha seicheamhach é, scríofa ar bhealach iniompartha. Is féidir PRC a úsáid chun sonraí 3D a leabú i gcomhad PDF. Tacaíonn PRC leis an gcuid is mó de phríomhphíopaí CAD, mar shampla cóimeálacha agus páirteanna, crainn aonáin 3D, léiriú cruinn céimseata, léiriú triantánach, agus marcáil. Úsáideann PRC an síneadh .prc agus is é an cineál meán idirlín a úsáidtear ná *model/prc*.

Is formáid comhaid ilchuspóireach é PRC ar féidir é a stóráil bunaithe ar a úsáid trí úsáid a bhaint as comhbhrú rialta chun sonraí CAD a léiriú go díreach nó is féidir é a stóráil le comhbhrú ard chun méid an chomhaid a laghdú. Tá na sonraí 3D atá stóráilte i bhformáid PDF ag baint úsáide as formáid PRC idir-inoibritheach le feidhmchláir CAM agus CAE.

### Sonraíocht i bhFormáid Chomhaid Dhlúth Léiriúcháin Táirge (PRC).

Tá príomhroinn ceanntásca amháin i gcomhad PRC agus struchtúr comhaid amháin nó níos mó ina dhiaidh sin agus comhad samhail amháin ag an deireadh. Tá ceanntásc amháin ag struchtúr comhaid agus na ranna sonraí seo a leanas ina dhiaidh:

- **Globals**: Tá na struchtúir comhad tagartha agus dathanna, stíleanna líne, agus córais chomhordanáidí do gach aonán crann den struchtúr comhaid.
- **Tree**: It contains a description of the tree of items like product occurrences, part definitions, representation items, and markup.
- **Teisiliúchán**: Tá na sonraí teisilithe (triantánacha) go léir in aonáin dhuilleacha an chrainn (míreanna léirithe agus marcálacha).
- **Céimseata**: Tá na sonraí cruinn ar chéimseata agus topology maidir le haonáin dhuilleacha an chrainn (míreanna léirithe).
- **Céimseata breise**: Tá sonraí achoimre na céimseata ann. Ligeann sé seo an comhad a luchtú go páirteach gan an geoiméadracht iomlán a luchtú.

Seo a leanas struchtúr gnáthchomhaid PRC.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Cad é comhad r-leabhar MobiPocket le síneadh PRC
Tá formáid comhaid ríomhleabhair á tabhairt isteach ag cuideachta Fhrancach ar a dtugtar **Mobipocket** ag baint úsáide as an síneadh .prc. Ar dtús, sheol an Mobipocket feidhmchlár saor in aisce ar ilfheistí cliste mar, ríomhairí pearsanta táibléid, PDAs agus fóin chliste. Is ionann an síneadh .prc agus .mobi i ndáiríre ach úsáidtear é go háirithe le haghaidh PDAanna nach dtacaíonn ach le síntí **.prc** nó **.pdb**.

### Sonraíochtaí formáid comhaid Mobipocket PRC
Tá formáid comhaid MobiPocket PRC bunaithe ar an gcaighdeán Open eBook ag baint úsáide as XHTML agus is féidir JavaScript agus frámaí a áireamh leis. Tá tacaíocht ar fáil freisin do cheisteanna dúchais SQL le húsáid le bunachair shonraí leabaithe.

Tá leabharlann leathanach baile ag an Mobipocket Reader. Is féidir le léitheoirí leathanaigh bhána a chur isteach in aon chuid de leabhar agus líníochtaí inathraithe a chur leis. Is féidir na rudaí ar nós Anótálacha, leabharmharcanna, ceartúcháin, nótaí, agus líníochtaí a láimhseáil ó áit amháin. Tiontaítear íomhánna go formáid GIF agus tá uasmhéid 64K acu atá leordhóthanach le haghaidh fóin phóca le scáileáin bheaga. Tá na leabharmharcanna leictreonacha ag Mobipocket Reader, agus foclóir ionsuite.

Tá modh lánscáileáin ag an léitheoir le haghaidh léitheoireachta agus tacaíocht a thabhairt do go leor PDAanna, Cumarsáideoirí agus Fóin Chliste. Tacaíonn na táirgí Mobipocket le formhór na gcóras oibriúcháin Palm, Windows, Symbian, sméar dubh, ach ní le Android. Oibríonn an léitheoir faoi Linux nó Mac OS X ag baint úsáide as WINE.

## Tagairtí

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Comparison of e-book formats - By Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

