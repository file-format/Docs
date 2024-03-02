{
  "date": "2020-08-20",
  "keywords": [
"comhad otf",
"formáid comhaid otf",
"cad is comhad otf ann",
"comhad",
"sampla otf",
"síneadh comhad otf",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTF - Formáid Comhaid Cló TrueType",
  "description": "Foghlaim faoi fhormáid comhaid OTF agus APIanna ar féidir comhaid OTF a chruthú agus a oscailt.",
  "linktitle": "OTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-ot-gaf"
}
},
  "lastmod": "2020-09-21"
}

## Cad is comhad OTF ann?

Tagraíonn comhad le síneadh .otf d'fhormáid chló OpenType. Tá formáid chló OTF níos inscálaithe agus leathnaíonn sí na gnéithe atá ann cheana i bhformáidí [TTF](/font/ttf/) le haghaidh clóghrafaíocht dhigiteach. Arna fhorbairt ag Microsoft agus Adobe, comhcheanglaíonn OTF gnéithe formáidí cló PostScript agus TrueType. Déanann sé seo formáid OTF chun freastal ar chórais scríbhneoireachta tromlaigh agus is é sin an fáth go n-úsáidtear go haonfhoirmeach é ar ardáin mhóra ríomhaireachta. Tacaíonn Mac OS X agus Windows 2000 agus níos déanaí le formáid an chló OpenType.

## Stair Ghearr

The requirement of OpenType fonts originated as a requirement for a more expressive font format that could handle fine typography. In addition, it was aimed to meet the requirements of complex behaviour of many of the world's writing systems. Microsoft attempted to license Apple's advanced typography technology, known as GX Typography, in the early 1990's. This didn't go well and as a result, Microsoft started enhancing its owns TrueType font technology in 1994. Áiríodh leis na modhnuithe freisin formáid chló níos oiriúnaí a thabhairt isteach a chomhlíonann gnéithe formáidí cló Cineál 1 (PostScript) Adobe.

Chuaigh Adobe, i 1996, le Microsoft ina chuid iarrachtaí chun dul in ionad TrueType Apple agus a bhformáidí cló Cineál 1 féin. Ba é an toradh a bhí air seo ná an dá fhormáid bhunúsacha cló a chomhcheangal chun na teorainneacha a shárú agus síntí nua a chur leis. Tugadh an teicneolaíocht nua seo isteach an bhliain chéanna leis an ainm **OpenType**.

## Sonraíochtaí Formáid Comhaid OTF

OTF specifications are available publicly by Microsoft and can be referred to from developer's perspective. Like TTF, it uses the same 'sfnt' container structure and is compatible with the TrueType specifications. Data inside an OpenType font file is used for different purposes such as calculating the text layout, defining glyphs as TrueType or Compact Font Format (CFF) outlines, providing monochromatic or color bitmaps or SVG documents as alternate glyph descriptions, and meta-data information.

### Cineálacha Sonraí OTF
Úsáideann comhaid OTF na cineálacha sonraí seo a leanas atá ar fad in Big Endian.

|Cineál Sonraí| Cur Síos|
---|---|
|uint8| Slánuimhir 8-giotán gan síniú. ||
|int8| Slánuimhir sínithe 8-giotán.|
|uint16| Slánuimhir 16-giotán gan síniú. ||
|int16| Slánuimhir sínithe 16-giotán. ||
|uint24| Slánuimhir 24-giotán gan síniú. ||
|uint32| Slánuimhir 32-giotán gan síniú. ||
|int32| Slánuimhir sínithe 32-giotán. ||
|Seasta| Uimhir phointe seasta sínithe 32-giotán (16.16)|
|FWORD| int16 a chuireann síos ar chainníocht in aonaid dearaidh cló.|
|UFWORD| uint16 a chuireann síos ar chainníocht in aonaid dearaidh cló.|
|F2DOT14| Uimhir sheasta sínithe 16-giotán agus an 14 ghiotán íseal den chodán (2.14) ||
|FADDATETIME| Tá an dáta agus an t-am léirithe i líon na soicind ó 12:00 meán oíche, 1 Eanáir, 1904, UTC. Léirítear an luach mar shlánuimhir sínithe 64-giotán.|
|Clib| Sraith de cheithre uint8 (fad = 32 giotán) a úsáidtear chun tábla, ais deartha-éagsúlachta, script, córas teanga, gné, nó bonnlíne a aithint |
|Fritháireamh16| Fritháireamh gearr chuig tábla, mar an gcéanna le uint16, fritháireamh NULLComment = 0x0000|
|Fritháireamh32| Fritháireamh fada le tábla, mar an gcéanna le uint32, fritháireamh NULLComment = 0x00000000|
|Leagan16Dot16| Luach pacáilte 32-giotán le huimhreacha móra agus mionleaganacha. (Féach Tábla Uimhreacha Leaganacha.)|

### Eolaire Táblaí OTF

Tosaíonn comhad OTF le eolaire tábla. Is é an t-eolaire seo an bailiúchán barrleibhéil de na táblaí sa chlóchomhad. Ag brath ar líon na gclónna i gcomhad, d'fhéadfadh an t-eolaire tábla a bheith suite in áiteanna éagsúla sa chomhad. Mar shampla, i gcás nach bhfuil ach cló amháin sa chomhad cló, tosaíonn an t-eolaire tábla ag beart 0 den chomhad. I gcás bailiúchán iolrach Clónna OpenType,
tá an t-eolaire tábla ag tosú léirithe sa TTCheader.

|Cineál |Ainm |Cur síos|
---|---|---|
|uint32 |sfntLeagan| 0x00010000 nó 0x4F54544F ('OTTO') |
|uint16| numTables |Líon táblaí.|
|uint16|	searchRange	|Maximum power of 2 less than or equal to numTables, times 16 ((2\**floor(log2(numTables))) * 16, i gcás inar oibreoir easpónantúcháin é **”)).|
|uint16 |Iontráil Loga Roghnóra2 den chumhacht uasta 2 níos lú ná nó cothrom le huimhreacha Táblaí (log2(Range Cuardach/16), atá cothrom le hurlár(log2(numTables))).|
|uint16	|rangeShift	|numTables times 16, minus searchRange ((numTables * 16) - raon cuardaigh).|
|Taifead boird| tableRecords[numTables] |Eagar taifid táblaí – ceann do gach tábla barrleibhéil sa chló|


### Taifead Tábla

I gcás gach tábla ardleibhéil sa chló, tá Taifead Tábla ina bhfuil na réimsí seo a leanas.

|Cineál| Ainm| Cur Síos|
---|---|---|
|Clib| táblaClib| Aitheantóir tábla.|
|uint32| sheic | Seiceam don tábla seo.|
|Fritháireamh32| fritháireamh| Fritháireamh ó thús an chomhaid chló.|
|uint32| fad Fad an tábla seo.|

Tá gach tábla sa chlóchomhad OpenType léirithe ag ainmneacha ar a dtugtar clibeanna tábla. Ní mór na taifid go léir san eagar a shórtáil in ord ardaitheach de réir clib.

## Tagairtí
 * [Sonraíochtaí Cló OpenType le Microsoft]( https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [Forbhreathnú TrueType]( https://learn.microsoft.com/en-us/typography/truetype/)

