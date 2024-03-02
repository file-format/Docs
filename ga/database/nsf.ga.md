{
  "date": "2020-11-11",
  "keywords": [
"NSF",
"síneadh",
"comhad",
"formáid comhaid",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Comhaid Bunachar Sonraí"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid NSF agus APIanna ar féidir leo comhaid NSF a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid NSF - Formáid Bunachar Sonraí Lotus Notes",
  "linktitle": "NSF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ns-gaf"
}
},
  "lastmod": "2020-08-12"
}

## Cad is comhad NSF ann?

Is formáid comhaid bunachar sonraí é comhad a bhfuil an síneadh .nsf (Notes Storage Facility) in úsáid ag an [IBM Notes software](https://en.wikipedia.org/wiki/HCL_Domino), ar tugadh Lotus Notes air roimhe seo. Sainmhíníonn sé an scéimre chun rudaí de chineálacha éagsúla a stóráil amhail ríomhphoist, coinní, doiciméid, foirmeacha agus tuairimí. Tá an fhaisnéis seo go léir le fáil i gcomhad amháin NSF le haghaidh comhoibriú gnó cosúil le comhad PST/OST. I measc cuid de na feidhmchláir is féidir comhaid NSF a oscailt tá IBM Lotus Notes agus IBM Domino.

## Sonraíochtaí Formáid Comhaid NSF

Is comhaid dhénártha iad comhaid NSF agus tá a sonraíochtaí ar fáil ag Joachim Metz ar [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). De réir na sonraí seo, cuimsíonn comhad NSF:

 * Ceanntásc Comhad
 * Ceanntásc Bunachar Sonraí

Ina theannta sin, tá sé comhdhéanta de:

 * Sárbhloc
 * Bloc tuairisceoir buicéad
 * Giotán
 * Buicéad Veicteoir Athlonnú Taifead
 * buicéid achoimre
 * Buicéid gan achoimre


### Ceanntásc Comhad NSF

6 beart atá i gceanntásc comhaid an NSF. Tá sé comhdhéanta de:

|Fritháireamh|Méid|Luach|Cur Síos|
---|---|---|---|
0|2|0x1a 0x00|Síniú|
2|4| |Méid ceanntásca an bhunachair shonraí|

### Ceanntásc bunachar sonraí

Tá na luachanna deimhnithe seo a leanas i gceanntásc Bhunachar Sonraí NSD.

 * Eolas Bunachar Sonraí
   * Aitheantóir bunachar sonraí (DBID)
 * Faisnéis maidir le macasamhlú
 * Bratacha maoláin faisnéise bunachar sonraí
   * Teideal
   * Catagóirí
   * Aicme
   * Aicme dearaidh (ainm teimpléad)
 * Aitheantóirí nótaí speisialta
 * Stuáil
 * Bunachar sonraí faisnéise fb2
 * Bunachar sonraí faisnéise 3
 * Bunachar sonraí faisnéise 4
 * Bunachar sonraí faisnéise 5
 * Stuáil
 * Aitheantóir cásanna bunachar sonraí (DBIID)
 * Stair macasamhlaithe

## Tagairtí

 * [Formáid NSF - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

