{
  "date": "2021-07-13",
  "keywords": [
"CFM",
"síneadh",
"comhad",
"formáid",
"córas",
"Teanga Marcáil Fusion Fusion",
"teanga",
"CFM leathanaigh ghréasáin",
"Inneall CFML",
"CFML"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFM - Marcáil Comhleá Fuar",
  "description": "Foghlaim faoi fhormáid comhaid CFM agus APIanna ar féidir leo comhaid CFM a chruthú agus a oscailt.",
  "linktitle": "CFM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cf-gam"
}
},
  "lastmod": "2021-07-13"
}

## Cad is comhad CFM ann? ##

Tá síntí CFM ar na leathanaigh ghréasáin agus ar na comhaid a úsáidtear i **Teanga Marcála Comhleá Fuar** agus tugtar leathanaigh ghréasáin CFM orthu. Ritheann an teanga scriptithe forbartha gréasáin seo ar Google App Engine, creat .NET, agus JVM. Is féidir teanga ríomhchlárúcháin nó cód na teanga a bheith ann. Nuair a fhaigheann an t-úsáideoir rochtain ar aon cheann dá leathanaigh, déanann freastalaí gréasáin ColdFusion é a fhorghníomhú. Is féidir CFScript (atá gar do JavaScript) nó clibeanna a úsáid chun CFML a scríobh. Is féidir CFML a úsáid chun teangacha eile a ghiniúint seachas [HTML](/web/html/) ar nós [CSS](/web/css/), [JavaScript](/web/js/), [XML](/web/xml/), agus eile.

Úsáidtear an teanga seo agus na clibeanna a thacaíonn sé go príomha le feidhmchláir dhinimiciúla gréasáin a fhorbairt Is féidir na comhaid a rith go díreach sa bhrabhsálaí ar líne má tharlaíonn aon earráid le linn úsáid as líne ar ardán forbartha an fheidhmchláir.
 
Oibríonn CFML ar bhealach ina dtugtar síntí comhaid freastalaí ar leith (.cfc, .cfm) le próiseáil chuig an inneall CFML. Má tá na hinnill bunaithe ar Java, baintear amach é trí úsáid a bhaint as servlets Java. Ní phróiseálann inneall CFML ach feidhmeanna agus clibeanna agus cuireann sé feidhmeanna agus téacs ar ais lasmuigh de na clibeanna CFML chuig an bhfreastalaí gréasáin gan aon athrú.


## Stair Ghearr ##

I 1995, chruthaigh corparáid darb ainm Allaire é den chéad uair. I 2005 fuair Adobe é agus cuireann sé seirbhísí ar fáil chun ColdFusion a fhorbairt go fóill. Le blianta beaga anuas, d'fhorbair agus d'uasghrádaigh go leor daoine agus cuideachtaí é. In 2012, seoladh fondúireacht darb ainm OpenCFML. Níos déanaí, in 2015 chuir an t-iar Railo a chuid seirbhísí ar fáil chun feidhmíocht CFM a fheabhsú agus rinne sé na hacmhainní níos lú le haghaidh feidhmiúlacht níos fearr. Seoladh an nuashonrú is déanaí in 2020 agus fógraítear go leanfar leis go dtí 2028.

## Formáid Chomhaid CFM ##

Cuimsíonn cód na gcomhad CFM agus na leathanaigh ghréasáin den chuid is mó na clibeanna cosúil le HTML ach le difríocht bheag. Tá na comhaid seo freagrach as oibríochtaí éagsúla a dhéanamh a chumasaíonn scripteanna ColdFusion a rith.
* Is féidir na comhaid seo a rochtain agus a reáchtáil go díreach ar Windows agus macOS araon ag baint úsáide as brabhsálaí aon chórais oibriúcháin.
* Soláthraíonn Adobe ColdFusion ardán chun leathanaigh ghréasáin agus feidhmchláir dhinimiciúla a fhorbairt ar ríomhaire.
* Is féidir aon eagarthóir téacs ar nós NotePad nó aon eagarthóir téacs eile i gcóras oibriúcháin a úsáid chun na comhaid seo a oscailt toisc go bhfuil na comhaid seo bunaithe ar théacs.
* Nuair a osclaítear aon chomhad CFM in eagarthóir téacs taispeánann sé cód atá comhdhéanta de na clibeanna agus na scripteanna nach dtuigfeadh duine mura bhforbróir gréasáin é.

## Sampla Úsáide CFM ##

Taispeánann an méid seo a leanas sampla úsáide simplí comhad CFM.

### Cáipéis CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Tagairtí ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

