{
  "date": "2019-10-11",
  "keywords": [
"comhad dcm",
"formáid comhaid dcm",
"cad is comhad dcm ann",
"comhad",
"sampla dcm",
"síneadh comhad dcm",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid DCM - Comhad Faisnéise Digiteach Míochaine",
  "description": "Foghlaim faoi fhormáid comhaid DCM agus APIanna ar féidir comhaid DCM a chruthú agus a oscailt.",
  "linktitle": "DCM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dc-gam"
}
},
  "lastmod": "2021-07-03"
}

## Cad is comhad DCM ann?

Is ionann comhaid le síneadh .dcm agus íomhá dhigiteach a stórálann faisnéis leighis othar ar nós MRIanna, scananna CT agus íomhánna ultrafhuaime. Úsáideann comhaid DCM formáid comhaid íomhá [DICOM](/image/dicom/) (Íomháíocht Dhigiteach agus Cumarsáid sa Leigheas) agus is féidir faisnéis othar a áireamh le haghaidh tagartha. D'fhorbair [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) é agus bhí sé i gceist formáid an chomhaid íomháithe a chaighdeánú chun íomhánna leighis a dháileadh agus a fheiceáil.

## Formáid Chomhaid DCM

Stórálann comhaid DCM faisnéis i bhformáid íomhá DICOM. Stórálann na comhaid seo an Tacar Sonraí, ar faisnéis í an fhíorshaol, a sheasann do chás SOP a bhaineann le DICOM IOD. Stóráiltear Faisnéis Meta Comhad DICOM sa chomhad agus leanann sruth beart an tacair sonraí iarbhír.

### Eolas Meta Comhad DICOM ##

Áirítear i ngach comhad DICOM ceanntásc faisnéise aitheantais don tacar sonraí inchamhlaithe atá comhdhéanta de:
   * Réamhfhocal Comhad 128 beart
   * Réimír 4 bheart DICOM
   * Eilimintí Meta Comhad

Tá an ceanntásc seo riachtanach do gach comhad DICOM.

### Eilimintí Meta Comhad ###
|Ainm Tréith|Clib|Cineál| Cur Síos Tréith
---|---|---|---|
|Brollach an Chomhaid|Gan Chlib nó Réimsí Fad|1|Réimse seasta 128 beart ar fáil do Phróifíl Feidhmchláir nó d'úsáid shonraithe chur chun feidhme. Mura n-úsáidtear Próifíl Feidhmchláir nó cur chun feidhme sonrach, socrófar gach beart go 00H. Ní bheidh Léitheoirí Tacaithe Comhad nó Nuashonróirí ag brath ar ábhar an Bhrollaigh seo chun a chinneadh gur Comhad DICOM nó nach Comhad DICOM é seo.
| Réimír DICOM|Gan Chlib nó Réimsí Fad|1|Ceithre beart ina bhfuil an teaghrán carachtair DICM. Tá sé beartaithe an Réimír seo a úsáid chun a aithint gur Comhad DICOM nó nach Comhad DICOM é seo.
|Fad Grúpa Faisnéise an Chomhaid|(0002,0000)|1|Líon beart tar éis na hEiliminte Meta Comhad seo (deireadh an réimse Luach) suas go dtí agus lena n-áirítear an Eilimint Meta Comhad deiridh den Fhaisnéis Meta Comhad Grúpa 2
|File Meta Information Version|(0002,0001)|1|This is a two byte field where each bit identifies a version of this File Meta Information header. In version 1 the first byte value is 00H and the second value byte value is 01H.Implementations reading Files with Meta Information where this attribute has bit 0 (lsb) of the second byte set to 1 may interpret the File Meta Information as specified in this version of PS3.10. Ní dhéanfar gach giotán eile a sheiceáil.
|Stóráil Meán Aicme SOP Aitheantais Sonraítear AitheantasÚsáideora Aicme SOP a cheadaítear do stóráil meán i PS3.4 - Próifílí Feidhmchláir Stórála Meán.
|Meán-Stóráil AitheantasÚsáideora SOP|(0002,0003)|1|Aithníonn sé go huathúil an Chás SOP a bhaineann leis an Tacar Sonraí a cuireadh sa chomhad agus tar éis an Fhaisnéis Meta Comhaid.
|AitheantasÚsáideora Comhréire Aistrithe|(0002,0010)|1|Aithníonn sé go huathúil an Comhréir Aistrithe a úsáidtear chun an Tacar Sonraí seo a leanas a ionchódú. Ní bhaineann an Comhréir Aistrithe seo leis an bhFaisnéis Meta Comhad.
|Aicme Cur i bhFeidhm AitheantasÚsáideora|(0002,0012)|1|Aithníonn sé go uathúil an cur i bhfeidhm a scríobh an comhad seo agus a bhfuil ann. Soláthraíonn sé sainaithint gan athbhrí ar an gcineál cur chun feidhme a scríobh an comhad deireanach i gcás fadhbanna idirmhalartaithe.
|Ainm an Leagan Forfheidhmithe|(0002,0013)|3|Aithníonn sé leagan d'AitheantasÚsáideora Aicme Cur i bhFeidhm (0002,0012) a úsáideann suas le 16 charachtar den stór.
|Foinse Teideal an Aonáin Feidhmchláir|(0002,0016)|3|An tEintiteas Feidhmchláir DICOM (AE) Teideal an AE a scríobh ábhar an chomhaid seo (nó a nuashonraigh an uair dheireanach é). Má úsáidtear é, ceadaíonn sé foinse na n-earráidí a rianú i gcás fadhbanna idirmhalartaithe meán.
|AitheantasÚsáideora um Fhaisnéis Phríobháideach|(0002,0100)|3|AitheantasÚsáideora de chuid cruthaitheoir na faisnéise príobháidí (0002,0102).
|Faisnéis Phríobháideach|(0002,0102)|1C|Tá Faisnéis Phríobháideach curtha sa Chomhad Meiteaisnéis ann. Déanfar an cruthaitheoir a shainaithint in (0002,0100). Ag teastáil má tá AitheantasÚsáideora Faisnéise Príobháideach (0002,0100) i láthair.

### Ionchamháil Tacar Sonraí ###

Tá Tacar Sonraí amháin i gcomhad DICOM a sheasann do Chás SOP amháin a bhaineann le hAicme SOP amháin. Is é AitheantasÚsáideora Comhréire Aistrithe an Fhaisnéis Meta Comhad DICOM a shaineoidh an Comhréir Aistrithe a úsáidtear chun an Tacar Sonraí a ionchódú.

### Tacaíocht d'Faisnéis Bainistíochta Comhad ###

Soláthraíonn Sraith Formáid na Meán an Fhaisnéis Bainistíochta Comhad seo a leanas más gá do Phróifíl Feidhmchláir DICOM ar leith.

  * Aitheantas úinéara ábhair comhaid

  * Staitisticí rochtana comhad (m.sh., dáta agus am cruthaithe)

  * Rialú rochtana comhaid iarratais

  * Rialú rochtana meán fisiceach (m.sh., cosaint scríobh)

## Tagairtí ##
  * [Caighdeán DICOM](https://www.dicomstandard.org/current/)
  * [Formáid Comhaid DICOM](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

