{
  "date": "2019-12-10",
  "keywords": [
"XLTX",
"comhad",
"síneadh",
"formáid comhaid",
"Excel Oscailte XML",
"Scarbhileog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Do threoir formáid comhaid le fios a bheith agat cad is comhad XLTX agus APIs ann ar féidir leo iad a chruthú agus a oscailt.",
  "title": "Cad is comhad XLTX ann?",
  "linktitle": "XLTX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-gax"
}
},
  "lastmod": "2019-12-10"
}

## Cad is comhad XLTX ann?

Is ionann comhaid le síneadh .xltx agus comhaid Teimpléad Microsoft Excel atá bunaithe ar shonraíochtaí formáid comhaid Office OpenXML. Úsáidtear é chun comhad caighdeánach teimpléid a chruthú ar féidir a úsáid chun comhaid [XLSX](/spreadsheet/xlsx/) a ghiniúint a thaispeánann na socruithe céanna agus atá sonraithe sa chomhad XLTX.

## Stair Ghearr

Go luath sa bhliain 2000, chinn Microsoft an t-athrú a dhéanamh chun freastal ar an gcaighdeán le haghaidh **Office Open XML**. Aithníodh doiciméid, de chineálacha éagsúla, faoin gCaighdeán nua seo trí X a chur i gceangal lena gcuid síntí, áit a raibh X do XML. Faoi 2007, tháinig an fhormáid comhaid nua seo chun bheith ina cuid d’Oifig 2007 agus leantar ar aghaidh léi sna leaganacha nua de Microsoft Office freisin. Tá buntáistí breise ag an gcineál comhaid nua maidir le méideanna beaga comhaid, níos lú athruithe truaillithe agus léiriú íomhánna dea-fhormáidithe.

## Sonraíochtaí Formáid Comhaid XLTX

Tá comhaid XLTX bunaithe ar fhormáid comhaid Office OpenXML agus úsáideann XML agus [ZIP](/compression/zip/) chun méid comhaid a laghdú. Cruthaíodh é le scaoileadh Microsoft Office 2007 chun formáid comhaid dhénártha XLT a athsholáthar. Cosúil le XLTX, is féidir formáid comhaid XLT a úsáid chun comhaid [XLS](/spreadsheet/xls/) a chruthú trí úsáid a bhaint as Microsoft Excel 2003 agus 2007. Is féidir iad seo a oscailt le Microsoft Excel trí chliceáil faoi dhó ar an gcomhad. Is féidir eagraíocht na gcomhad i bhformáid comhaid XLTX a fheiceáil tríd an gcomhad a athainmniú go ZIP agus ansin a bhfuil ann a bhaint go diosca.

### [Ábhar_Cineálacha].xml ###

Is é seo an t-aon chomhad a fhaightear ag an mbonnleibhéal nuair a bhaintear an zip. Liostaíonn sé na cineálacha ábhair le haghaidh páirteanna laistigh den phacáiste. Déantar tagairt do gach tagairt do na comhaid XML atá sa phacáiste sa chomhad XML seo.

### \_rels (Fillteán) ###

Is é seo an fillteán Relationships ina bhfuil comhad XML amháin a stórálann na caidrimh ar leibhéal an phacáiste. Tá naisc chuig na príomhchodanna de chomhaid Xltx sa chomhad seo mar URIanna. Sainaithníonn na URIanna seo an cineál caidrimh a bhaineann le gach príomhchuid den phacáiste. Áiríonn sé seo an gaol le doiciméad príomhoifige atá suite mar xl/workbook.xml agus codanna eile laistigh de docProps mar chroí-airíonna leathnaithe.

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


## Tagairtí ##

* [[MS-XLSX] - Formáid Chomhaid .Xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Oifig Oscailte XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


