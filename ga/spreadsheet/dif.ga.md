{
  "date": "2019-12-10",
  "keywords": [
"DIF",
"comhad",
"síneadh",
"formáid comhaid",
"Comhad Idirmhalartaithe Sonraí",
"Scarbhileog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Do threoir formáid comhaid le fios a bheith agat cad is síneadh comhaid DIF agus APIs ann ar féidir comhaid DIF a chruthú agus a oscailt.",
  "title": "DIF - Formáid Chomhaid Idirmhalartaithe Sonraí",
  "linktitle": "DIF",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-di-gaf"
}
},
  "lastmod": "2019-12-10"
}

## Cad is comhad DIF ann?

Seasann DIF do Formáid Idirmhalartaithe Sonraí a úsáidtear chun sonraí scarbhileoga a allmhairiú/onnmhairiú idir feidhmchláir éagsúla. Ina measc seo tá Microsoft Excel, OpenOffice Calc, StarCalc agus go leor eile. Stórálann sé sonraí atá i scarbhileog amháin agus is é sin an t-aon teorainn leis an bhformáid comhaid seo.

## Stair Achomair d'Fhormáid Chomhaid DIF ##

D'fhorbair Software Arts, Inc. formáid comhaid DIF go luath sna 1980idí. Áiríodh na sonraíochtaí formáid comhaid do DIF i VisiCalc, an chéad scarbhileog do ríomhairí pearsanta. Bhí cóipcheart ar na sonraíochtaí seo i 1981 agus ba thrádmharc cláraithe iad de chuid Software Arts Products Corp.

## Formáid Chomhaid DIF ##

Stóráil DIF inneachar scarbhileog i gcomhad téacs ASCII a cheadaíonn é a fheiceáil agus a chur in eagar le heagarthóir téacs. Is leis an bhformáid a áit i liosta formáidí sraitheachú sonraí dá saintréithe idirmhalartaithe sonraí. Tá 2 chuid i gcomhad DIF; ceanntásc agus sonraí.

Léirítear gach rud i DIF le smután 2 nó 3-líne. Faigheann ceanntásca smután 3-líne; sonraí, 2 .

* Tosaíonn smután ceanntásca le haitheantóir téacs arb ionann é agus gach caipín, gan ach carachtair aibítreacha, agus níos lú ná 32 litir. Ní mór péire uimhreacha a bheith sa líne seo a leanas, agus ní mór an tríú líne a bheith ina sreang luaite.

* Tosaíonn smután sonraí le péire uimhreacha agus is teaghrán luaite nó eochairfhocal an chéad líne eile.


### Luachanna ###

Tá dhá líne ag luach, péire uimhreacha sa chéad cheann agus téad nó eochairfhocal sa dara ceann. Léiríonn an chéad uimhir den phéire cineál:

* −1 – directive type, the second number is ignored, the following line is one of these keywords:
** BOT – tús an tuple (tús an ró)
** EOD – deireadh na sonraí
* 0 – numeric type, value is the second number, the following line is one of these keywords:
** V – bailí
** NA – níl sé ar fáil
** EARRÁID - earráid
** TRUE – fíorluach Boole
** BRÉAGACH – luach boolean bréagach
* 1 – cineál teaghrán, tá an dara uimhir neamhaird, is é an líne seo a leanas an teaghrán i Sleachta dúbailte


### Scuad Ceanntásca DIF ###

Cuimsíonn an smután ceanntásc de chomhad DIF líne aitheantóra agus dhá líne luacha ina dhiaidh. Ní úsáideann na luachanna uimhriúla i smután ceanntásca ach teaghrán folamh in ionad na heochairfhocail bailíochta. Seo a leanas sonraí na smután ceanntásca seo.

* TÁBLA - leanann luach uimhriúil den leagan, tá trácht gineadóra ar an dara líne as úsáid den luach

* VECTORS - seo a leanas líon na gcolún mar luach uimhriúil

* TUPLES - seo a leanas líon na sraitheanna mar luach uimhriúil

* SONRAÍ - tar éis luach uimhriúil 0 caochadán, leanann na sonraí don tábla, agus luach BOT roimh gach sraith, cuirtear luach EOD deireadh leis an tábla iomlán


### DIF Sampla ###

Léiríonn an sampla seo a leanas a bhfuil i mbileog oibre shimplí agus a léiriú DIF comhionann.


|Ainm|Aois
---|---|
|Bob|34
| Bileoga|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Tagairtí ##

* [DIF - Le Vicipéid]( https://ga.wikipedia.org/wiki/Data_Interchange_Format)


