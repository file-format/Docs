{
  "date": "2021-05-24",
  "keywords": [
"xul",
"Comhad",
"Síneadh",
"Formáid Chomhaid",
"Síneadh Comhad",
"Teanga Chomhéadain Úsáideora XML"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XUL - Comhad Teanga Chomhéadain Úsáideora XML",
  "description": "Foghlaim faoi fhormáid comhaid XUL agus APIanna ar féidir leo comhaid XUL a chruthú agus a oscailt.",
  "linktitle": "XUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xu-gal"
}
},
  "lastmod": "2021-05-24"
}

## Cad is comhad XUL ann?

Comhad teanga marcála bunaithe ar [XML](/web/xml/) chun comhéadain úsáideora a chruthú is ea comhad a bhfuil iarmhír .xul aige (seasann [XUL](https://wiki.mozilla.org/XUL:Home_Page) do XML User Interface Language). D'fhorbair Mozilla é d'fhorbróirí chun gnéithe den chomhéadan grafach úsáideora a chruthú cosúil le teangacha marcála eile a úsáidtear chun leathanaigh ghréasáin a chruthú. Tá XUL in úsáid go forleathan ag Mozilla ina bhrabhsálaí Firefox áit ar bhain sé úsáid as bunchód Mozilla. Déantar rindreáil XUL ag baint úsáide as an
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(software)). Coimeádann forcanna Firefox mar Pale Moon, Basilisk, agus Waterfox tacaíocht do bhreiseáin XUL. Aithnítear comhaid XUL le cineál MIME: application/vnd.mozilla.xul+xml.

## Formáid Chomhaid XUL

Scríobhtar comhaid XUL i ngnáth-théacs bunaithe ar fhormáid comhaid XML agus déantar iad a úsáid le hinneall Gecko. Is iad na trí phríomhchuid de struchtúr XUL:

 * `Ábhar` - Áirítear leis seo dearbhuithe na fuinneoige agus na heilimintí comhéadan úsáideora atá laistigh díobh.
 * `Skin` - Cuimsíonn sé aon stílbhileoga, íomhánna agus comhaid eile a bhaineann le téamaí. Déantar cur síos ar chuma fuinneoige sna bileoga stíl.
 * `Locale` - Stóráiltear an téacs a thaispeántar laistigh d'fhuinneog ar leithligh agus is féidir le húsáideoirí úsáid a bhaint as sraith iolrach de chomhaid teanga.

### XUL Sampla

Cruthaíonn an sampla seo a leanas trí chnaipe atá cruachta ar bharr a chéile i dtreo ingearach.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Tagairtí

* [XUL - Le Vicipéid](https://ga.wikipedia.org/wiki/XUL)

* [Doiciméadúchán Cartlainne XUL - Le Mozilla](https://wiki.mozilla.org/XUL:Home_Page)


