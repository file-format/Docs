{
  "date": "2019-10-11",
  "keywords": [
"comhad odg",
"Formáid comhaid odg",
"cad is comhad odg ann",
"comhad",
"odg shampla",
"síneadh comhad odg",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid ODG",
  "description": "Foghlaim faoi fhormáid comhaid ODG agus APIanna ar féidir leo comhaid ODG a chruthú agus a oscailt.",
  "linktitle": "ODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-od-gag"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad ODG ann?

Úsáideann an feidhmchlár Draw Apache OpenOffice formáid comhaid ODG chun eilimintí líníochta a stóráil mar íomhá veicteora. Leanann sé na sonraíochtaí formáid comhaid atá bunaithe ar XML atá leagtha amach ag Cur Chun Cinn na gCaighdeán Faisnéise Struchtúrtha (OASIS). Léiríonn ODG líníochtaí mar íomhánna veicteora ag baint úsáide as pointí, línte agus cuair. Chomh maith le OpenOffice, soláthraíonn LibreOffice agus feidhmchláir eile tacaíocht freisin chun oibriú le formáid comhaid ODG. I measc na bhformáidí eile a fhaigheann tacaíocht ó OpenOffice, mar shampla, tá [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) agus [ODS](/spreadsheet/ods/).


## Sonraíochtaí Formáid Comhaid ODG

Tá formáid comhaid ODG bunaithe ar fhormáid OpenDocument atá i bhformáid doiciméad struchtúrtha XML le scéimre dea-shainithe.
Léirítear gach comhpháirt struchtúrach i bhformáid OpenDocument ag eilimint a bhfuil tréithe gaolmhara aici. Tá an struchtúr bunaithe ar XML coitianta do gach cineál doiciméad mar doiciméad téacs, scarbhileog nó comhad líníochta. Is féidir stíleanna éagsúla a bheith i ndoiciméad. Tá na heilimintí seo a leanas i struchtúr comhaid OpenDocument.
  * Fréamh Doiciméad
  * Meiteashonraí Doiciméad
  * Eilimint Coirp agus cineálacha Doiciméad
  * Socruithe Feidhmchláir
  * Scripteanna
  * Dearbhuithe Cló Aghaidh
  * Stíleanna
  * Stíleanna agus Leagan Amach Leathanach

##  Fréamhacha an Doiciméid ##

Cuimsíonn buneilimint doiciméid an doiciméad iomlán agus is í an phríomheilimint í de chomhad i bhformáid OpenDocument. Tá na cineálacha céanna fréamhacha doiciméad infheidhme maidir le gach cineál doiciméad amhail téacs, doiciméid, scarbhileoga agus doiciméid líníochta.

### Eilimintí Fréamhacha ###
Is ionann doiciméad XML amháin agus a fhréamhghné féin. Seo a leanas na cúig fhréamhghné tacaithe éagsúla.

`<office:document> ` - Doiciméad oifige a chomhlánú i ndoiciméad singleXML.
`<office:document-content> ` - Ábhar doiciméad agus stíleanna uathoibríocha a úsáidtear san ábhar.
`<office:document-styles> ` - Stíleanna a úsáidtear in ábhar an doiciméid agus stíleanna uathoibríocha a úsáidtear sna stíleanna féin.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` - Socruithe a bhaineann go sonrach le feidhmchlár, amhail méid na fuinneoige nó faisnéis an phrinéara.

### Meiteashonraí Doiciméad ODG ###
The OpenDocument contains all metadata elements in the \<office:meta> element. This general information about a document is contained at the start of the document and applications can update multiple instances of the same elements.

### Eilimint Coirp agus Cineálacha Doiciméad ###
Léiríonn an comhlacht doiciméad an cineál ábhair atá sa doiciméad ag baint úsáide as an eilimint cineál doiciméid. Is iad na cineálacha doiciméad seo:
  * doiciméid téacs
  * doiciméid a tharraingt
  * doiciméid cur i láthair
  * doiciméid scarbhileog
  * doiciméid cairte
  * doiciméid íomhá

### Socruithe Feidhmchláir ###
The settings for office applications represent different settings that are related to the document configuration or visual appearance of the document. Each category is represented by a `<config:config-item-set>`. Examples of such setting categories include:
  * Socruithe doiciméid m.sh. printéir réamhshocraithe
  * Amharc ar Shocruithe m.sh. leibhéal súmáil

### Scripteanna ###
It is common for a document to contain several scripts. Each script in an OpenDocument file is represented by an `<office:script>` element. These script elements are contained in a single `<office:scripts>` element. Scripts do not update a document while the document is loading.
### Dearbhuithe Cló Aghaidh ###

Tá faisnéis i ndearbhú aghaidh cló faoi na clónna a úsáideann údar doiciméid. Cuidíonn an fhaisnéis seo leis na clónna seo a aimsiú ar chórais eile.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Stíleanna ###
Tacaíonn an fhormáid OpenDocument leis na stíleanna seo a leanas.

`Stíleanna Coiteanna` - Tagraítear do léirithe XML stíleanna dá leithéid mar stíleanna
`Stíleanna Uathoibríocha` - Tá airíonna formáidithe ann a shanntar do réad cosúil le mír i gcomhéadan úsáideora doiciméad.
`Stíleanna Mater` - stíl choiteann ina bhfuil faisnéis faoi fhormáidiú agus ábhar breise a thaispeántar le hábhar an doiciméid nuair a chuirtear an stíl i bhfeidhm. Sampla de stíl mháistir is ea leathanaigh mháistir.

## Tagairtí ##
  * [Formáid Doiciméad Oscailte OASIS le haghaidh Feidhmchláir Oifige](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
  * [Formáid OpenDocument - Vicipéid](https://en.wikipedia.org/wiki/OpenDocument)

