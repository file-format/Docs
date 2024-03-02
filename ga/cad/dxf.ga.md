{
  "date": "2020-03-16",
  "keywords": [
"Comhad DXF",
"Formáid Chomhaid",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid DXF agus APIs ar féidir leo comhaid DXF a chruthú agus a oscailt.",
  "title": "Formáid Comhaid DXF",
  "linktitle": "DXF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dx-gaf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad DXF ann?

Is léiriú sonraí clibeáilte de chomhad líníochta AutoCAD é DXF, Formáid Idirmhalartaithe Líníochta, nó Formáid Malartaithe Líníochta. Tá uimhir slánuimhir réimír ag gach eilimint sa chomhad ar a dtugtar cód grúpa. Seasann an grúpchód seo go hiarbhír don eilimint a leanann agus léiríonn sé an bhrí atá le eilimint sonraí do chineál áirithe réad. Is féidir le DXF beagnach gach faisnéis atá sonraithe ag an úsáideoir a léiriú i gcomhad líníochta.

D'fhorbair Autodesk formáid comhaid DXF mar fhormáid comhaid sonraí CAD le haghaidh idir-inoibritheachta sonraí idir AutoCAD agus feidhmchláir eile. Mar sin, is féidir sonraí a allmhairiú ó fhormáidí eile go DXF go AutoCAD de réir na sonraíochtaí idir-inoibritheachta formáid comhaid DXF.

## Stair Ghearr ##


The history of DXF file format dates back to 1982 when it was introduced as part of AutoCAD 1.0. Ní thacaíonn leaganacha tosaigh AutoCAD ach le formáid comhaid ASCII de DXF. Le scaoileadh 10 de AutoCAD (agus os a chionn) i 1988, tugadh isteach tacaíocht don dá ASCII chomh maith le formáid comhaid dénártha DXF i AutoCAD. Sna céimeanna tosaigh, níor roinn Autodesk aon sonraíochtaí formáid comhaid agus mar gheall air seo, ní raibh sé éasca comhaid DXF a allmhairiú i gceart. Mar sin féin, foilsíonn Autodesk na sonraíochtaí DXF anois agus tá siad ar fáil don phobal i gcoitinne.

## Sonraíochtaí Formáid Chomhaid ##

Úsáideann formáid comhaid DXF an cód grúpa agus péirí luacha chun an t-ábhar a shocrú ina rannóga. Tá gach cuid comhdhéanta de thaifid ina bhfuil cód grúpa agus mír sonraí i ngach taifead. Tá gach cód grúpa agus luach ar a líne féin sa chomhad DXF. Tosaíonn gach roinn le cód grúpa 0 agus an teaghrán, ROINN, ina dhiaidh sin. Ina dhiaidh sin tá cód grúpa 2 agus sreang a léiríonn ainm na coda (mar shampla, ROINN 1). Tá gach cuid comhdhéanta de chóid ghrúpa agus de luachanna a shainíonn na heilimintí atá ann. Críochnaíonn cuid le 0 agus an teaghrán ENDSEC ina dhiaidh.

Measann formáid comhaid DXF rudaí atá difriúil ó aonáin. Níl aon léiriú grafach ar réad anseo ach tá sé ag aonáin. Mar sin, tagraítear d’iontrálacha i DXF mar réada grafacha agus tagraítear d’oibiachtaí réada mar réada neamhghrafacha. Tá Aonáin sna codanna BLOCK agus ENTITIES de chomhad DXF agus is ionann úsáid na gcód grúpa sa dá chuid seo. Léiríonn an chéad ghrúpa 0 eile deireadh aonáin, a thosaíonn an chéad eintiteas eile nó a léiríonn deireadh na rannóige.

### Struchtúr Comhad ###

Socraítear codanna i gcomhad DXF san ord seo a leanas:

|Section|Basic description
---|---|
|Ceanntásc|Tá faisnéis ghinearálta faoin líníocht sa chuid seo. Tá sé cosúil le feidhmiúlacht na Socruithe i do ghuthán, ina bhfuil na hathróga éagsúla a bhaineann leis an líníocht agus na luachanna a bhaineann leis. Mar shampla, saineoidh an rannán Ceanntásc an leagan AutoCAD a úsáideann an comhad DXF (an athróg $ACADVER) nó an t-aonad a úsáidtear chun uillinneacha sa chomhad a thomhas (an athróg $AUNITS)
|Ranganna|Tá an t-eolas sa rannán RANGANNA d'aicmí arna sainiú ag feidhmchlár a bhfuil a gcásanna le fáil sna ranna BLOCKS, ENTITIES, and OJECTS den bhunachar sonraí.
|Táblaí|Tá sainmhínithe sa chuid seo ar roinnt táblaí éagsúla, agus tá roinnt iontrálacha siombailí difriúla i ngach ceann acu. Mar shampla sainmhíníonn an tábla [line type](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) (LTYPE) patrún na ndashes, na poncanna, an téacs agus na siombailí sa chomhad DXF agus conas a dhéantar iad a scála. Seo liosta iomlán de na táblaí atá le fáil sa chuid seo:<ul><li> Tábla ID Iarratais (APPID).</li><li> Tábla Taifead Bloc (BLOCK_RECORD).</li><li> Tábla Toise Stíl (DIMSTYPE).</li><li> Ciseal (LAYER) tábla</li><li> Cineál líne (LTYPE) tábla</li><li> Stíl téacs (STÍL) tábla</li><li> Tábla an Chórais Chomhordaithe Úsáideoirí (UCS).</li><li> Féach ar (VIEW) tábla</li><li> Tábla cumraíochta Viewport (VPORT).</li></ul>
|Bloic|Tá na réada grafacha agus na haonáin líníochta a dhéanann suas gach blocthagairt sa líníocht sa chuid seo.
|Eintitis|Tá na sonraí oibiachta iarbhír agus aonáin ghrafacha na líníochta sa roinn seo. D’fhéadfadh sonraí amh a bheith san áireamh leis seo – mar shampla, sainítear aonán ciorcail de réir a thiús, a lárphointe, a gha agus a threo easbhrúite.
|Oibiachtaí|Anseo, gheobhaidh tú na codanna neamhghrafacha den líníocht. Mar shampla, tá foclóirí AutoCAD stóráilte anseo.

## Tagairtí ##

* [DXF File Specifications](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF le Vicipéid](https://ga.wikipedia.org/wiki/AutoCAD_DXF)


