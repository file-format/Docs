{
  "date": "2019-12-10",
  "keywords": [
"XLTM",
"comhad",
"síneadh",
"formáid comhaid",
"Excel Oscail XML Macra",
"Scarbhileog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Do threoir formáid comhaid le fios a bheith agat cad is comhad XLTM agus APIs ann ar féidir leo iad a chruthú agus a oscailt.",
  "title": "Cad is comhad XLTM ann?",
  "linktitle": "XLTM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-gam"
}
},
  "lastmod": "2019-12-10"
}

## Cad is comhad XLTM ann?

Léiríonn an síneadh comhad XLTM comhaid a ghineann Microsoft Excel mar chomhaid teimpléid Macra-chumasaithe. Tá comhaid XLTM cosúil le [XLTX](/spreadsheet/xltx/) i struchtúr seachas an ceann is déanaí ní thacaíonn sé le comhaid teimpléid a chruthú le macraí. Úsáidtear comhaid teimpléid den sórt sin chun leagan amach, formáidiú, agus socruithe eile a ghiniúint agus a shocrú mar aon leis na macraí chun comhaid XLSX den chineál céanna a chruthú ansin.

## Stair Ghearr ##

Go luath sa bhliain 2000, chinn Microsoft an t-athrú a dhéanamh chun freastal ar an gcaighdeán le haghaidh **Office Open XML**. Aithníodh doiciméid, de chineálacha éagsúla, faoin gCaighdeán nua seo trí X a chur i gceangal lena gcuid síntí, áit a raibh X do XML. Faoi 2007, tháinig an fhormáid comhaid nua seo chun bheith ina cuid d’Oifig 2007 agus leantar ar aghaidh léi sna leaganacha nua de Microsoft Office freisin. Tá buntáistí breise ag an gcineál comhaid nua maidir le méideanna beaga comhaid, níos lú athruithe truaillithe agus léiriú íomhánna dea-fhormáidithe.

## Sonraíochtaí Formáid Chomhaid XLTM ##

Tá comhaid XLTM bunaithe ar fhormáid comhaid Office OpenXML agus úsáideann XML agus [ZIP](/compression/zip/) chun méid comhaid a laghdú. Is féidir iad seo a oscailt le Microsoft Excel ach cliceáil faoi dhó ar an gcomhad. Is féidir eagraíocht na gcomhad i bhformáid comhaid XLTM a fheiceáil tríd an gcomhad a athainmniú go ZIP agus ansin a bhfuil ann a bhaint go diosca.

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

* [Formáid Comhaid MS-XLSX]( https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Oifig Oscailte XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


