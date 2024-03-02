{
  "date": "2020-08-20",
  "keywords": [
"comhad ttf",
"Formáid comhaid ttf",
"Cad is comhad ttf ann",
"comhad",
"ttf shampla",
"Síneadh comhad ttf",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TTF - Formáid Comhaid Cló TrueType",
  "description": "Tá clónna TrueType (TTF) bunaithe ar shonraíochtaí teicneolaíochta cló digiteach a dhear Apple, Inc ar dtús. Bhain Apple agus Microsoft úsáid as TTF ar chórais oibriúcháin Mac agus Windows.",
  "linktitle": "TTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-gaf"
}
},
  "lastmod": "2020-09-21"
}

## Cad is comhad TTF ann?

Léiríonn comhad le síneadh .ttf comhaid chló bunaithe ar theicneolaíocht chló sonraíochtaí TrueType. Dhear agus sheol Apple Computer, Inc le haghaidh Mac OS ar dtús é agus ghlac Microsoft le haghaidh Windows OS é níos déanaí. Soláthraíonn clónna TrueType taispeáint den chaighdeán is airde ar scáileáin agus printéirí ríomhaire gan spleáchas ar thaifeach. Tá gach feidhmchlár nua-aimseartha a úsáideann clónna in ann oibriú le comhaid TTF. Tá comhaid chló TTF ar fáil go héasca ar an idirlíon agus is féidir iad a thiontú go formáidí clóchomhaid eile ar nós OTF agus WOFF.

## Stair Ghearr

Designed by Apply Computer, Inc in 1980s for MacOS, the TTF font format was aimed at resolving some technical limitations by Adobe's Type 1 format. Apple included support for TrueType fonts in Mac in 1991. Ba é an cuspóir deartha a bhí taobh thiar de chlónna TTF ná éifeachtúlacht stórála agus próiseála, agus insínteacht. Bunaithe ar an fairsingeacht seo, is féidir clónna atá ann cheana a thiontú go formáid TrueType.

Bhain Microsoft úsáid as na clónna TrueType i Windows 3.1 den chéad uair i mí Aibreáin 1992 tar éis d’Apple aontú ar TrueType a cheadúnú do Microsoft. D'fheabhsaigh sé an meicníocht rasterization, agus d'fheabhsaigh sé a éifeachtúlacht agus a fheidhmíocht.

## Sonraíochtaí Fíor-Chineál Formáide Comhaid

Is comhad dénártha é clóchomhad TrueType atá comhdhéanta de sheicheamh táblaí comhcheangailte. Is seicheamh focal é gach tábla agus tá ainm ar a dtugtar `Clib`. Tá gach clib de chineál sonraí uint32 agus tá ceithre charachtar ann. Is eolaire cló é an chéad tábla sa chomhad a thugann rochtain ar tháblaí eile sa chlóchomhad. Tá sonraí cló i dtáblaí eile agus ina dhiaidh sin tar éis an tábla eolaire cló. Ós rud é go bhfuil gach tábla inrochtana ag a chlib, is féidir na táblaí le feiceáil in aon ord sa chomhad.

Taispeántar na táblaí riachtanacha agus a n-ainmneacha clibeanna sa tábla seo a leanas.

|**Clib**|**Tábla**|
---|---|
|'cmap'| mapáil carachtar go glyph|
|'glyf'| sonraí glyph|
|'ceann'| ceanntásc cló|
|'hhea'| ceanntásc cothrománach |
|'hmtx'| méadracht chothrománach|
|'loca'| innéacs don suíomh|
|'uasmhéadú'| próifíl uasta |
|'ainm'| ainmniú|
|'post'| PostScript|

### Cineálacha Sonraí
Úsáideann clónna TrueType an tslánuimhir chaighdeánach agus na cineálacha sonraí breise mar atá liostaithe sa tábla seo a leanas.

|**Cineál Sonraí** | **Cur síos** |
---|---|
|gearrFrac| Codán sínithe 16-giotán |
|Seasta| Uimhir phointe seasta sínithe 16.16-giotán |
|FWord| Slánuimhir sínithe 16-giotán a chuireann síos ar chainníocht in FUUnits, an fad is lú intomhaiste san em spás.|
|uFWord| Slánuimhir 16-giotán gan síniú a chuireann síos ar chainníocht in FUNits, an fad is lú intomhaiste san em spás.|
|F2Dot14| Uimhir sheasta sínithe 16-giotán leis na 14 ghiotán ísle a sheasann don chodán.|
|longDateTime|	The long internal format of a date in seconds since 12:00 midnight, January 1, 1904. It is represented as a signed 64-bit integer.|

### Eolaire Cló

Is é an chéad tábla sa chló TrueType an t-eolaire cló a sholáthraíonn rochtain ar an bhfaisnéis a theastaíonn chun rochtain a fháil ar shonraí i dtáblaí eile. Ina theannta sin tá sé comhdhéanta de:

 * `Fritháireamh' - coimeádann sé taifead de na táblaí sa chló agus soláthraíonn sé faisnéis fhritháireamh chun rochtain a fháil ar gach tábla sa chomhadlann
 * `Eolaire Tábla` - Tá iontrálacha ann do gach tábla sa chló

#### Fritháireamh Fo-Tábla
Taispeántar thíos an fothábla fritháireamh.

|**Cineál**|**Ainm**|**Cur síos**|
---|---|---|
|uint32| cineál scálaire | Clib chun an scálaire OFA a chur in iúl a úsáidfear chun an cló seo a rasterú; féach an nóta ar an gcineál scálaire thíos le haghaidh tuilleadh eolais.|
|uint16| uimhreacha táblaí| líon na dtáblaí|
|uint16| raon cuardaigh| (uaschumhacht 2 <= numTables)*16|
|uint16| iontráilRoghnóir| log2(uaschumhacht 2 <= numTables)|
|uint16| raonShift| numTables*16-Raon cuardaigh|

#### Eolaire tábla
Tagann an t-eolaire tábla díreach tar éis an fhotábla fhritháireamh. Tá a struchtúr mar a thaispeántar sa tábla seo a leanas.

|**Cineál**|**Ainm**|**Cur síos**|
---|---|---|
|uint32| chlib | Aitheantóir 4-bheart |
|uint32| seicSum| sheic don tábla seo|
|uint32| fritháireamh| fritháireamh ó thús sfnt|
|uint32| fad| fad an tábla seo i mbeart (an fad iarbhír ní fad stuáilte)|

Caithfidh a iontráil eolaire tábla féin a bheith ag gach tábla i gcomhad cló. Ní mór iontrálacha i dtábla a shórtáil in ord ardaitheach de réir clib.


## Tagairtí
 * [Lámhleabhar Tagartha Cló TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
 * [Forbhreathnú TrueType]( https://learn.microsoft.com/en-us/typography/truetype/)

