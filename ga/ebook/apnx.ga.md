{
  "date": "2021-03-11",
  "keywords": [
"APNX",
"Innéacs Uimhir Leathanach Amazon",
"síneadh",
"comhad",
"formáid",
"ríomhleabhar",
"Amazon Kindle"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid Amazon APNX agus APIs ar féidir leo comhaid APNX a chruthú agus a oscailt.",
  "title": "APNX - Innéacs Uimhir Leathanach Amazon",
  "linktitle": "APNX",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-apn-gax"
}
},
  "lastmod": "2021-05-28"
}

## Cad is comhad APNX ann? ##

Is cineál comhaid ríomhleabhair é an comhad Innéacs Uimhir Leathanach Amazon a úsáideann an síneadh .apnx; in úsáid ag Amazon Kindle. Tugtar comhaid uimhriúcháin ar na comhaid seo a úsáideann gléasanna Kindle. Mar sin cruthaítear na comhaid APNX de ghnáth chun leathanaigh Kindle eBook a mharcáil. Cuireadh tús leis an ngné uimhriúcháin ar fheistí Amazon Kindle óna fhirmware 3.1. Féachann sé isteach sa chomhad APNX le haghaidh innéacsanna leathanaigh agus ansin mapálann sé é le huimhreacha na leathanach sa bhunleabhar priontála. Déantar na comhaid seo a shábháil i bhfeistí Kindle mar aon le comhaid ríomhleabhair Amazon. Ní féidir leat na comhaid APNX a oscailt ná a chur in eagar.

## Sonraíochtaí Formáid Chomhaid APNX ##

### Leagan Amach

|bearta | ábhar| tuairimí|
---|---|---|
|4 |00010001 | Aitheantóir formáide. Luach 65537 gan teorainn, ||
|4 |tús an chéad cheann eile | An fhritháireamh tar éis deireadh a chur le suíomh an chéad cheannteidil. Cuirtear tús le seicheamh nua faisnéise ceanntásca|
|4 |fad | Fad an chéad cheannteidil |
|N |an chéad cheannteideal | Teaghrán ina bhfuil ceanntásc ábhair. Tosaíonn sé an chéad seicheamh eile|
|2 |anaithnid | I gcónaí 1|
|2 | fad | Fad an dara ceanntásc |
|2 | líon na leathanach | Líon iomlán na mbeart tar éis an dara ceanntásc a sheasann do na leathanaigh. Áirítear leis an iomlán seo bearta a dtugann an leathanachMap neamhaird orthu.|
|2 |anaithnid | I gcónaí 32|
|N |an dara ceanntásc | Teaghrán ina bhfuil an ceanntásc mapála leathanaigh |
|4*N |stuáil | Léiríonn an chéad uimhir a thugtar i gceanntásc na mapála leathanaigh líon na 0 beart.|
|4*N | liosta leathanach ||

### Ceanntásc Ábhair

Is éard atá i gceanntásc an ábhair teaghrán atá faoi iamh in {} ina bhfuil eochair, péirí luacha:

|ábhar| tuairimí|
---|---|
|treoir ábhar| Treoraí.|
| asainn | Aitheantóir Amazon don leagan Kindle den leabhar.|
|Cineál | Cineál cde MOBI. Ba cheart go mbeadh EBOK ann i gcónaí do ríomhleabhair.|
|fileRevisionId | Leasú ar an gcomhad seo.|

#### Sampla
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Ceanntásc Mapála Leathanaigh
Is éard atá sa cheanntásc mapála leathanaigh ná teaghrán iniata in {} ina bhfuil eochair, péirí luacha.

|ábhar | tuairimí|
---|---|
| asainn | ISBN 10 don leabhar páipéir a gcomhfhreagraíonn na leathanaigh dó|
|leathanachMapa| Trí luach tuple. Is cosúil: (N,N,N)\
1) Líon na mbeart i ndiaidh an chinnteidil a thosaíonn an t-ord uimhrithe leathanaigh\
2) anaithnid\
3) anaithnid\|
#### Sampla
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Liosta Leathanach

Is é atá sa liosta leathanach ná seicheamh fritháirimh sa HTML amh. gach ceann
luach tús leathanach nua. Is endian mór 4 bheart gach iontráil
slánuimhir



## Tagairtí

* [Formáid comhaid Amazon APNX](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)

* [APNX - le MobileRead Wiki]( https://wiki.mobileread.com/wiki/APNX)


