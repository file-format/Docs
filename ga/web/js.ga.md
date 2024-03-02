---
date: 2019-10-11
keywords: js, .js, js file format, how to open js files, javascript files
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS Foirm Chomhaidat
linktitle: JS
description: Ltuilleamh faoi fhormáid comhaid JS agus APIs ar féidir leo comhad JS a chruthú agus a oscailts.
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Cad is comhad JS ann? ##

Is comhaid iad JS (JavaScript) a bhfuil cód JavaScript iontu le cur i gcrích ar leathanaigh ghréasáin. Stóráiltear comhaid JavaScript leis an síneadh .js. Laistigh den doiciméad [HTML](/web/html/), is féidir leat an cód JavaScript a leabú trí úsáid a bhaint as \ \ <script>\</script> clibeanna nó cuir comhad JS san áireamh. Cosúil le comhaid [CSS](/web/css/), is féidir comhaid JS a áireamh in iliomad doiciméad HTML chun cód a ath-úsáid. Is féidir JavaScript a úsáid chun an HTML DOM a ionramháil.

## Stair Ghearr ##

Seoladh JavaScript den chéad uair mar chuid den Bhrabhsálaí Navigator i Meán Fómhair 1995 leis an ainm LiveScript ag Netscape. Athainmníodh JavaScript air trí mhí ina dhiaidh sin. I 1996, rinne Microsoft ateangaire cúl-innealtóireacht Navigator chun JScript a chruthú. Eisíodh JScript le Internet Explorer agus bhí sé an-difriúil ná JavaScript.

Netscape submitted JavaScript to ECMA International that lead to the official release of the first ECMAScript specification in 1997. Eisíodh ECMAScript 2 i 1998, ECMAScript 3 i 1999, agus cuireadh tús le hobair ar ECMAScript 4 i 2000 ach níor tháinig sé riamh i gcrích.

Sa bhliain 2005 d'eisigh Jesse James Garrett páipéar bán inar chum sé an téarma *Ajax*. D’úsáid sé seo JavaScript mar chnámh droma chun feidhmchláir ghréasáin a chruthú a lódáil sonraí sa chúlra agus a sheachain athlódáil leathanaigh iomlána. Mar thoradh air seo cruthaíodh leabharlanna mar JQuery, Prototype, Dojo, etc.

Google released the Chrome browser with the V8 JavaScript engine in 2008. Go luath in 2009, rinneadh comhaontú an obair ábhartha ar fad a chur le chéile agus JavaScript a chur chun cinn. Ba é an toradh a bhí air seo ná gur eisíodh Caighdeán ECMAScript 5 i mí na Nollag 2009.

## Conas comhaid JS a úsáid ##

Chun comhad JS a úsáid, cuireann tú é sa doiciméad HTML. Úsáideann tú an chlib naisc chun an comhad a chur san áireamh mar a thaispeántar thíos.

```html
<script src="site.js"></script>
```

Tá an chonair chuig an gcomhad JS san aitreabúid *src* den chlib *script*. Trí seo a dhéanamh, cuirtear an fheidhmiúlacht JS leis an doiciméad HTML.

## Comhréir JS ##

Is féidir le hathróga, oibreoirí, feidhmeanna, coinníollacha, lúba, eagair, réada, srl a bheith i gcomhaid JavaScript. Tugtar thíos forbhreathnú gairid ar chomhréir JavaScript.

- Críochnaíonn gach ordú le leathstad (;).
- Bain úsáid as an eochairfhocal *var* chun athróga a dhearbhú.
- Supports arithmetic operators ( + - * / ) luachanna a ríomh.
- Cuirtear tráchtanna aonlíne leis // agus tá /* agus */ timpeallaithe ag tuairimí illíne.
- Tá na haitheantóirí uile cás-íogair .i. is dhá athróg dhifriúla iad *múnla* agus *modelno*.
- Feidhmeanna a shainmhíniú ag baint úsáide as an * fheidhm * eochairfhocal.
- Is féidir eagair a shainiú ag baint úsáide as lúibíní cearnacha [].
- Tacaíonn JS le hoibreoirí comparáide mar ==, != , >=, !==, etc.
- Is féidir ranganna a shainiú ag baint úsáide as an eochairfhocal * rang*.

## Sampla Úsáide JS ##

Taispeánann an méid seo a leanas sampla úsáide simplí de chomhad JavaScript.

### Doiciméad HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### Cód JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Tagairtí ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

