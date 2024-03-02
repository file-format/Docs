{
  "date": "2019-12-10",
  "keywords": [
"XLSX",
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
  "description": "Foghlaim faoi cad is comhad XLSX agus APIs ann ar féidir comhaid XLSX a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid XLSX - Cad is comhad XLSX ann?",
  "linktitle": "XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-gax"
}
},
  "lastmod": "2019-12-10"
}

## Cad is comhad XLSX ann?

**XLSX** is well-known format for Microsoft Excel documents that was introduced by Microsoft with the release of Microsoft Office 2007. Bunaithe ar struchtúr arna eagrú de réir na gCoinbhinsiúin um Phacáistiú Oscailte mar atá leagtha amach i [Part 2](https://www.ecma-international.org/publications-and-standards/standards/ecma-376/) den chaighdeán OOXML ECMA-376, is pacáiste zip é an fhormáid nua ina bhfuil roinnt comhad XML. Is féidir an bunstruchtúr agus na comhaid a scrúdú ach an comhad .xlsx a dhísipeáil.

## Stair Achomair ar Fhormáid Chomhaid XLSX

XLSX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Roimhe XLSX, ba í [XLS](/spreadsheet/xls/) an fhormáid chomhaid choitianta a úsáideadh, formáid dhénártha íon. Tá buntáistí breise ag an gcineál comhaid nua maidir le méideanna beaga comhaid, níos lú athruithe truaillithe agus léiriú íomhánna dea-fhormáidithe. Go luath sa bhliain 2000, chinn Microsoft an t-athrú a dhéanamh chun freastal ar an gcaighdeán le haghaidh **Office Open XML**. Faoi 2007, tháinig an fhormáid comhaid nua seo chun bheith ina cuid d’Oifig 2007 agus leantar ar aghaidh léi sna leaganacha nua de Microsoft Office freisin.

## Sonraíochtaí Formáid Comhaid XLSX

Tá an [XLSX file format specifications](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) oifigiúil ar fáil ar líne ó Microsoft. D'fhonn a fheiceáil cad atá taobh istigh den chomhad XLSX, níl le déanamh ach é a athainmniú go comhad {{ HYPERLINK2}} tríd an síneadh a athrú agus ansin é a bhaint as chun féachaint ar chomhaid an leabhair oibre Excel seo. Nuair a bhaintear leabhar oibre bán amach, bíonn na comhaid agus na fillteáin seo a leanas ann.

### [Ábhar_Cineálacha].xml ###

Is é seo an t-aon chomhad a fhaightear ag an mbonnleibhéal nuair a bhaintear an zip. Liostaíonn sé na cineálacha ábhair le haghaidh páirteanna laistigh den phacáiste. Déantar tagairt do gach tagairt do na comhaid XML atá sa phacáiste sa chomhad XML seo.

### \_rels (Fillteán) ###

Is é seo an fillteán Relationships ina bhfuil comhad XML amháin a stórálann na caidrimh ar leibhéal an phacáiste. Tá naisc chuig na príomhchodanna de chomhaid Xlsx sa chomhad seo mar URIanna. Sainaithníonn na URIanna seo an cineál caidrimh a bhaineann le gach príomhchuid den phacáiste. Áirítear leis seo an gaol le doiciméad príomhoifige atá suite mar xl/workbook.xml agus codanna eile laistigh de docProps mar réadmhaoine lárnacha agus leathnaithe.

### docProps ###

Tá airíonna foriomlána an doiciméid san fhillteán seo. Ina measc seo tá sraith de chroí-airíonna, sraith airíonna sínte nó sainfheidhmchláir agus réamhamharc mionsamhail ar an doiciméad. Tá dhá chomhad san fhillteán seo ag leabhar oibre bán, eadhon app.xml agus core.xml. Tá faisnéis mar údar, dáta cruthaithe agus sábháilte, agus modhnaithe sa core.xml. Tá faisnéis ag App.xml faoi ábhar an chomhaid.

### xl (Fillteán) ###

Is é seo an príomhfhillteán ina bhfuil na sonraí go léir faoi ábhar an leabhair oibre. De réir réamhshocraithe, tá fillteáin seo a leanas aige:

* \_rels

* téama

* bileoga oibre


agus comhaid xml a leanas:

* stíleanna.xml

*leabhar oibre.xml


## Sampla Formáid XLSX ##


I gcás gach bileog oibre Excel atá i leabhar oibre, tá comhad XML amháin. Is féidir leat na comhaid XML seo a fháil i bhfillteán xl/bileoga oibre. Eagraítear an fhaisnéis go léir atá i mbileog oibre i gcodanna éagsúla sa chomhad XML. Scrúdóimis bileog oibre shamplach ó leabhar saothair a thaispeántar san íomhá seo a leanas.

{{< figure src="../XLSX file format.png" alt="Formáid Chomhaid XLSX" >}}

Mar is léir, tá a bhfuil sa bhileog oibre seo i gcealla A1 go B2 agus in íomhá. Ina theannta sin, is é cill G13 an chill ghníomhach sa bhileog oibre faoi láthair. Anois, déanaimis scrúdú ar an gcomhad xl/sheets/sheet1.xml chun a fheiceáil conas a léirítear an fhaisnéis seo sa chomhad XML. Tá a bhfuil sa chomhad XML seo mar a thaispeántar thíos.

{{< figure src="../XLSX File Format Details.png" alt="Formáid Comhaid XPS" >}}

1. Cuirtear dath téama ar an gcluaisín. Tá sé luaite sa chomhad XML le clib<tabColor> ag leanúint leis an téama id.
1. Tá an luach tabRoghnaithe socraithe go 1 a thaispeánann gurb é seo an leathán roghnaithe
1. Mar atá le feiceáil sa chéad íomhá thuas, is cill ghníomhach é cill G13 sa bhileog oibre a luaitear sa chomhad XML freisin.
1. Léiríonn an táb sheetData na sonraí atá sa bhileog oibre. Mar sin féin, is féidir leat a fheiceáil nach bhfuil bunábhar na bileoige oibre in áit ar bith sa chuid seo. Tá sé seo amhlaidh toisc go ndéantar tagairt indíreach don téacs ó bhileog XML sharedStrings. Cinntíonn an nascadh seo nach ndéantar gach téacs a shábháil ach uair amháin agus gur féidir tagairt a dhéanamh dó arís chun spás a shábháil.
1. Déantar tagairt don íomhá mar atá le feiceáil ag an tagairt id rId2

## Cur

An bhfuil ort rud éigin a roinnt faoi fhormáidí comhaid XLSX nó Scarbhileog? Is féidir leat do thorthaí a phostáil sa rannán [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet).

## Tagairtí

* [[MS-XLSX] - Formáid Chomhaid XLSX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)

* [Oifig Oscailte XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


