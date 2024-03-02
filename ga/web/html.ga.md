{
  "date": "2019-10-11",
  "keywords": [
"html",
"comhad html",
"Formáid comhaid html",
"Cineál comhaid html",
"comhad",
"cineál",
"Cad é an comhad html"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid HTML",
  "description": "Foghlaim faoi fhormáid comhaid HTML agus APIs ar féidir leo comhaid HTML a chruthú agus a oscailt.",
  "linktitle": "HTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htm-gal"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad HTML ann?

Is é HTML (Hyper Text Markup Language) an síneadh do leathanaigh ghréasáin a cruthaíodh le taispeáint i mbrabhsálaithe. Ar a dtugtar teanga an ghréasáin, tá HTML tagtha chun cinn agus riachtanais faisnéise nua le taispeáint mar chuid de leathanaigh ghréasáin. Tugtar HTML 5 ar an leagan is déanaí a thugann go leor solúbthachta maidir le bheith ag obair leis an teanga. Faightear leathanaigh HTML ón bhfreastalaí, áit a ndéantar iad a óstáil, nó is féidir iad a luchtú ón gcóras áitiúil freisin. Tá gach leathanach HTML comhdhéanta d'eilimintí HTML cosúil le foirmeacha, téacs, íomhánna, beochan, naisc, etc. Léirítear na heilimintí seo le clibeanna agus go leor eile ina bhfuil tús agus deireadh ag gach clib. Is féidir leis feidhmchláir scríofa i dteangacha scriptithe ar nós JavaScript agus Stílbhileoga (CSS) a leabú freisin chun leagan amach iomlán a léiriú.

## Stair Ghearr ##

Since its inception and first role out, the HTML specifications have been maintained by World Wide Web Consortium (W3C) since 1996. Sa bhliain 2000, rinneadh caighdeán idirnáisiúnta de freisin (ISO/IEC 15445:2000). Sa bhliain 1999, foilsíodh HTML 4.01. In 2004, thosaigh an Grúpa Oibre um Theicneolaíocht Feidhmchláir Hipirtéacs Gréasáin (WHATWG) ag obair ar an leagan HTML5 a tháinig chun bheith ina chomhsholáthar leis an W3C in 2008. Críochnaíodh agus caighdeánaíodh é an 28 Deireadh Fómhair 2014.

## Struchtúr Formáide Comhaid HTML ##

Tá trí chuid i gcáipéis HTML 4:

1. líne ina bhfuil faisnéis faoin leagan HTML
1. alt ceanntásc dearbhaithe
1. comhlacht, ina bhfuil ábhar iarbhír an doiciméid. Féadfaidh an eilimint COMHLACHT nó an eilimint FRAMESET an corp a chur chun feidhme chun an corp a choinneáil i bhfrámaí

Is féidir spásanna bána, línte nua, cluaisíní agus nótaí tráchta a threorú nó a leanúint. Tá sampla de dhoiciméad HTML simplí mar a thaispeántar thíos:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding Formáid Comhaid HTML</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Eolas faoin Leagan ###

An chéad líne de chód, \<!DOCTYPE html> , ar a dtugtar dearbhú doctype agus insíonn sé don bhrabhsálaí cén leagan de HTML a bhfuil an leathanach scríofa ann. Ag brath ar an leagan de HTML, tá roinnt dearbhuithe doctype éagsúla ann a ainmníonn an sainmhíniú ar an gcineál doiciméid (DTD) atá in úsáid don doiciméad. Tá gach DTD difriúil ó na cinn eile sna heilimintí a thacaíonn sé agus difriúil mar a leanas:

* HTML 4.01 Strict - folaíonn sé gach eilimint agus airí nach bhfuil [deprecated](https://www.w3.org/TR/html401/conform.html#deprecated) nó nach bhfuil le feiceáil i gcáipéisí frameset

* HTML 4.01 Idirthréimhseach - folaíonn sé gach rud sa DTD docht móide gnéithe agus tréithe dímheasta (baineann an chuid is mó acu le cur i láthair amhairc

* Fráma HTML 4.01 - folaíonn sé gach rud san idirthréimhseach DTD móide frámaí chomh maith


Maidir le **HTML5**, tá an fhaisnéis faoin leagan díreach mar a luaitear thíos.

```
<!DOCTYPE html>
```

### Eolas Ceanntásca HTML ###

Is féidir roinnt eilimintí HTML nach bhfuil rindreáilte ag an mbrabhsálaí a áireamh i gceanntásc doiciméad HTML. Is meiteashonraí iad gnéithe den sórt sin a chuireann síos ar fhaisnéis faoin leathanach nó a chuimsíonn ranna a úsáidtear chun faisnéis a fháil ó acmhainní seachtracha amhail stílbhileoga CSS nó comhaid JavaScript. Léirítear ceanntásc leathanach leis an gclib ceann.

Chun teideal an leathanaigh a shocrú, is í an eilimint **teideal** an t-aon eilimint amháin atá ag teastáil laistigh den<head> clibeanna. Úsáideann innill chuardaigh an rud céanna chun teideal leathanach a aithint.

### Eolas Coirp HTML ###

Is é seo an príomh-alt sa chomhad ina bhfuil gach ábhar an chomhaid atá rindreáilte ag brabhsálaithe. Is féidir marcálacha a bheith i gcorp Html ar féidir leo tagairt a dhéanamh do bhlocanna tógála éagsúla i gcruth clibeanna. Féadfaidh sé go bhfuil cineálacha éagsúla faisnéise mar téacs, íomhánna, dathanna, grafaicí, etc. Ina theannta sin, is féidir gnéithe fuaime agus físe a neadú freisin i gcorp html le rindreáil ag brabhsálaithe. I láthair iarratais stílbhileoga nua-aimseartha ar léiriú amhairc, tá tréithe cur i láthair COMHLACHT cosúil le dath cúlra, dath naisc, dath an téacs, srl. Mar sin, is féidir na héifeachtaí céanna a bhaint amach trí úsáid a bhaint as stílbhileoga mar a thaispeántar thíos:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Is furasta stílbhileoga inlíne a leabú agus le haghaidh feidhmeanna tapa ar na héifeachtaí amhairc, bíonn sé níos áisiúla stílbhileoga seachtracha iad a imscaradh uair amháin agus rochtain a fháil orthu in go leor áiteanna.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Eilimintí HTML ###

Mar a luadh níos luaithe, déantar inneachar laistigh de Chomhlacht HTML a léiriú le clibeanna, ar a dtugtar Eilimintí Html freisin. Is féidir faisnéis bhreise a bheith ag gach clib i bhfoirm tréithe a scríobhtar mar<tag attribute1#value1 attribute2#value2> , cé nach gá tréithe a bheith agat le gach clib. Mura luaitear tréithe, úsáidtear luachanna réamhshocraithe i ngach cás. Seo a leanas roinnt de na samplaí Eiliminte:

#### Ceanntásc ####

```
<head>
  <title>The Title</title>
</head>
```

#### Ceannteidil ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Ailt ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Tagairtí ##

* [Struchtúr Domhanda an doiciméid HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


