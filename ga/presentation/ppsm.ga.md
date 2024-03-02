{
  "date": "2019-10-11",
  "keywords": [
"comhad ppsm",
"Formáid comhaid ppsm",
"cad is comhad ppsm ann",
"comhad",
"sampla ppsm",
"Síneadh comhad ppsm",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PPSM - Comhad Cur i Láthair PowerPoint Macra-chumasaithe",
  "description": "Foghlaim faoi fhormáid comhaid PPSM agus APInna ar féidir leo comhaid PPSM a chruthú agus a oscailt.",
  "linktitle": "PPSM",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pps-gam"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad PPSM ann?

Is ionann comhaid le síneadh PPSM agus formáid comhaid Taispeántas Sleamhnán Macra-chumasaithe a cruthaíodh le Microsoft PowerPoint 2007 nó níos airde. Formáid chomhaid chomhchosúil eile is ea [PPTM](/presentation/pptm/) atá difriúil ó thaobh oscailt le Microsoft PowerPoint i bhformáid eagarthóireachta seachas é a rith mar Thaispeántas Sleamhnán. Nuair a reáchtáiltear é mar thaispeántas sleamhnán, taispeánann an comhad PPSM na sleamhnáin léirithe agus an t-ábhar slán sa taispeántas sleamhnán agus é i mód inléite amháin de réir réamhshocraithe. Is féidir comhaid PPSM a chur in eagar fós i Microsoft PowerPoint trína oscailt in PowerPoint.

## Formáid Chomhaid ##

Tugadh formáid comhaid PPSM isteach le PowerPoint 2007 agus tá sé bunaithe ar fhormáid comhaid OpenXML a úsáideann meascán de XML agus [ZIP](/compression/zip/) chun a bhfuil ann a stóráil. Comhaid a ghintear leis an oifig Is éard atá i bhformáid comhaid XML Oscailte ná bailiúchán de chomhaid XML mar aon le comhaid eile a sholáthraíonn naisc idir na comhábhair go léir. Is cartlann chomhbhrúite é an bailiúchán seo ar féidir a bhaint as chun féachaint ar a bhfuil ann. Chun é sin a dhéanamh, ní gá ach an síneadh comhad PPSM a athainmniú le zip agus bain amach é chun a bhfuil ann a bhreathnú.

Caitheann na codanna seo a leanas roinnt solais ar gach ceann díobh seo.

### [Ábhar_Cineálacha].xml ###

Is é seo an t-aon chomhad a fhaightear ag an mbonnleibhéal nuair a bhaintear an zip. Liostaíonn sé na cineálacha ábhair le haghaidh páirteanna laistigh den phacáiste. Déantar tagairt do gach tagairt do na comhaid XML atá sa phacáiste sa chomhad XML seo. Seo a leanas cineál ábhair do chuid sleamhnáin:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Más gá páirteanna nua a chur leis an bpacáiste, is féidir é a dhéanamh tríd an gcuid nua a chur leis agus aon chaidreamh laistigh de na comhaid .rels a nuashonrú. Ní mór a choinneáil i gcuimhne go gcaithfear an Content_Types.xml a nuashonrú freisin le haghaidh athrú dá leithéid.

### \_rels (Fillteán) ###

Coinníonn an chuid caidrimh idir na codanna eile agus na hacmhainní lasmuigh den phacáiste. Tá comhad XML amháin san fhillteán Caidrimh a stórálann na caidrimh ar leibhéal an phacáiste. Tá naisc chuig na príomhchodanna de na comhaid léirithe sa chomhad seo mar URIanna. Sainaithníonn na URIanna seo an cineál caidrimh a bhaineann le gach príomhchuid den phacáiste. Áirítear leis seo an gaol le doiciméad príomhoifige atá suite mar ppt/presentation.xml agus codanna eile laistigh de docProps mar réadmhaoine lárnacha agus leathnaithe.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
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

* [Formáid Chomhaid Láithreachais OpenXML](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Oifig Oscailte XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


