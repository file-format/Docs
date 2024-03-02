{
  "date": "2021-06-29",
  "keywords": [
"ICNS",
"síneadh",
"comhad",
"formáid",
"íomha",
"Íomhá Icon Apple",
"macOS",
"Úll",
"Deilbhín"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICNS - Íomhá Icon Apple",
  "description": "Foghlaim faoi fhormáid comhaid ICNS agus APIs ar féidir leo comhaid ICNS a chruthú agus a oscailt.",
  "linktitle": "ICNS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-icn-gas"
}
},
  "lastmod": "2021-06-29"
}

## Cad is comhad ICNS ann? ##

Tugtar comhad ICNS ar fhormáid deilbhín a úsáideann cláir macOS. Ceadaíonn sé bandaí alfa 1-giotán agus 8-giotán agus sábhálann sé pictiúr amháin nó níos mó, déanta as doiciméid [PNG](/image/png/) de ghnáth. Taispeántar deilbhín an chláir i mbrabhsálaí agus comhéadan macOS ag baint úsáide as comhaid ICNS.

Bunaithe ar an suíomh, is féidir socruithe iolracha a bheith ag an deilbhín stíl chéanna. Tá go leor athruithe déanta ar fhormáid an ICNS agus tá sí tagtha chun cinn go dtí an pointe gur féidir é a úsáid anois mar bhunús le haghaidh formáidí comhoiriúnacha éagsúla. Seo roinnt pointí tábhachtacha eile nach mór duit fios a bheith agat:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource, agus Mac OS icons Resource tá cuid de na hainmneacha eile. 

* Chun eolas a fháil ar dheilbhín, úsáidtear foinse sa bhrainse acmhainne.

* I bhformhór na gcásanna, tá go leor íomhánna i gcomhad. Tá méideanna pictiúir tacaithe ag 1612 picteilín cearnach agus 1024, 512, 256, 128, 48, 32, agus 16 picteilín cearnach.



## Formáid Chomhaid ICNS ##

Is capsule é formáid sonraí an ICNS le haghaidh íomhá amháin nó níos mó, ag tacú le bannaí 1-giotán agus stáit íomhá iomadúla.
Is féidir leis an gcóras oibriúcháin pictiúir deilbhín a athrú chun an méid taispeána atá riachtanach a oiriúnú. Go hiondúil déantar na pictiúir deilbhíní níos mó a shábháil mar chomhaid [JPEG](/image/jpeg/) 2000 nó [PNG](/image/png/). Is féidir cineál comhaid ICNS comhbhrúite agus neamh-chomhbhrúite araon.

Comhdhéanann ceanntásc agus sonraí deilbhín dhénártha struchtúr comhaid ICNS. Tá 8 mbeart sonraí sa cheanntásc, ceithre cinn acu mar an draíocht liteartha agus ceithre cinn acu ar fad an chomhaid. Stóráiltear cineál agus méid gach pictiúr deilbhín sa rannóg sonraí deilbhín, a leanann na sonraí íomhá dhénártha. Cinneann méid an phictiúir méid an ailt dhénártha.

## Sonraíocht Theicniúil ##

### Ceanntásc ###

|Fritháireamh|Méid|Cuspóir
---|---|---|
|0|4|Draíocht litriúil, ní mór gur icns é (0x69, 0x63, 0x6e, 0x73)
|4|4|Fad an chomhaid, i mbearta, msb ar dtús


### sonraí deilbhín ###

|Fritháireamh|Méid|Cuspóir
---|---|---|
|0|4|Cineál deilbhín
|4|4|Fad na sonraí, i mbearta (lena n-áirítear cineál agus fad), msb ar dtús
|8|Athróg|Sonraí deilbhín

### Comhbhrú ###

Tá na sonraí picteilín comhbhrúite go pointe áirithe. Is minic a chomhbhrúitear na picteilíní 32-giotán (is32, il32, ih32, it32) agus ARGB (ic04, ic05) (in aghaidh an chainéil) ar bhealach cosúil le PackBits.

|Luach Luaidhe|Tailbhearta|Toradh (neamh-chomhbhrúite)
---|---|---|
|0 - 127|1 - 128|1 - 128 Beart
|128 - 255|1 Beart|3 - 130 Cóip

## Tagairt ##

* [ICNS - Vicipéid]( https://en.wikipedia.org/wiki/Apple_Icon_Image_format)


