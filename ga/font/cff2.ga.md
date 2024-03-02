{
  "date": "2020-08-20",
  "keywords": [
"comhad cff2",
"Formáid comhaid cff2 saor in aisce,",
"Cad is comhad cff2 ann",
"comhad",
"sampla cff2",
"Síneadh comhad cff2 saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF2 - Leagan 2 den Fhormáid Cló Dlúth",
  "description": "Foghlaim faoi Fhormáid Chomhaid CFF2 agus APInna chun comhaid CFF2 a chruthú agus a oscailt.",
  "linktitle": "CFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cff-ga2"
}
},
  "lastmod": "2020-10-21"
}

## Cad is comhad CFF2 ann?

CFF2 file format is the version 2.0 of the CFF file format and allows efficient storage of glyph outlines and metadata similar to the CFF file format. CFF2 differs from CFF in that it is intended to be used in the context of an OpenType font as a 'sfnt' table with the tag CFF2. Ní féidir é a úsáid mar chlár neamhspleách agus braitheann sé ar shonraí i dtáblaí OpenType eile.

## Formáid Comhaid CFF2

Tá sonraí sa [CFF2 file format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) faoi leagan amach inmheánach sonraí, cineálacha sonraí, táblaí agus faisnéis inmheánach eile faoin bhformáid comhaid. Is féidir é a tharchur le haghaidh tagartha an fhorbróra. Tá cuid de na sonraí fúthu seo mar a leanas.

### Leagan Amach Sonraí

Tá sonraí dénártha formáid comhaid CFF2 eagraithe go loighciúil mar roinnt struchtúir sonraí ar leith. Tá an leagan amach laistigh de na sonraí dénártha mar a thaispeántar sa tábla seo a leanas.

|Iontráil | Tráchtanna |
---|---|
|Ceanntásc |Suíomh seasta|
|DICT is fearr| Suíomh seasta|
|Innéacs Fo-Dhomhanda | Suíomh seasta|
|Athrú |Siopa|
|FDSelect |Ná láthair ach amháin má tá níos mó ná Cló DICT amháin san INDEX Cló DICT.|
|Cló INDEX DICT ||
|Eagar Clónna DICT| San áireamh i Cló INDEX DICT.|
|DiCT Príobháideach| Ceann in aghaidh an Cló DICT.|

Níl ach na chéad trí struchtúr bunaithe ar láithreacha seasta. Baintear amach an chuid eile trí fhritháirimh, agus is féidir a n-ordú a athrú.

### Cineálacha Sonraí

Úsáideann formáid comhaid CFF2 na cineálacha sonraí seo a leanas.

|Ainm | Raon | Cur síos|
---|---|---|
|uint8 |0 go 255 |Uimhir 8 ngiotán gan síniú |
|uint16 |0 go 65535| Uimhir 16 ghiotán gan síniú |
|uint32 |0 go 4294967295| Uimhir 32-giotán gan síniú |
|Fritháireamh | athraíonn| Fritháireamh beart 1, 2, 3, nó 4 (arna sonrú ag réimse OffSize i dtábla Innéacs)|
|Amhmhéid |1 go 4| Sonraíonn uimhir neamhshínithe 1 bheart méid réimse nó réimsí Fritháireamh|

Stórálann sé na sonraí uimhriúla ilbhearta go léir agus na réimsí fritháirimh in ord beart mór-endian. Tá formáid CFF2 saor ó bhearta stuála mar ní urramaíonn sé aon srianta ailínithe.

### Sonraí DICT

Cuimsíonn comhaid CFF2 sonraí an fhoclóra cló mar phéirí eochairluacha i bhformáid dhlúth comharthaíochta. Ionchódaítear eochracha foclóra mar 1 nó 2 oibreoir beart agus déantar luachanna foclóir a ionchódú mar oibriúcháin uimhriúla inathraithe-mhéid. Tá trí struchtúr ann a úsáideann formáid Sonraí DICT: `Top DICT`, `Cló DICT` agus `DiCT Príobháideach`. Sainmhínítear roinnt cineálacha slánuimhir operand de mhéideanna éagsúla agus déantar iad a ionchódú mar a thaispeántar sa tábla seo a leanas (is é b0 an chéad bheart den operand, an dara beart b1, agus mar sin de).

|Méid | raon b0 |Raon luacha |Ríomh luacha |
---|---|---|---|
|1 |32 go 246| -107 go +107 |b0 - 139|
|2	|247 to 250|	+108 to +1131	|(b0 - 247) * 256 + b1 + 108|
|2	|251 to 254|	-1131 to -108|	-(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 go +32767| b1 << 8 | b2|
|5 |29| -(2^31) go +(2^31 - 1)| b1 <<24 || b2 << 16 \ || b3 <<8 || b4|

### Ceanntásc

Tosaíonn na sonraí dénártha le ceanntásc a bhfuil an fhormáid a thaispeántar sa Tábla thíos.

|Cineál |Ainm |Cur síos|
---|---|---|
|uint8| mórleagan| Leagan mór formáid. Socraigh go 2. ||
|uint8| mionleagan| Formáid leagan mion. Socraigh go nialas.|
|uint8| Méid ceanntásca| Méid an cheanntásca (bearta).|
|uint16| barrDictLength| Fad struchtúr Top DICT i mbearta.|

## Tagairtí

 * [Formáid Comhaid CFF2]( https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

