{
  "date": "2019-12-13",
  "keywords": [
"Comhad pptx",
"Formáid comhaid pptx saor in aisce,",
"Cad is comhad pptx ann",
"comhad",
"sampla pptx",
"Síneadh comhad pptx saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid PPTX agus APIanna ar féidir leo comhaid PPTX a chruthú agus a oscailt.",
  "title": "PPTX - Formáid Chomhaid Léirithe PowerPoint",
  "linktitle": "PPTX",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-ppt-gax"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad PPTX ann?

Is comhaid léirithe iad comhaid a bhfuil síneadh PPTX acu a cruthaíodh le feidhmchlár móréilimh Microsoft PowerPoint. Murab ionann agus an leagan roimhe seo den fhormáid comhaid léirithe PPT a bhí dénártha, tá an fhormáid PPTX bunaithe ar fhormáid comhaid léirithe XML oscailte Microsoft PowerPoint. Is éard atá i gcomhad léirithe ná bailiúchán sleamhnán inar féidir le gach sleamhnán a bheith comhdhéanta de théacs, íomhánna, formáidiú, beochan, agus meáin eile. Cuirtear na sleamhnáin seo i láthair don lucht féachana i bhfoirm taispeántais sleamhnán le socruithe saincheaptha cur i láthair.

## Stair Ghearr

PPTX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Roimh PPTX, ba é PPT an fhormáid chomhaid choitianta a úsáideadh, formáid dhénártha íon. Tá buntáistí breise ag an gcineál comhaid nua maidir le méideanna beaga comhaid, níos lú athruithe truaillithe agus léiriú íomhánna dea-fhormáidithe. Go luath sa bhliain 2000, chinn Microsoft an t-athrú a dhéanamh chun freastal ar an gcaighdeán le haghaidh **Office Open XML**. Faoi 2007, tháinig an fhormáid comhaid nua seo chun bheith ina cuid d’Oifig 2007 agus leantar ar aghaidh léi sna leaganacha nua de Microsoft Office freisin.

## Sonraíochtaí Formáid Comhaid PPTX

Comhaid a ghintear leis an oifig Is éard atá i bhformáid comhaid XML Oscailte ná bailiúchán de chomhaid XML mar aon le comhaid eile a sholáthraíonn naisc idir na comhábhair go léir. Is cartlann chomhbhrúite é an bailiúchán seo ar féidir a bhaint as chun féachaint ar a bhfuil ann. Chun é sin a dhéanamh, níl le déanamh ach an síneadh comhad PPTX a athainmniú le zip agus bain amach é chun a bhfuil ann a bhreathnú (Féach [PPTX file format specifications](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f) le Microsoft).

Caitheann na codanna seo a leanas roinnt solais ar gach ceann díobh seo.

### [Ábhar_Cineálacha].xml

Is é seo an t-aon chomhad a fhaightear ag an mbonnleibhéal nuair a bhaintear an zip. Liostaíonn sé na cineálacha ábhair le haghaidh páirteanna laistigh den phacáiste. Déantar tagairt do gach tagairt do na comhaid XML atá sa phacáiste sa chomhad XML seo. Seo a leanas cineál ábhair do chuid sleamhnáin:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Más gá páirteanna nua a chur leis an bpacáiste, is féidir é a dhéanamh tríd an gcuid nua a chur leis agus aon chaidreamh laistigh de na comhaid .rels a nuashonrú. Ní mór a choinneáil i gcuimhne go gcaithfear an Content_Types.xml a nuashonrú freisin le haghaidh athrú dá leithéid.

### \_rels (Fillteán) ###

Coinníonn an chuid caidrimh idir na codanna eile agus na hacmhainní lasmuigh den phacáiste. Tá comhad XML amháin san fhillteán Caidrimh a stórálann na caidrimh ar leibhéal an phacáiste. Tá naisc chuig na príomhchodanna de na comhaid PPTX sa chomhad seo mar URIanna. Sainaithníonn na URIanna seo an cineál caidrimh a bhaineann le gach príomhchuid den phacáiste. Áirítear leis seo an gaol le doiciméad príomhoifige atá suite mar ppt/presentation.xml agus codanna eile laistigh de docProps mar réadmhaoine lárnacha agus leathnaithe.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

Beidh a chuid gaolta féin ag gach cuid den doiciméad atá mar fhoinse gaoil amháin nó níos mó ina bhfaightear gach cuid den ghaolmhaireacht laistigh d'fho-fhillteán \_rels den chuid agus go n-ainmnítear í trí '.rels' a chur i gceangal le hainm an chuid. Tá a chuid caidrimh féin ag an bpríomhchuid ábhar (cur i láthair.xml) (cur i láthair.xml.rels). Tá caidrimh ann le codanna eile den ábhar ar nós slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, chomh maith leis na URIanna le haghaidh naisc sheachtracha.

#### Gaol follasach ####

Maidir le gaol follasach, déantar tagairt d'acmhainn ag baint úsáide as an aitreabúid Id de a<Relationship> eilimint. Is é sin le rá go bhfuil an tAitheantas sna foinsí mapaí díreach chuig ID de mhír chaidrimh, le tagairt shainráite don sprioc.

Mar shampla, d’fhéadfadh hipearnasc mar seo a bheith i sleamhnán:

```
<a:hlinkClick r:id#"rId2">
```

Déanann an r:id# rId2 tagairt don ghaol seo a leanas laistigh den chuid caidrimh don sleamhnán (slide1.xml.rels).

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### Gaol intuigthe ####

Maidir le gaol intuigthe, ní dhéantar tagairt dhíreach dá leithéid do `<Relationship> Id`. Ina áit sin, tuigtear an tagairt.

### Fillteán ppt ###

Is é seo an príomhfhillteán ina bhfuil na sonraí go léir faoi ábhar an Léirithe. De réir réamhshocraithe, tá fillteáin seo a leanas aige:

* \_rels

* téama

* sleamhnáin

* Leagan Amach sleamhnán

* SlideMasters


agus comhaid xml a leanas:

*cur i láthair.xml

* presProps.xml

* táblaStíleanna.xml

* amharcProps.xml


## Tagairtí ##

* [[MS-PPTX] - Formáid Chomhaid PPTX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)

* [Oifig Oscailte XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


