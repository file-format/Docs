{
  "date": "2019-12-16",
  "keywords": [
"XLS",
"comhad",
"síneadh",
"formáid comhaid",
"Excel",
"Scarbhileog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Do threoir formáid comhaid le fios a bheith agat cad is comhad XLS agus APIs ann ar féidir leo iad a chruthú agus a oscailt.",
  "title": "Cad é formáid comhaid XLS? Foghlaim ó Shaineolaithe Formáid Comhaid!",
  "linktitle": "XLS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-gas"
}
},
  "lastmod": "2019-12-16"
}

## Cad is comhad XLS ann?

Files with XLS extension represent Excel Binary File Format. Such files can be created by Microsoft Excel as well as other similar spreadsheet programs such as OpenOffice Calc or Apple Numbers. File saved by Excel is known as Workbook where each workbook can have one or more worksheets. Data is stored and displayed to users in table format in worksheet and can span numeric values, text data, formulas, external data connections, images, and charts. Applications like Microsoft Excel lets you export workbook data to several different formats including [PDF](/pdf/), [CSV](/spreadsheet/csv/), [XLSX](/spreadsheet/xlsx/), [TXT](/word-processing/txt/), [HTML](/web/html/), [XPS](/page-description-language/xps/), and several others. The XLS file format was replaced with a more open and structured format, XLSX, with the release of Microsoft Excel 2007. The latest versions still provide support for creating and reading XLS files, though XLSX is the first choice of use now.

## Stair Ghearr

XLS was created by Microsoft for use with Microsoft Excel and is also known as Binary Interchange File Format (BIFF). This file type was introduced for the first time by making it part of Excel for Windows in 1987. XLS file format specifications were made public for the first in June 2008 as Revision 1. After that, the specifications were continuously updated and the latest revision available is as of August 2018 that is marked as Revision 8.0. A brief history of different versions of XLS file format is as follow:

* Version 7.0 (released with office 95):  This version of excel was the most robust and faster among all the versions and internal stream rewrites were updated to 32 bits.
* Leagan 8 (scaoileadh le hoifig 97): Tugadh VBA isteach mar theanga chaighdeánach agus ionchorpraíodh lipéid teanga nádúrtha sa leagan seo den chéad uair. Thug sé isteach freisin cúntóir oifige gearrthóg páipéir don chéad uair.

* Leagan 9 (Eisithe leis an Oifig 2000): Ní raibh ach mionathruithe ar Leagan 9 nuair a d’fhéadfadh cúntóir oifige fáiscíní páipéir roinnt rudaí nach raibh indéanta roimhe seo a shealbhú ag an am céanna.

* Leagan 10 (Eisithe le hoifig XP): Ní raibh aon fheabhsú suntasach sa leagan seo.

* Version 11 (Released with office 2003): Major update in version 11, excel 2003 was the introduction of new tables.

## Sonraíochtaí Formáid Chomhaid XLS ##

Socraítear sonraí i gcomhad XLS mar shruthanna dénártha i bhfoirm comhaid chumaisc mar a thuairiscíonn Microsoft i ndoiciméad [MS-CFB]. Data is stored in the compound file by using storages, streams, and substreams that contain information about the content and structure of a workbook, including workbook data such as worksheet definitions. Each stream or substream contains a series of binary records. Each binary record contains zero or more structured fields that contain the workbook data. This section gives a brief overview of XLS File Structure, but for detailed file format specifications, one must consult the [XLS File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx).

#### Sruth agus Foshruth ####

Léirítear leabhar saothair sa sruth leabhar saothair. Léiríonn Foshruthanna gach bileog oibre i leabhar oibre. Ina theannta sin, tá Foshruthán Bileog Cairte, Foshraith Bileog Macra, nó Foshruthán Bileog Dialóige aige a leanann an Foshruth Domhanda. NÍ MÓR gach sruth dénártha nó fo-shruth ina bhfuil sonraí leabhar oibre a scríobh mar shraith de thaifid dhénártha.

#### Taifead ####

Stóráiltear faisnéis faoi ghnéithe i leabhar saothair mar thaifead atá ina sheicheamh beart inathraitheach. Tá na trí chomhpháirt seo a leanas i dtaifead dénártha:

**Cineál Taifead:** Is slánuimhir dhá bheart gan síniú é an cineál taifid a shonraíonn cén cineál faisnéise atá sonraithe sa taifead agus conas a ordaítear agus a struchtúraítear struchtúr na sonraí taifid a bhaineann leis an taifead seo. NÍ MÓR do luachanna cineáil taifead a bheith ina luach ón Áireamh Taifead (cuid 2.3) nó NÍ MÓR don taifead úsáid a bhaint as ailtireacht taifead amach anseo (cuid 2.1.6).

**Méid na dTaifead**: Is slánuimhir dhá bheart gan síniú é méid na dtaifead a shonraíonn comhaireamh beart a shonraíonn méid iomlán na sonraí taifid. NÍ MÓR méid an taifid a bheith níos mó ná nó cothrom le 0 agus NÍ MÓR di a bheith níos lú ná nó cothrom le 8224.

**Sonraí Taifead:** Tá réimsí sa chomhpháirt sonraí taifid a fhreagraíonn do chineál taifid ar leith agus a chuimsíonn an chuid eile den taifead. Sonraítear ord agus struchtúr na réimsí do chineál áirithe taifid sa roinn chomhfhreagrach don chineál taifid sin. NÍ MÓR méid na comhpháirte sonraí taifid a bheith comhionann le méid an taifid. Is féidir luachanna simplí, eagair luachanna, struchtúir roinnt réimsí, eagair réimsí, agus eagair struchtúr a bheith i réimsí sa chomhpháirt sonraí taifid.

#### Tábla Cille ####

Is iad cealla na bloic bhunúsacha de leabhar oibre a stórálann inneachar an leabhair oibre cosúil le téacs, foirmlí agus sonraí uimhriúla. Coinníonn cealla taifead ar na sonraí stóráilte trí struchtúr sonraí ar a dtugtar an Tábla Cille. Stóráiltear an Tábla Cille féin sa seicheamh taifead a chloíonn leis na rialacha CELLTABLE atá sainmhínithe sa doiciméad sonraíochtaí. Is éard atá ann ná sraith de bhlocanna rónna ina bhfuil na sraitheanna socraithe i mbloic rónna. Tá sraitheanna i ngach bloc rónna ón gcéad ró ina bhfuil sonraí go dtí an tsraith dheireanach ina bhfuil sonraí.

Déantar sonraí nó formáidiú ró a shábháil i dtaifead Rae do gach bloc rónna. Tá taifead á léiriú ag gach cill ina bhfuil sonraí nó formáidiú cille aonair. Is féidir formáidiú a bhaineann le cill a dhíorthú ó fhormáidiú cille aonair, formáidiú ró, formáidiú colúin, nó formáid réamhshocraithe cille. Is é an t-ord tosaíochta le haghaidh formáidithe ná formáidiú cille aonair leis an tosaíocht is airde, ina dhiaidh sin formáidiú ró, agus ansin formáidiú colúin, agus ansin an fhormáid réamhshocraithe cille. Ní shábháiltear cealla nach bhfuil sonraí iontu agus nach bhfuil formáidiú aonair iontu.

#### Foirmlí ####

Is éard is foirmle ann seicheamh luachanna, tagairtí cille, ainmneacha, feidhmeanna, nó oibreoirí i gcill a tháirgeann luach nua le chéile. Stóráiltear foirmlí i léiriú tokenized ar a dtugtar nathanna parsáilte. Tiontaítear slonn parsáilte ina fhoirmle théacsúil ag am rite le haghaidh taispeáint agus eagarthóireacht úsáideora. Sonraítear foirmlí cille leis an taifead Foirmle. Sonraítear foirmlí Eagar sa taifead Eagar. Sonraítear foirmlí roinnte ag taifead ShrFmla.

#### Cairteacha ####

Sonraíonn an chairtbhileog cairt, grafaic a thaispeánann sonraí nó na gaolta idir tacair sonraí i bhfoirm amhairc, agus taisce sonraí cairte, cóip áitiúil de na sonraí a úsáidtear i sonraí na cairte in easnamh nó má tá naisc chuig seachtracha tá foinsí sonraí briste. Sonraíonn an chairt grúpaí ais amháin nó dhá-ais, sraith aiseanna a bhfuil sonraí na cairte breactha ina n-aghaidh, agus an tsraith, línte treochta agus barra earráide sonraithe sa chairt. Sonraíonn gach grúpa aisghrúpa aon go ceithre ghrúpa cairte a shonraíonn an cineál léirshamhlaithe a úsáidtear chun na sonraí a thaispeáint. Sonraíonn gach sraith, treolíne, agus barra earráide grúpa cairte a bhfuil baint aige leis.

#### Meiteashonraí ####

Is sonraí breise iad meiteashonraí a bhaineann le cill áirithe nó lena hinneachar. Déantar meiteashonraí a thaifeadadh in BIFF8 chun críocha fairsingithe amach anseo amháin.

#### Pivot Tables ####

Is meicníocht é PivotTable chun sonraí foinseacha a achoimriú chun forbhreathnú a fháil ar dháileadh na sonraí sin. I PivotTable, déantar réimsí de na colúin is infheidhme de na sonraí foinseacha ar féidir iad a úsáid chun sonraí a achoimriú. Nuair is sonraí foinseacha OLAP iad sonraí foinseacha an PivotTable, déantar ordlathas OLAP agus roinnt eintiteas OLAP eile ina réimsí sa PivotTable.
Tá dhá mhórchuid ag PivotTable, PivotCache agus radharc PivotTable. Is féidir le tuairimí iolracha PivotTable a bheith bunaithe ar PivotCache amháin neamh-OLAP.

#### Stíleanna ####

Déanann an forbhreathnú seo cur síos ar conas a shonraítear faisnéis maidir le formáidiú agus cosaint do chealla i mbileog (1). Tá formáidiú cille comhdhéanta de roinnt tacair airíonna:

* Airíonna cló (trom, iodálach, dath an chló, clómhéid, srl…)

* Airíonna líonadh (dath tulra, dath cúlra, patrún, grádán, srl ...)

* Airíonna ailínithe (clé, lár, ailíniú ar dheis, etc...)

* Airíonna teorann (clé, ar dheis, barr, bun, tiubh nó tanaí, dath, srl…)

* Airíonna formáidithe uimhreach (dáta, am, líon na n-ionad deachúlacha, srl…)

* Airíonna cosanta (faoi ghlas, i bhfolach, srl…)


Déanann na hairíonna seo, ina n-iomláine, cur síos ar conas a thaispeántar agus a phriontáiltear cill ar leith.

## Tagairtí ##

* [[MS-XLS] - Struchtúr Formáide Comhad Dénártha Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [[MS-CFB] - Formáid Chomhaid Dhénártha Comhdhúile](https://msdn.microsoft.com/en-us/library/dd942138.aspx)


