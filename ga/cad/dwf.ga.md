{
  "date": "2020-03-16",
  "keywords": [
"DWF",
"Formáid Chomhaid",
"Oscail",
"Léigh",
"Cruthaigh",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Learn about DWF file format and APIs that can create and open DWF files.",
  "title": "DWF File Format",
  "linktitle": "DWF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dwf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad DWF ann?

Léiríonn Dearadh Gréasáin Formáid (DWF) líníocht 2D/3D i bhformáid chomhbhrúite chun comhaid dearaidh a fheiceáil, a athbhreithniú nó a phriontáil. Tá grafaicí agus téacs mar chuid de shonraí dearaidh agus laghdaíonn sé méid an chomhaid mar gheall ar a bhformáid chomhbhrúite. Déanann an méid comhaid laghdaithe dáileadh agus cumarsáid sonraí deartha saibhir go héifeachtach. Ní éilíonn DWF go mbeadh an faighteoir ar an eolas faoi úsáid na mbogearraí CAD a chruthaigh an líníocht bhunaidh. Is féidir leis an ábhar i bhformáid comhaid DWF a bheith simplí agus gan ach bileog amháin nó casta go leor chun clónna, dath, agus íomhánna a bheith san áireamh.

## Stair Ghearr ##

Thug Autodesk formáid comhaid DWF isteach i 1995 mar chuid de plug-in Netscape Nascleanúint, WHIP. Tháinig an fhormáid chun cinn ó fhormáid 2T amháin chun ábhair 3T a chur san áireamh le himeacht ama. Baineann go leor feidhmchlár tríú páirtí leas as an bhformáid seo freisin.

## Formáid Chomhaid DWF ##

Is formáid oscailte, slán é DWF atá deartha go sonrach chun sonraí dearadh innealtóireachta saibhir a roinnt. Tá sé neamhspleách ar na bogearraí feidhmchláir bhunaidh, na crua-earraí agus an córas oibriúcháin a úsáideadh chun na sonraí dearaidh sin a chruthú. Cuireann sé seo ar chumas na mball foirne nach n-úsáideann feidhmchláir CAD páirt a ghlacadh sna próisis dhigiteacha trí amharc ar dhearadh foirgnimh, GIS nó táirgí. Tá roinnt comhaid XML agus dhénártha i gcartlann comhaid DWF atá pacáistithe le chéile i gcartlann chomhbhrúite a cruthaíodh le comhbhrú [ZIP](/compression/zip/). Is féidir leat síneadh comhad DWF a athainmniú go ZIP agus féachaint ar a bhfuil sa chomhad. Is féidir go leor cineálacha sonraí dearaidh a bheith sa phacáiste DWF, mar shampla grafaic 2T, grafaicí 3D, meiteashonraí pacáiste agus rannáin, agus comhaid acmhainne eile.

**DWF metadata files** – XML files that contain information pertaining to metadata and structure (author, title, creation time, section dependencies, section ordering, resource file descriptions, roles, mimetypes, etc.) and pertaining to the section (page information, design metadata, etc.).  The structural metadata is used to create logical objects (collections of files to represent a part or page, etc.).

**Comhaid acmhainne** – comhaid meán nó ábhair eile a ndéantar tagairt dóibh ó mheiteashonraí an phacáiste/rannáin agus ar gnách iad a chur i láthair sonraí dearaidh i bhformáidí éagsúla (ZGL, W2D, [JPG](/image/jpeg/), [PNG](/image/png/), AVI, XML, [TXT](/word-processing/txt/), [DOC](/word-processing/doc/), srl.)

### Sonraí Formáid Chomhaid ###

Tá comhaid DWF eagraithe i dtrí phríomhchuid mar a thaispeántar thíos.

* Ceanntásc aitheantais comhaid

* Comhad bloc sonraí

* Leantóir foirceannadh comhaid


#### Ceanntásc Aitheantóra Comhad ####

The file identifier header allows for identification of DWF files by applications. It also identifies which version of DWF specifications was used for encoding the file. It is a 12 byte header that is arranged as follow:


| Beart|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Carachtar|(|D|W|F|(spás)|V|0|0|.|3|0|)

Seo achoimre ar an tábla seo:

* Léiríonn na chéad sé bheart den cheanntásc carachtair ASCII i gcónaí "(DWF V"

* Sna 5 bheart seo a leanas tá faisnéis faoin uimhir leagain m.sh. "00.30" le luach leagain mór agus mion na formáid


Ba cheart go sonródh feidhmchláir a chruthaíonn comhad DWF an uimhir leagain is ísle is féidir a chaithfidh feidhmchlár léitheora tacú léi chun na sonraí a úsáid i gceart.

#### Bloc Sonraí Comhad ####

Tosaíonn an bloc sonraí comhaid ag an 13ú beart de chomhad DWF, agus is sraith de phéirí opcode agus operand é, mar atá sa tábla seo a leanas.

| Réimse 1 | Réimse 2 | Réimse 3 | Réimse 4 | Réimse 5 | Réimse 5
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

Is féidir le péirí opcode-operand a bheith i gcomhad DWF mar ASCII inléite chomh maith le cód dénártha nó meascán den dá cheann acu seo. Tá foirm opcode/operand ASCII inléite ag gach oibríocht DWF, agus tá foirm opcode/operand dhénártha códaithe ag formhór na n-oibríochtaí. Tá opcodes i mbeart aonair a cheadaíonn breis agus 200 oibríocht. Is cásanna eisceachtúla iad ASCII leathnaithe agus dénártha leathnaithe. Is féidir le luachanna Opcodes raon ó 0-255 le roinnt eisceachtaí. Seachas an dá chineál speisialta opcodes sínte ASCII agus dénártha leathnaithe, ní mór go mbeadh a fhios ag léitheoir comhaid conas an fad operand a ríomh.

##### Roghanna Toirmiscthe #####

Ní féidir na huiríll ASCII do na nithe seo a leanas a úsáid mar opcodes:

Ní féidir tar éis uiríll ASCII a úsáid mar opcodes:

* Spás (0x20)

* Cluaisín (0x09)

* Fleiscín (0x2D)

* digití ASCII 0-9 (0x30 - 0x39)

* Seol ar ais (0x0D)

* Fotha líne (0x0A)

* Comhartha Athfhriotail Aonair (0x27)

* Comhartha athfhriotail dhúbailte (0x22)

* Tréimhse (0x2E)

* Parenthesis (0x28 agus 0x29)

* Lúibíní curacha (0x7B agus 0x7D)

* Lúibíní cearnacha (0x5B agus 0x5D)

* Slais ar gcúl (0x5C)


#### Leantóir Foirceannadh Comhad ####

Níl sa leantóir foirceanta comhaid le haghaidh DWF ach opcode speisialta a léiríonn deireadh an chomhaid. Is féidir le roinnt feidhmchlár sonraí neamh-DWF a stóráil tar éis an fhoirceannadh opcode.Tá an leantóir mar a thaispeántar thíos:


| Beart|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Carachtar|(|E|n|d|0|f|D|W|F|)

## Tagairtí ##

* [DWF - Le Vicipéid](https://ga.wikipedia.org/wiki/Design_Web_Format)

* [Formáid Sonraí WHIP](http://paulbourke.net/dataformats/whip/)

* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1 ](https://learn.microsoft.com/en-us/archive/blogs /opc/eachtraí-i-phacáistiú-eipeasóid-1)


