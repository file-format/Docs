{
  "date": "2019-10-11",
  "keywords": [
"tga comhad",
"formáid comhaid tga",
"cad is comhad tga",
"comhad",
"tga shampla",
"síneadh comhad tga",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid TGA - Comhad Íomhá Grafach TARGA",
  "description": "Foghlaim faoi fhormáid comhaid TGA agus APIanna ar féidir leo comhaid TGA a chruthú agus a oscailt.",
  "linktitle": "TGA",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-tg-gaa"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad TGA ann?

Is formáid ghrafach raster é comhad le síneadh .tga agus chruthaigh Truevision Inc é. Dearadh é do bhoird TARGA (Truevision Advanced Raster Adapter) agus chuir sé tacaíocht taispeána Highcolor/fíordhathanna ar fáil do ríomhairí pearsanta IBM-comhoiriúnach. Tacaíonn sé le 8, 16, 24 agus 32 giotán in aghaidh an picteilín agus cainéal alfa 8-giotán. Tacaíonn sé freisin le comhbhrú RLE lossless is féidir a chur i bhfeidhm chun laghdú ar an méid íomhá. Úsáideann grianghraif agus uigeachtaí digiteacha formáid íomhá TGA.

## Stair Ghearr

Tháinig foirmiú comhaid TGA ar an saol i 1984 ag AT&T EPICenter (a bhaintear agus a foirmíodh níos déanaí mar eintiteas neamhspleách ar a dtugtar Truevision) a bhí ag obair ar mhargaíocht teicneolaíochtaí nua arna bhforbairt ag AT&T le haghaidh maoláin fhráma datha. Bhí EPICenter ag obair ar a chéad dá chárta cheana féin, an VDA (Cuibheoir Taispeána Físeáin) agus ICB (bord gabhála íomhánna) a raibh obair ar dhá chineál comhaid, .vda agus .icb, ar siúl cheana féin ina leith. Códaíodh na formáidí comhaid seo agus tugadh isteach TGA formáid comhaid nach raibh chomh leathan céanna. Síneadh a bhí in TGA ar a raibh in úsáid cheana féin, agus chuir sé faisnéis ar fáil mar leithead, airde, doimhneacht picteilín, léarscáil datha gaolmhar agus tionscnamh íomhá.

Áiríodh i leagan 2.0 TGA, a foilsíodh i 1989, roinnt gnéithe feabhsaithe mar:

 * Mionsamhlacha
 * Cainéal alfa
 * Luach Gáma
 * Meiteashonraí Téacsúla

I measc na bpríomh-rannpháirtithe do leagan 2.0 TGA tá Shawn Steiner ó Truevision, Kevin Fiedly agus David Spoelstra.

## Sonraíochtaí Formáid Comhaid TGA TARGA

Tá 2 phríomhchuid i gcomhad TGA:

 * Ceanntásc
 * Eolas Dath picteilíní

Tá na luachanna go léir i gcomhad TGA i littl-endian de réir na sonraíochtaí formáide.

### Ceanntásc TGA

Tá na 5 réimse seo a leanas i gceanntásc comhaid TGA.

|Uimhir an raoin.|Fad |Ainm an raoin |Cur síos|
---|---|---|---|
|1| 1 beart | fad aitheantais| Fad réimse aitheantais na híomhá (0-255)|
|2| 1 beart |Cineál datha léarscáile| Cibé an bhfuil léarscáil daite san áireamh (0 - léiríonn sé nach bhfuil aon sonraí léarscáile daite san áireamh leis an íomhá seo. 1 - léiríonn sé go bhfuil mapa daite san áireamh leis an íomhá seo.)|
|3| 1 beart |Cineál íomhá| Cineálacha comhbhrú agus datha (0- Níl Sonraí Íomhá san áireamh. 1- Neamh-chomhbhrúite, Íomhá mapáilte le dath, 2- Neamh-chomhbhrúite, Íomhá Fíordhath, 9- Fad Rith ionchódaithe, Íomhá mapáilte le dath, 11- Fad Rith ionchódaithe, Íomhá dubh agus bán )|
|4| 5 beart |Sonraíocht léarscáile daite| Cur síos ar an léarscáil dathanna|
|5| 10 beart |Sonraíocht íomhá| Toisí agus formáid na híomhá|

### Sonraí Léarscáile Íomhá agus Datha

| Réimse uimh. |Fad | Réimse | Cur síos |
---|---|---|---|
|6 |Ó réimse fhad aitheantais na híomhá| Aitheantas na hÍomhá| Réimse roghnach ina bhfuil faisnéis aitheantais |
|7 |Ó réimse sonraíochta léarscáile datha| Sonraí léarscáile datha| Tábla cuardaigh ina bhfuil sonraí léarscáile daite|
|8 |Ó réimse sonraíochta na híomhá| Sonraí íomhá| Stóráilte de réir tuairisceoir na híomhá |

### Réimse Forbróra (Roghnach)

Soláthraíonn TGA Leagan 2.0 tacaíocht le haghaidh feabhsuithe/breise breise a raibh go leor forbróirí ag iarraidh tuilleadh eolais a stóráil. Tá an fhaisnéis roghnach sa chaoi is mura bhfuil díchódóir TGA in ann í a léirmhíniú, déanfar neamhaird de.

### Réimse Sínte (Roghnach)

|Uimhir réimse.| Fad| Réimse | Cur síos|
---|---|---|---|
|10| 2 beart |Méid an tsínte |Méid na mbeart i limistéar an tsínidh, 495 i gcónaí|
|11| 41 beart| Ainm an údair |Ainm an údair. Mura n-úsáidtear iad, ba chóir bearta a shocrú go NULLComment (\0) nó spásanna|
|12| 324 beart| Trácht an údair| Nóta tráchta, eagraithe i gceithre líne, gach ceann comhdhéanta de 80 carachtar móide NULLComment |
|13| 12 beart| Stampa dáta/ama |Dáta agus am ar cruthaíodh an íomhá|
|14| 41 beart| ID poist||
|15| 6 beart| Am fostaíochta| Uaireanta, nóiméad agus soicind a chaitear ag cruthú an chomhaid (le haghaidh billeála, etc.)|
|16| 41 beart| ID Bogearraí |An feidhmchlár a chruthaigh an comhad.|
|17| 3 beart| Leagan bogearraí ||
|18| 4 beart| Dath eochrach||
|19| 4 beart| Cóimheas gné picteilín ||
|20| 4 beart| Luach gáma||
|21| 4 beart| Fritháireamh ceartúcháin dathanna |Líon beart ó thús an chomhaid go dtí an tábla ceartúcháin dathanna má tá sé i láthair|
|22| 4 beart| Stampa postais | Líon na mbeart ó thús an chomhaid go dtí an íomhá stampa postais más ann |
|23| 4 beart| Fritháireamh líne scanadh| Líon na mbeart ó thús an chomhaid go dtí an tábla línte scan má tá sé i láthair|
|24| 1 beart| Cineál tréithe| Sonraítear an cainéal alfa|

### Buntásc Comhad (Roghnach)

Is ionann na 26 beart deiridh den chomhad agus an buntásc, rud a chiallaíonn más ann do chomhad leagan 2 TGA.

|Réimse Uimh.| Fad| Réimse| Cur Síos|
---|---|---|---|
|28| 4 beart| Fritháireamh síneadh | Fritháireamh i mbeart ó thús an chomhaid|
|29| 4 beart| Fritháireamh an limistéir fhorbróra| Fritháireamh i mbeart ó thús an chomhaid|
|30| 16 beart| Síniú| Tá TRUEVISION-XFILE |
|31| 1 beart| | Tá .|
|32| 1 beart| | Tá NULLComment |


## Tagairtí

 * [TGA 2.0 File Format Specifications](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
 * [TGA le Vicipéid](https://ga.wikipedia.org/wiki/Truevision_TGA)

