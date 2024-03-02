{
  "date": "2019-10-11",
  "keywords": [
"apkg",
"comhad apk",
"Formáid comhaid apk",
"cineál comhaid apk",
"comhad",
"cineál",
"Cad is comhad APKG ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APKG - Formáid Chomhaid Deic Anki Flashcard",
  "description": "Foghlaim faoi cad is comhad APKG agus APIs ann ar féidir leo iad a chruthú agus a oscailt.",
  "linktitle": "APKG",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-apk-gag"
}
},
  "lastmod": "2021-06-16"
}

## Cad is comhad APKG ann?

Is éard is comhad le síneadh .apkg ann ná deic luaschártaí a ghintear le húsáid i bhfeidhmchlár bogearraí [Anki](https://ankiweb.net/about) ar clár foghlama atá bunaithe ar chárta spléach é. Tá téacs [HTML](/web/html/) ann le luchtú agus le taispeáint i bhfeidhmchlár Anki agus is féidir íomhánna agus fuaimeanna a bheith ann le haghaidh foghlama amhairc agus inchloiste. Ligeann Anki d’úsáideoirí a ndecaí spléach-chárta Anki féin a chruthú chomh maith le deiceanna spléach-chárta úsáideoirí eile a allmhairiú.

## Formáid Comhaid APKG

Cruthaítear deiceanna cártaí Anki ó theimpléid atá scríofa i HTML, teanga choitianta agus choitianta chun leathanaigh ghréasáin a chruthú. Baintear úsáid as CSS i stíliú cártaí deic, arb é an teanga a úsáidtear chun leathanaigh ghréasáin a stíliú. Áirítear sa stíliú modhnuithe ar:

 * font-family - Ainm an chló atá le húsáid ar an gcárta.
 * font-size - Méid an chló i bpicteilíní.
 * text-ailíniú - Sainmhíníonn sé cé acu ba chóir an téacs a ailíniú sa lár, ar chlé nó ar dheis.
 * dath - Sainmhíníonn sé dath an téacs ar féidir a bheith ina n-ainmneacha simplí datha ar nós gorm, dearg, etc. nó cóid datha HTML.
 * cúlra-dath - Sainmhíníonn an dath cúlra an chárta

Roinntear an fhaisnéis stílithe i measc na gcártaí go léir, rud a chuireann isteach ar gach cárta nuair a dhéantar athrú. Úsáidfidh an sampla seo a leanas cúlra buí ar gach cárta seachas an chéad cheann:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Is féidir íomhánna méide a athrú i gcárta Anki a rialú mar seo a leanas.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Javascript a neadú i gcártaí Anki

Is féidir [Javascript](/web/js/) a leabú i gcárta Anki trí úsáid a bhaint as teimpléid chártaí. Mar gheall ar ardleibhéal Javascript, áfach, ní chuirtear a thacaíocht ar fáil. Ina theannta sin, féadfaidh feistí rindreála tionchar feidhmiúcháin Javascript a thaispeáint ar an gcárta ar bhealach difriúil, rud a d'fhág go mbeidh gá le tástáil a dhéanamh ar an gcur i bhfeidhm ar gach feiste. Gnéithe áirithe Javascript ar nós window.alert, rud a fhágann go bhfuil sé deacair an cód Javascript atá scríofa agat a dhífhabhtú.

## Tagairtí ##

* [Anki Documentation](https://docs.ankiweb.net/intro.html)

