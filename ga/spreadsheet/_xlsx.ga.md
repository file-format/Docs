{
  "date": "2019-12-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Do threoir formáid comhaid le fios a bheith agat cad is comhad _XLSX agus APIs ann ar féidir comhaid _XLSX a chruthú agus a oscailt.",
  "title": "Cad is comhad _XLSX ann?",
  "linktitle": "_XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-_xls-gax"
}
},
  "lastmod": "2021-11-22"
}

## Cad is comhad _XLSX ann?

Is comhad [XLSX](/spreadsheet/xlsx/) é comhad a bhfuil iarmhír .\_xlsx air agus athainmnítear é ag feidhmchlár éigin eile. Is féidir leis seo tarlú i gcásanna áirithe nuair a bhíonn . ag deireadh ainm an chomhaid. Is féidir na comhaid \_XLSX a oscailt i Microsoft Excel cosúil leis na comhaid XLSX trí iad seo a athainmniú arís mar shíneadh .xlsx.

## _XLSX Formáid Chomhaid - Tuilleadh eolais

The _XLSX files are no different than the XLSX files and use the Open XML standard adopted by Microsoft back in 2000. Roimh XLSX, ba í [XLS](/spreadsheet/xls/) an phríomhfhormáid comhaid a úsáideadh chun oibriú le scarbhileoga Excel chun doiciméid a shábháil i bhformáid dhénártha. Tháinig buntáistí leis an bhformáid comhaid XML nua seo, mar shampla méideanna beaga comhaid, frithsheasmhacht in aghaidh éilliú comhaid, agus léiriú íomhánna dea-fhormáidithe. Tháinig an fhormáid comhaid nua seo atá bunaithe ar XML mar chuid d'Oifig 2007 agus cuirtear i gcrích é sna leaganacha nua de Microsoft freisin.

## \_XLSX Sonraíochtaí Formáid Chomhaid

Toisc gur comhad XLSX é comhad \_XLSX a athainmníodh, tá na sonraíochtaí céanna aige agus a bhí sa bhunchomhad. Níl ann ach comhad cartlainne atá bunaithe ar fhormáid comhaid cartlainne [ZIP](/compression/zip/). Más mian leat a bhfuil sa chartlann seo a fheiceáil, níl le déanamh ach an comhad a athainmniú go síneadh .zip agus é a bhaint as chun féachaint ar chomhaid an leabhair oibre Excel seo. Nuair a bhaintear leabhar oibre bán amach, bíonn na comhaid agus na fillteáin seo a leanas ann.

### [Ábhar_Cineálacha].xml

Is é seo an t-aon chomhad a fhaightear ag an mbonnleibhéal nuair a bhaintear an zip. Liostaíonn sé na cineálacha ábhair le haghaidh páirteanna laistigh den phacáiste. Déantar tagairt do gach tagairt do na comhaid XML atá sa phacáiste sa chomhad XML seo.

### \_rels (Fillteán)

Is é seo an fillteán Relationships ina bhfuil comhad XML amháin a stórálann na caidrimh ar leibhéal an phacáiste. Tá naisc chuig na príomhchodanna de chomhaid Xlsx sa chomhad seo mar URIanna. Sainaithníonn na URIanna seo an cineál caidrimh a bhaineann le gach príomhchuid den phacáiste. Áirítear leis seo an gaol le doiciméad príomhoifige atá suite mar xl/workbook.xml agus codanna eile laistigh de docProps mar réadmhaoine lárnacha agus leathnaithe.

### docProps

Tá airíonna foriomlána an doiciméid san fhillteán seo. Ina measc seo tá sraith de chroí-airíonna, sraith airíonna sínte nó sainfheidhmchláir agus réamhamharc mionsamhail ar an doiciméad. Tá dhá chomhad san fhillteán seo ag leabhar oibre bán, eadhon app.xml agus core.xml. Tá faisnéis mar údar, dáta cruthaithe agus sábháilte, agus modhnaithe sa core.xml. Tá faisnéis ag App.xml faoi ábhar an chomhaid.

### xl (Fillteán)

Is é seo an príomhfhillteán ina bhfuil na sonraí go léir faoi ábhar an leabhair oibre. De réir réamhshocraithe, tá fillteáin seo a leanas aige:

* \_rels

* téama

* bileoga oibre


agus comhaid xml a leanas:

* stíleanna.xml

*leabhar oibre.xml


## Tagairtí

* [MS-XLSX - Formáid Chomhaid .xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Oifig Oscailte XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


