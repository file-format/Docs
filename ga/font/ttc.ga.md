{
  "date": "2021-02-25",
  "keywords": [
"comhad ttc",
"formáid comhaid ttc",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "TTC - Formáid Chomhaid Bhailithe TrueType",
  "description": "Comhcheanglaíonn comhad TrueType Collection (TTC) go leor clónna in aon chomhad amháin. Bhain Apple agus Microsoft úsáid as TTF ar chórais oibriúcháin Mac agus Windows.",
  "linktitle": "TTC",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-gac"
}
},
  "lastmod": "2021-02-25"
}

## Cad is comhad TTC ann?
Déantar an TTC a ghiorrú mar gur síneadh ar fhormáid TrueType Collection é TrueType Collection. Is féidir le comhad TTC na comhaid chló iolracha a chomhcheangal ann. Tá na comhaid seo tairbheach chun clónna iolracha a chomhcheangal a roinneann go leor glyphs i bpáirt. Roimh Windows 2000, baineadh úsáid as na comhaid TTC i leaganacha Sínise, Seapánacha agus Cóiréis d'fhuinneoga ach níos déanaí bhí an tacaíocht ar fáil do gach réigiún.


## Struchtúr an Chomhaid Bhailithe Cló 
Tá comhad TTC comhdhéanta de thábla Ceanntásca TTC, Comhadlanna Tábla, agus táblaí iolracha OpenType. Ní mór an Ceanntásc TTC a fháil ag tús an chomhaid. Ní mór eolaire tábla iomlán a bheith ann do gach cló. Ba cheart go mbeadh formáid an TableDirectory cosúil leis an bhformáid a bhí i gcomhad neamhbhailiúcháin. Ríomhtar an comhaireamh tábla i ngach eolaire laistigh de chomhad TTC ó thús comhad TTC.
Déantar tagairt do na táblaí i gcomhad TTC tríd an eolaire tábla dá gcuid clónna faoi seach. Caithfidh roinnt táblaí OpenType a bheith le feiceáil go minic, uair amháin in aghaidh gach cló a chuirtear leis an TTC. De bharr an méid is féidir na táblaí eile a roinnt le clónna iolracha sa chomhad TTC.

### Ceanntásc TTC
Tá dhá leagan den tábla Ceanntásc TTC ar fáil go dtí seo:
- Úsáidtear Leagan 1.0 le haghaidh comhaid TTC gan sínithe digiteacha.
- Is féidir Leagan 2.0 a úsáid le haghaidh comhaid TTC le sínithe digiteacha nó gan síniú digiteach.
Seo na táblaí Ceanntásc TTC den dá leagan:

**TTC Header Leagan 1.0:**

|Cineál|Ainm|Cur Síos|
---|---|---|
|TAG|ttcTag|Teaghrán aitheantais Bailiúchán Cló: 'ttcf' (a úsáidtear le haghaidh clónna a bhfuil imlíne CFF nó CFF2 orthu chomh maith le breac-chuntas TrueType)|
|uint16|leagan mór|Mórleagan den Cheanntásc TTC, = 1. ||
|uint16|mionleagan|Mionleagan den Cheanntásc TTC, = 0. ||
|uint32|numFonts|Líon na gclónna in TTC|
|Fritháireamh32|Socruithe Comhadlainne tábla[numFonts]|Eagar fritháirimh chuig an Eolaire Tábla do gach cló ó thús an chomhaid |

**TTC Header Leagan 2.0:**

|Cineál|Ainm|Cur Síos|
---|---|---|
|TAG|ttcTag|Teaghrán aitheantais Bailiúchán Cló: 'ttcf'|
|uint16| majorVersion |Mórleagan den Cheanntásc TTC, = 2.|
|uint16| minorVersion |Mionleagan den Cheanntásc TTC, = 0.|
|uint32| numFonts |Líon na gclónna in TTC|
|Fritháireamh32| tableDirectoryOffsets[numFonts] |Eagar fritháirimh chuig an Eolaire Tábla do gach cló ó thús an chomhaid|
|uint32| dsigTag |Clib a thugann le fios go bhfuil tábla DSIG ann, 0x44534947 ('DSIG') (níl mura bhfuil síniú ann)|
|uint32| dsigLength |Fad (i mbeart) an tábla DSIG (níl aon síniú)|
|uint32| dsigOffset |Fritháireamh (i mbeart) an tábla DSIG ó thús an chomhaid TTC (níl aon síniú)|

## Tagairtí
 * [An Comhad Cló OpenType]( https://learn.microsoft.com/en-us/typography/opentype/spec/otff)
 * [TrueType (Wikipedia)]( https://en.wikipedia.org/wiki/TrueType)

