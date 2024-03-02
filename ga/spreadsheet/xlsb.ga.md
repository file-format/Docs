{
  "date": "2019-12-10",
  "keywords": [
"XLSB",
"comhad",
"síneadh",
"formáid comhaid",
"Comhad Scarbhileog Dénártha Excel"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Do threoir formáid comhaid le fios a bheith agat cad is comhad XLSB ann agus APIanna ar féidir leo iad a chruthú agus a oscailt.",
  "title": "Cad is comhad XLSB ann?",
  "linktitle": "XLSB",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-gab"
}
},
  "lastmod": "2019-12-10"
}

## Cad is comhad XLSB ann?

Sonraíonn formáid comhaid XLSB an Formáid Comhad Dénártha Excel, arb é bailiúchán taifead agus struchtúir é a shonraíonn ábhar leabhar oibre Excel. Is féidir táblaí neamhstruchtúrtha nó leathstruchtúrtha d’uimhreacha, téacs, nó an dá uimhir agus téacs, foirmlí, naisc sheachtracha sonraí, cairteacha agus íomhánna a áireamh san ábhar. Murab ionann agus {{ HYPERLINK1}} (atá bunaithe ar fhormáid comhaid Open XML), seasann an XLSB do chomhad leabhar saothair dénártha Excel. Is féidir comhaid XLSB a léamh agus a scríobh go tapa, rud a fhágann go bhfuil siad úsáideach chun oibriú le comhaid mhóra. Is annamh a úsáidtear XLSB chun leabhair oibre a stóráil mar is iad XLSX (agus [XLS](/spreadsheet/xls/) roimhe seo) na formáidí comhaid is coitianta a roghnaíonn úsáideoirí chun leabhair oibre a shábháil. Is féidir é a oscailt le Microsoft Office 2007 agus os a chionn.

## Sonraíochtaí Formáid Chomhaid XLSB ##

The file format specifications for XLSB file format were made public back in 2008 as version 1.0. Ó shin i leith, tá na sonraíochtaí athbhreithnithe arís agus arís eile agus foilsíodh an leagan is déanaí de shonraíochtaí (v 10.0) i mí Aibreáin 2018. Tá na sonraíochtaí ar fáil go poiblí ag Microsoft mar [[MS-XLSB] - Excel Binary File Format specifications](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) agus ba cheart do dhuine ar bith dul i gcomhairle leo le haghaidh léamh nó comhaid a scríobh i bhformáid comhaid XLSB.

## Struchtúr Comhad XLSB ##

Is pacáiste é comhad XLSB atá comhdhéanta de bhailiúchán páirteanna. Tá faisnéis sna codanna seo faoi ábhar leabhar oibre, lena n-áirítear sonraí leabhar saothair agus struchtúr an phacáiste. Tá faisnéis stóráilte ag baint úsáide as taifid dhénártha i gcodanna áirithe, cuid eile mar XML, agus tá faisnéis stóráilte mar shruth beart dénártha i gcodanna eile. Tá nialas nó níos mó réimsí struchtúrtha ina bhfuil sonraí an leabhair oibre i ngach taifead dénártha.

#### Pacáiste ####

Is cartlann [ZIP](/compression/zip/) atá i bpacáiste XLSB agus ní mór cuid amháin den leabhar saothair a bheith ann. Caithfidh an chuid seo a bheith ina sprioc caidrimh sa chuid caidrimh phacáiste seo. Is é an leabhar oibre an chuid tosaigh sa doiciméad XLSB.

#### Cuid ####

Is éard is cuid ann ná sruth beart a bhfuil cineál ábhair gaolmhar aige a shonraíonn nádúr agus cineál an ábhair atá stóráilte sa chuid. Stórálann codanna áirithe faisnéis i bhformáid dhénártha agus stórálann cuid eile faisnéis mar XML. Sa rannán [parts enumeration](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) den doiciméad sonraíochtaí liostaítear na codanna bailí, na cineálacha ábhair agus na gaolmhaireachtaí riachtanacha/roghnacha i measc gach cuid de phacáiste.

#### Gaol ####

Tá nasc idir foinse agus acmhainn sprice. Is féidir le caidreamh a bheith:

**Caidreamh pacáiste:** nuair is cuid an sprioc agus gurb é an pacáiste ina iomláine an fhoinse

**Caidreamh páirt le páirt:** nuair is cuid an sprioc agus gur cuid den phacáiste an fhoinse

**Gaol soiléir:** nuair a dhéantar tagairt d’acmhainn ó inneachar na coda foinseach trí thagairt a dhéanamh don aitreabúid ID luach eiliminte gaoil

Is caidreamh nach bhfuil follasach é **caidreamh intuigthe**

**Caidreamh inmheánach:** nuair is cuid den phacáiste an sprioc

**Caidreamh seachtrach:** nuair is acmhainn sheachtrach nach bhfuil sa phacáiste an sprioc

#### Taifead ####

Is éard is taifead ann ná an bunchloch tógála a úsáidtear chun faisnéis a stóráil faoi ghnéithe i leabhar saothair. Is seicheamh fad athraitheach beart é gach taifead dénártha. Tá trí chomhpháirt i dtaifead dénártha:

* cineál taifead

* méid taifead, agus

* na sonraí taifid a bhaineann go sonrach leis an gcineál taifid sin.


**Cineál Taifid:** Léiríonn an cineál taifid an cineál taifid atá sonraithe ag an taifead. Sonraíonn sé freisin struchtúr na sonraí taifid a bhaineann go sonrach leis an taifead seo. Tá na cineálacha taifead bailí liostaithe sa rannán [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) den doiciméad sonraíochtaí. Ní mór beart amháin nó dhó a bheith sa chineál taifid agus caithfidh sé a bheith níos mó ná nó cothrom le 128 agus níos lú ná 16384.

**Méid na dTaifead:** Sonraíonn méid an taifid líon na mbeart a shonraíonn méid iomlán na sonraí taifid. NÍ MÓR an luach seo a bheith idir aon agus ceithre bheart. NÍ MÓR an luach seo a bheith ina bheart amháin má tá an giotán ard sa bheart íseal cothrom le 0; ar shlí eile, NÍ MÓR an luach seo a bheith níos mó ná beart amháin. Má tá líon na mbeart níos mó ná beart amháin, sonraítear sa ghiotán ard i ngach beart comhleanúnach cé acu an n-úsáidtear beart breise. Más ionann ardghiotán an dara beart agus 1, ansin NÍ MÓR an luach seo tríú beart breise a úsáid. Más ionann ardghiotán an tríú beart agus 1, ansin NÍ MÓR an luach seo ceathrú beart breise a úsáid. NÍ MÓR neamhaird a dhéanamh ar ghiotán ard an cheathrú beart. Is éard atá sa luach na seacht ngiotán ísle de gach beart le chéile. Tá na giotáin is ísle, is lú suntas, sa chéad bheart, agus tá giotán ord níos airde ná an beart roimhe seo i ngach beart comhleanúnach.

**Sonraí Taifead:** Tá réimsí sa chomhpháirt sonraí taifid a fhreagraíonn do chineál taifid ar leith agus a chuimsíonn an chuid eile den taifead. Tá ord agus struchtúr na réimsí le haghaidh cineál áirithe taifid atá liostaithe in Áireamh Taifead sonraithe sa roinn chomhfhreagrach don chineál taifid sin i dTaifid. NÍ MÓR méid iomlán na comhpháirte sonraí taifid a bheith comhionann le méid an taifid. Is féidir luachanna simplí, eagair luachanna, struchtúir roinnt réimsí, eagair réimsí, agus eagair struchtúr a bheith i réimsí sa chomhpháirt sonraí taifid.

#### Sampla Taifead XLSB ####

Sonraíonn an cineál taifid seo a leanas agus méid an taifid taifead **BrtCommentText** a bhfuil méid 200 beart ann:

11111101 00000100 11001000 00000001 [Réimsí Taifead]

The first byte is 11111101, specifying a low value of 125 and that the record type requires a second byte. The second byte is 00000100, specifying a high value of 4 * 128, arb ionann é agus 512. Is é luach an chineáil taifid ná 125 + 512, nó 637, a fhreagraíonn do chineál taifid **BrtCommentText**. Is é 11001000 an chéad bheart eile, ag sonrú luach íseal 72 agus go n-éilíonn an méid taifead an dara beart. Is é an dara beart ná 00000001, ag sonrú luach níos airde de 1 * 128 agus nach bhfuil beart breise ag teastáil ón méid taifead. Is é an méid taifead ná 72 + 128, nó 200, a shonraíonn méid iomlán, i mbeart, den chomhpháirt sonraí taifid. Sonraítear na réimsí sa chomhpháirt sonraí taifid le **BrtCommentText**.

## Tagairtí ##

* [[MS-XLSB] - Formáid Chomhaid Dhénártha Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)


