---
date: 2019-10-11
keywords: json, .json, json file format, how to open json files, javascript object notation, json data format, .json file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFormáid Chomhaid SON - Cad is comhad JSON anne?
linktitle: JSON
description: Ltuilleamh faoi fhormáid comhaid JSON agus APIs ar féidir leo comhad JSON a chruthú agus a oscailts.
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Cad is comhad JSON ann?

Is formáid comhaid chaighdeánach oscailte é JSON (JavaScript Object Notation) chun sonraí a chomhroinnt a úsáideann téacs atá inléite ag an duine chun sonraí a stóráil agus a tharchur. Stóráiltear comhaid JSON leis an iarmhír .json. Tá níos lú formáidithe ag teastáil ó JSON agus is rogha eile maith é do [XML](/web/xml/). Díorthaítear JSON ó JavaScript ach is formáid sonraí teanga-neamhspleách é. Tacaíonn go leor teangacha ríomhchlárúcháin le giniúint agus le parsáil JSON. Is é *app/json* an cineál meán a úsáidtear le haghaidh JSON.

## Formáid Chomhaid JSON - Stair Ghearr

There was a need for real-time server to client communication that lead to the creation of JSON. The JSON format was first specified by Douglas Crockford in March 2001. Bhí JSON bunaithe ar Chaighdeán ECMA-262 3ú Eagrán - Nollaig 1999 atá ina fho-thacar de JavaScript.

The first edition of JSON standard ECMA-404 was published in October 2013 by Ecma International. RFC 7159 became the main reference for JSON's Internet uses in 2014. I mí na Samhna 2017, foilsíodh ISO/IEC 21778:2017 mar chaighdeán idirnáisiúnta. Foilsíodh RFC 8259 an 13 Nollaig 2017 ag The Internet Engineering Task Force arb é an leagan reatha den Internet Standard STD 90 é.

## Struchtúr Comhad JSON

Tá sonraí JSON scríofa i bpéirí **eochair/luach**. Tá idirstad(:) idir an eochair agus an luach sa lár agus an eochair ar chlé agus an luach ar dheis. Tá péirí eochracha/luacha difriúla scartha le camóg(,). Is é an eochair ná teaghrán timpeallaithe ag comharthaí athfhriotail dúbailte mar shampla ainm. Is féidir na luachanna a bheith de na cineálacha seo a leanas.

- `Uimhir`
- `Teaghrán`: Seicheamh carachtair Unicode timpeallaithe ag comharthaí athfhriotail dúbailte.
- `Boolean`: Fíor nó Bréagach.
- `Eagar`: Liosta luachanna timpeallaithe ag lúibíní cearnacha, mar shampla

``` json
[ Apple, Banana, Oráiste ]
```

- `Réad`: Cnuasach de phéirí eochair/luacha timpeallaithe ag braces chatach, mar shampla

``` json
{ name : Jack, aois: 30, is fearr leat : Peil}
```

Is féidir réada JSON a neadú freisin chun struchtúr na sonraí a léiriú. Anseo thíos tá sampla de réad JSON.

### Sampla Formáid JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Cad é uasmhéid an chomhaid JSON?

Níl beagnach aon teorainn le huasmhéid comhaid JSON. Is féidir é a bheith chomh fada leis an spás a theastaíonn ón ábhar a stóráil.

Nuair a bhaineann sé le formáid comhaid JSON a úsáid chun sonraí a aistriú thar an idirlíon, ní mór a bheith cúramach faoi na hacmhainní ríomhaireachta atá ar fáil. Má aistrítear sonraí móra JSON, cuirfear isteach ar an aistriú má tá cuimhne theoranta ag brabhsálaí an chliaint.


Níl aon teorainn chrua sainithe ag sonraíocht, ach ní mór duit a bheith cúramach gan acmhainní a sceite ar do ríomhairí úsáideoirí, toisc go ndéanfaidh sé a n-eispéireas úsáideora a dhíghrádú go tapa, agus is dócha go ndéanfaidh siad d'app a thréigean.

## JSON vs XML

Is formáid comhaid choitianta eile é **XML** chun sonraí a mhalartú ar an idirlíon. Nuair a thagann sé chun sonraí a mhalartú idir feidhmchláir, tá rogha ag forbróirí formáidí comhaid XML agus JSON araon a úsáid. Glactar le JSON, áfach, mar an bealach is áisiúla chun sonraí a mhalartú idir feidhmchláir ar an idirlíon mar gheall ar na cúiseanna seo a leanas.

 1. Tugann JSON léargas soiléir agus níos éasca le léamh ar shonraí i gcomparáid le formáidí comhaid XML
 1. Laghdaíonn JSON forchostas an aistrithe sonraí thar an idirlíon toisc go bhfuil níos lú carachtar aige chun an tacar céanna sonraí a shainiú agus a dhéantar le XML
 1. Soláthraíonn teangacha ríomhchlárúcháin nua-aimseartha parsálaithe ionsuite chun freagra JSON a pharsáil ar an ngréasán.

## CCanna

 * **Cad chuige a n-úsáidtear comhad JSON?** Is féidir formáid comhaid JSON a úsáid mar fhormáid comhaid idirmheánach chun sonraí a ghintear a stóráil, mar shampla ó fhoirm a chuirtear isteach ar shuíomh Gréasáin. Úsáidtear é freisin mar chomhad formáid sonraí d’aon teanga ríomhchlárúcháin agus soláthraíonn sé idir-inoibritheacht idir cineálacha éagsúla sonraí.
 * **An ionann comhad JSON agus XML?** Ní hea i ndáiríre. Tá difríocht idir JSON agus XML sa mhéid is go bhfuil JSON níos giorra, gur féidir é a léamh agus i gceart go tapa, in ann eagair a úsáid agus ní úsáideann sé clib deiridh.
 * **Can I convert JSON to CSV?** Yes, there are certain online converter apps such as **GroupDocs Conversion apps** that can [convert JSON to CSV](https://products.groupdocs.app/conversion/json-to-csv).
 * **Conas JSON a Thiontú go PDF?** Is féidir leat aipeanna ar líne a úsáid mar Asopse.app for Cells chun [comhad JSON a thiontú go PDF](https://products.aspose.app/cells/conversion/json-to-pdf).
 * **Conas comhad JSON a oscailt i Word?** Is féidir leat aipeanna ar líne a úsáid mar Aspose.app for Words chun comhad JSON a thiontú go Word.

## An raibh a fhios agat?

You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about JSON or Web file formats, you can post your findings in [Web File Format News](https://news.fileformat.com/t/Web) section for people to learn more form these.

## Tagairtí

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [An Introduction to JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

