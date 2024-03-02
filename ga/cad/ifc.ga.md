{
  "date": "2020-03-16",
  "keywords": [
"Comhad IFC",
"Formáid",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid IFC agus APIanna ar féidir leo comhaid IFC a chruthú agus a oscailt.",
  "title": "Formáid Comhaid IFC",
  "linktitle": "IFC",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-if-gac"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad IFC ann?

Tagraíonn comhaid le síneadh IFC d'fhormáid comhaid Aicmí Fondúireachta Tionscail (IFC) a bhunaíonn caighdeáin idirnáisiúnta chun rudaí foirgníochta agus a n-airíonna a allmhairiú agus a onnmhairiú. Soláthraíonn an fhormáid comhaid seo idir-inoibritheacht idir feidhmchláir éagsúla bogearraí. Déanann buildingSMART International sonraíochtaí don fhormáid comhaid seo a fhorbairt agus a chothabháil mar a Chaighdeán Sonraí. Is é cuspóir deiridh formáid comhaid IFC cumarsáid, táirgiúlacht, am seachadta agus cáilíocht a fheabhsú ar feadh shaolré an fhoirgnimh.

Mar gheall ar na caighdeáin bhunaithe le haghaidh rudaí coitianta sa tionscal tógála, laghdaíonn sé an caillteanas faisnéise le linn tarchurtha ó iarratas amháin go ceann eile. Is féidir le IFC sonraí a choinneáil maidir le céimseata, ríomh, cainníochtaí, bainistíocht saoráidí, praghsáil srl. do go leor gairmeacha éagsúla (ailtire, leictreach, HVAC, struchtúrach, tír-raon etc.).

## Stair Ghearr ##

Ghlac Autodesk tionscnamh IFC i 1994 chun tacú le forbairt feidhmchláir chomhtháite agus chuimsigh sé cuideachtaí mar Honeywell, Butler Manufacturing, agus AT&T. I 1995, osclaíodh an bhallraíocht do dhuine ar bith agus athraíodh an t-ainm go International Alliance for Interoperability. Ba é rún an neamhbhrabúis an Tionscal Fondúireacht Aicme (IFC) a fhoilsiú mar mhúnla táirge AEC. Sa bhliain 2005, athraíodh an t-ainm arís agus coinníonn buildSMART é anois.

## Formáid Chomhaid IFC ##

The IFC file format has undergone several changes over the past to reach the file format specifications v4. Tharla roinnt mionathruithe ó am go chéile chomh maith leis sin a rinneadh mar chuid de na sonraíochtaí mar Aguisíní. Seo a leanas liosta de na leaganacha éagsúla de shonraíochtaí comhaid a foilsíodh san am atá thart.

* IFC4 Add2 (2016) IFC4 Add1 (2015)

* IFC4 (Márta 2013) ifcXML2x3 (Meitheamh 2007)

* IFC2x3 (Feabhra 2006) ifcXML2 le haghaidh breiseán IFC2x21 (RC2)

* Aguisín IFC2x2 1 (Iúil 2004)ifcXML2 le haghaidh IFC2x2 (RC1)

* IFC 2x2IFC 2x Aguisín 1ifcXML1 le haghaidh IFC2x agus

* Aguisín IFC2x 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5


Bíonn na leaganacha is deireanaí de shonraíochtaí formáid comhaid an IFC ar fáil i gcónaí ar shuíomh Gréasáin buildingSMART agus ba cheart d’fhorbróirí breathnú orthu seo le haghaidh aon chineál feidhmchlár atá beartaithe acu a fhorbairt. Agus an t-alt seo á scríobh, is iad sonraíochtaí leagan 4 na cinn is déanaí atá ar fáil ar líne.

### Formáidí Comhaid Sonraí IFC ###

Tacaíonn formáid comhaid IFF le malartú sonraí idir feidhmchláir a úsáideann formáidí éagsúla mar a liostaítear thíos:

**IFC:**  This is the default IFC exchange format and uses the STEP physical file structure according to ISO 10303-21. Tá síneadh comhaid .ifc ag an bhformáid comhaid seo agus is í an fhormáid IFC is mó a úsáidtear.

** IFC-XML:** Is leagan formáid comhaid XML é den IFC is féidir a ghiniúint go díreach tríd an bhfeidhmchlár seolta de réir struchtúr ISO 10303-28, ar a dtugtar CÉIM-XML freisin. Meastar go bhfuil formáid comhaid IFC-XML oiriúnach le haghaidh idir-inoibritheachta i measc uirlisí XML. I gcomparáid le formáid comhaid IFC, tá an IFC-XML 300-400% níos mó i méid.

**IFC-ZIP:** Is leagan comhbhrúite de [ZIP](/compression/zip/) de IFC nó IFC-XML é a bhfuil an ceann de na comhaid seo suite mar phríomh-eolaire na zip-cartlann. Comhbhrúíonn an fhormáid seo .ifc síos 60-80% agus comhad .ifc XML faoi 90-95%.

### Ailtireacht IFC ###

Áiríonn sonraíocht an IFC téarmaí, coincheapa agus míreanna sonraíochta a eascraíonn as úsáid laistigh de dhisciplíní, ceirdeanna agus gairmeacha earnáil an tionscail tógála agus bainistíochta saoráidí. Úsáideann téarmaí agus coincheapa na focail Bhéarla simplí, leanann na míreanna sonraí laistigh den tsonraíocht sonraí coinbhinsiún ainmniúcháin.

tosaíonn na hainmneacha míreanna sonraí le haghaidh cineálacha, eintiteas, rialacha agus feidhmeanna leis an réimír Ifc” agus leanann siad ar aghaidh leis na focail Bhéarla i gcoinbhinsiún ainmniúcháin CamelCase (gan béim ar bith, an chéad litir san fhocal sa chás uachtair); leanann na hainmneacha tréithe laistigh d'aonán coinbhinsiún ainmniúcháin CamelCase gan aon réimír; tosaíonn na sainmhínithe ar thacar maoine atá mar chuid den chaighdeán seo leis an réimír Pset_ agus leanann siad ar aghaidh leis na focail Bhéarla i gcoinbhinsiún ainmniúcháin CamelCase; Tosaíonn na sainmhínithe ar thacar cainníochta atá mar chuid den chaighdeán seo leis an réimír Qto_ agus leanann siad ar aghaidh leis na focail Bhéarla i gcoinbhinsiún ainmniúcháin CamelCase.

Sainmhíníonn ailtireacht scéimre sonraí an IFC ceithre shraith choincheapa, sanntar gach scéimre aonair do shraith choincheapúil amháin.

**Ciseal acmhainne** — folaíonn an ciseal is ísle gach scéimre aonair ina bhfuil sainmhínithe acmhainní, ní áirítear aitheantóir uathúil domhanda sna sainmhínithe sin agus ní úsáidfear iad go neamhspleách ar shainmhíniú arna dhearbhú ag ciseal níos airde;

**Croíchiseal** — folaíonn an chéad sraith eile an scéimre eithne agus na croí-scéimeanna sínte, ina bhfuil na sainmhínithe is ginearálta ar eintitis, iompraíonn na heintitis go léir atá sainithe ag an gcroíchiseal, nó os a chionn, aitheantas domhanda uathúil agus faisnéis úinéara agus staire go roghnach;

**Ciseal idir-inoibritheachta** — áirítear leis an gcéad chiseal eile scéimre ina bhfuil sainmhínithe eintitis a bhaineann go sonrach le speisialtóireacht ghinearálta táirge, próisis nó acmhainní a úsáidtear thar roinnt disciplíní, úsáidtear na sainmhínithe sin go hiondúil chun faisnéis foirgníochta a mhalartú agus a chomhroinnt idir fearainn;

**Ciseal fearainn** — áirítear leis an gciseal is airde scéimre ina bhfuil sainmhínithe eintitis ar speisialtóirí iad ar tháirgí, ar phróisis nó ar acmhainní a bhaineann go sonrach le disciplín áirithe, is gnách go n-úsáidtear na sainmhínithe sin chun faisnéis a mhalartú laistigh den fhearann agus chun faisnéis a roinnt.

## Tagairtí ##

* [Bunranganna Tionscail - De réir Vicipéid]( https://en.wikipedia.org/wiki/Industry_Foundation_Classes)


