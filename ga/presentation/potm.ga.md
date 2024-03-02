{
  "date": "2019-10-11",
  "keywords": [
"comhad potm",
"formáid comhaid potm",
"cad is comhad potm ann",
"comhad",
"sampla potm",
"síneadh comhad potm",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "POTM - Comhad Teimpléad Microsoft PowerPoint le Macraí",
  "description": "Foghlaim faoi fhormáid comhaid POTM agus APIanna ar féidir leo comhaid POTM a chruthú agus a oscailt.",
  "linktitle": "POTM",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pot-gam"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad POTM ann?

Is comhaid teimpléid Microsoft PowerPoint iad comhaid le síneadh POTM le tacaíocht do Macraí. Cruthaítear comhaid POTM le PowerPoint 2007 nó níos airde agus tá socruithe réamhshocraithe iontu ar féidir iad a úsáid chun comhaid léirithe breise a chruthú. Is féidir stíleanna, cúlraí, pailéad dathanna, clónna agus mainneachtainí a áireamh sna socruithe seo chomh maith le macraí a chuimsíonn feidhmeanna saincheaptha chun tasc ar leith a dhéanamh. Is féidir iad a oscailt freisin le leagan roimhe seo de PowerPoint le tacaíocht doiciméad Open XML suiteáilte. Is féidir comhaid POTM a oscailt i Microsoft PowerPoint le haghaidh eagarthóireachta mar aon chomhad PowerPoint eile.

## Sonraíochtaí Formáid Chomhaid ##

Tá formáid comhaid POTM bunaithe ar shonraíochtaí Office OpenXML agus tá sí cosúil le struchtúr an chomhaid [PPTX](/presentation/pptx/) atá ina chartlann chomhbhrúite [ZIP](/compression/zip/).

Féadfaidh téacs, pictiúir, físeáin, grafaic agus rudaí eile a bheith sna sleamhnáin taobh istigh de chomhad POTM ar féidir iad a shocrú go saor laistigh den leathanach. Úsáidtear teimpléid POTM ansin chun comhaid iolracha a chruthú a bhfaighidh gach rogha formáidithe an chomhaid mar oidhreacht. Mar sin, faightear na macraí atá sa chomhad POTM le hoidhreacht léirithe eile freisin. Déantar iad a leabú i struchtúr an doiciméid tríd an Macra-thaifeadán atá san áireamh in MS Office ar féidir leis seichimh ordaithe a shábháil agus macraí a chruthú chun iad a mhacasamhlú go huathoibríoch.

Comhaid a ghintear leis an oifig Is éard atá i bhformáid comhaid XML Oscailte ná bailiúchán de chomhaid XML mar aon le comhaid eile a sholáthraíonn naisc idir na comhábhair go léir. Is cartlann chomhbhrúite é an bailiúchán seo ar féidir a bhaint as chun féachaint ar a bhfuil ann. Chun é sin a dhéanamh, ní gá ach an síneadh comhad POTM a athainmniú le zip agus bain amach é chun a bhfuil ann a bhreathnú.

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

* [[MS-PPTX] - Formáid Chomhaid PPTX](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Oifig Oscailte XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


