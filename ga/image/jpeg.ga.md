{
  "date": "2019-11-25",
  "keywords": [
"comhad jpeg",
"Formáid comhaid jpeg saor in aisce,",
"Cad is comhad jpeg ann",
"comhad",
"Sampla jpeg saor in aisce,",
"Síneadh comhad jpeg saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPEG - Formáid Chomhaid Íomhá",
  "description": "Foghlaim faoi fhormáid comhaid JPEG agus APIs ar féidir leo comhaid JPEG a chruthú agus a oscailt.",
  "linktitle": "JPEG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jpe-gag"
}
},
  "lastmod": "2020-08-08"
}

## Cad is comhad JPEG ann? ##

Is cineál formáid íomhá é JPEG a shábháiltear trí úsáid a bhaint as an modh comhbhrú caillteach. Tá an íomhá aschuir, mar thoradh ar chomhbhrú, ina chomhbhabhtáil idir méid stórála agus cáilíocht íomhá. Is féidir le húsáideoirí an leibhéal comhbhrúite a choigeartú chun an leibhéal cáilíochta atá ag teastáil a bhaint amach agus ag an am céanna an méid stórála a laghdú. Is beag tionchar a bheidh ar cháilíocht íomhá má chuirtear comhbhrú 10:1 ar an íomhá. Dá airde an luach comhbhrú, is airde an díghrádú ar cháilíocht íomhá.

## Sonraíochtaí Formáid Chomhaid ##

Rinne an Comhghrúpa Saineolaithe Grianghrafadóireachta caighdeánú formáid comhaid íomhá JPEG agus, mar sin, an t-ainm JPEG. Ba í an fhormáid rogha íomhánna grianghrafadóireachta a stóráil agus a tharchur ar an ngréasán. Tá lucht féachana ag beagnach gach córas Oibriúcháin anois a thacaíonn le léirshamhlú íomhánna JPEG, a stóráiltear go minic le síneadh JPG freisin. Tacaíonn fiú na brabhsálaithe gréasáin le léirshamhlú íomhánna JPEG. Sula dtéann tú isteach i sonraíochtaí formáid comhaid JPEG, ní mór próiseas foriomlán na gcéimeanna a bhaineann le cruthú JPEG a lua.

### Céimeanna Comhbhrúite JPEG ###

** Claochlú:** Aistrítear íomhánna datha ó RGB go íomhá luminance/crominance (tá Eye íogair do luminance, ní cróminance, ionas gur féidir leis an gcuid cróminance mórán sonraí a chailleadh agus mar sin is féidir iad a chomhbhrú go mór.

**Sampláil Síos:** Déantar an tsampláil síos don chomhpháirt daite agus ní don chomhpháirt luminance. Déantar sampláil anuas ag cóimheas 2:1 go cothrománach agus 1:1 go hingearach (2h 1 V). Mar sin laghdaítear méid na híomhá ós rud é nach bhfuil baint ag an gcomhpháirt 'y', níl aon chaillteanas suntasach ar cháilíocht na híomhá.

**Ag Eagrú i nGrúpaí:** Eagraítear picteilíní gach comhpháirte datha i ngrúpaí de 8×2 picteilín ar a dtugtar aonaid sonraí” mura bhfuil líon na sraitheanna nó na gcolún iolraí de 8, déantar an ró bun agus na colúin ar dheis a mhacasamhlú.

**Claochlú Comhsain Scoite:** Cuirtear Trasfhoirmiú Comhshínis Scoite (DCT) i bhfeidhm ansin ar gach aonad sonraí chun léarscáil 8×8 de chomhpháirteanna claochlaithe a chruthú. Tá roinnt caillteanas faisnéise i gceist le DCT mar gheall ar bheachtais theoranta na huimhríochta ríomhaireachta. Ciallaíonn sé seo go gcaillfear cáilíocht íomhá éigin fiú gan an léarscáil ach is gnách go mbíonn sé beag.

**Cainníochtú:** Roinntear gach ceann de na 64 comhpháirt trasfhoirmithe san aonad sonraí ar uimhir ar leith ar a dtugtar a 'Chainníochtú Comhéifeacht (QC)' agus ansin slánaítear iad go slánuimhir. Seo an áit a gcailltear faisnéis go do-aisghabhálach, bíonn QC Mór ina chúis le caillteanas níos mó. Go ginearálta, ceadaíonn an chuid is mó d’uirlisí JPEG táblaí QC a úsáid a mhol an caighdeán JPEG.

** Ionchódú:** Ionchódaítear na 64 comhéifeacht claochlaithe cainníochtaithe (Ar slánuimhreacha iad anois) de gach aonad sonraí trí úsáid a bhaint as códú RLE agus Huffman.

**Ceanntásc a Chur Leis:** Leis an gcéim dheireanach cuirtear ceanntásc agus na paraiméadair JPEG go léir a úsáideadh agus aschuirtear an toradh.

Úsáideann an díchódóir JPEG na céimeanna ar ais chun an íomhá bunaidh a ghiniúint ón gceann comhbhrúite.

### Struchtúr Comhad ###

Léirítear íomhá JPEG mar sheicheamh míreanna ina dtosaíonn gach mír le marcóir. Tosaíonn gach marcóir le beart 0xFF agus bratach marcóra ina dhiaidh sin chun an cineál marcóra a léiriú. Tá an pálasta agus an marcóir ina dhiaidh sin difriúil de réir an chineáil marcóra. Tá na cineálacha marcóirí coitianta JPEG mar atá liostaithe thíos:

|Ainm Gearr|Bearta|Ualach Pá|Ainm|Tuairimí
---|---|---|---|---|
|SOI|0xFF, 0xD8|níl ar bith|Tosú na hÍomhá|
|S0F0|0xFF, 0xC0|méid inathraithe|Tosaigh an Fhráma|
|S0F2|0xFF, 0xC2|méid inathraithe|Tosaigh Fo Fráma|
|DHT|0xFF, 0xC4|méid inathraithe|Sainmhínigh Táblaí Huffman|
|DQT|0xFF, 0xDB|méid inathraithe|Sainmhínigh Tábla(í) Cainníochtaithe|
|DRI|0xFF, 0xDD|4 beart|Sainmhínigh Eatramh Atosaithe|
|SOS|0xFF, 0xDA|méid inathraithe|Tosú an Scan|
|RSTn|0xFF, 0xD//n//(//n//#0..7)|níl ar bith|Atosaigh|
|APPn|0xFF, 0xE//n//|méid inathraithe|Sainiúil don fheidhmchlár|
|COM|0xFF, 0xFE|méid inathraithe|Nóta tráchta|
|EOI|0xFF, 0xD9|níl ar bith|Deireadh na hÍomhá|

Laistigh de na sonraí códaithe eantrópachta, tar éis aon bheart 0xFF, cuireann an t-ionchódóir beart 0x00 isteach roimh an gcéad bheart eile, ionas nach cosúil go bhfuil marcóir ann nach bhfuil aon bheart ann, rud a chuireann cosc ar earráidí frámaithe. Ní mór do dhíchódóirí an beart 0x00 seo a scipeáil. Ní chuirtear an teicníocht seo, ar a dtugtar [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (féach sonraíocht JPEG F.1.2.3) i bhfeidhm ach ar na sonraí códaithe eantrópachta, ní chun sonraí pálasta a mharcáil. Tabhair faoi deara, áfach, go bhfuil roinnt marcóirí dá gcuid féin ag sonraí códaithe eantrópachta; go sonrach na marcóirí Athshocraigh (0xD0 trí 0xD7), a úsáidtear chun smuillí neamhspleácha de shonraí códaithe eantrópachta a leithlisiú chun díchódú comhthreomhar a cheadú, agus tá cead ag ionchódóirí na marcóirí Athshocraigh a chur isteach go rialta (cé nach ndéanann gach ionchódóir é seo).

