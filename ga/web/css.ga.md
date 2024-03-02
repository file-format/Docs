---
date: 2019-10-11
keywords: css, .css, css file format, how to open css files, cascading style sheets
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CFoirm Chomhaid SSat
linktitle: CSS
description: Ltuilleamh faoi fhormáid comhaid CSS agus APIs ar féidir leo comhad CSS a chruthú agus a oscailts.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Cad is comhad CSS ann? ##

Is comhaid iad CSS (Stílbhileoga Cascáideacha) a chuireann síos ar an gcaoi a dtaispeántar eilimintí HTML ar an scáileán, ar pháipéar, etc. Le HTML, is féidir leat stíleanna leabaithe nó stíleanna a shainiú i stílbhileog seachtrach. Chun na stíleanna a leabú, tá an \ <style>\</style> úsáidtear clibeanna. Stóráiltear na stílbhileoga seachtracha i gcomhaid leis an síneadh .css. Leis an CSS seachtrach, is féidir leat é a chur san áireamh ar leathanaigh HTML iolracha chun stíl na leathanach sin a nuashonrú. Is féidir fiú comhad CSS amháin a úsáid chun suíomh Gréasáin iomlán a stíliú.

## Stair Ghearr ##

CSS1 was released in 1996 with Bert Bos as the co-author. The CSS Working Group started working on the issues that were not addressed in CSS1. Mar thoradh air seo cruthaíodh CSS2 i mí na Samhna 1997 a foilsíodh mar mholadh W3C ar 12 Bealtaine 1998. Chuir an leagan seo tacaíocht le haghaidh gléasanna a bhaineann go sonrach le meáin ar nós printéirí, clónna in-íoslódáilte, táblaí, agus suíomh eilimint. I mí an Mheithimh 1999, rinneadh moladh W3C do CSS3. Roinn sé seo an doiciméadú i modúil ina raibh gnéithe sínte ag gach modúl a shainítear i CSS2.

## Conas comhaid CSS a úsáid ##

Chun comhad CSS a úsáid, cuireann tú é sa mhír chinn den doiciméad HTML. Úsáideann tú an chlib naisc chun an comhad a chur san áireamh mar a thaispeántar thíos.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

tá an chonair chuig an gcomhad CSS san aitreabúid *ref* den chlib naisc. Trí seo a dhéanamh, cuirtear na stíleanna infheidhme atá sa chomhad CSS atá san áireamh i bhfeidhm ar an doiciméad HTML.

## Comhréir CSS ##

Tá dhá chomhpháirt i riail CSS, roghnóir agus dearbhú. Díríonn roghnóir ar eilimint sa doiciméad HTML. Féadfaidh sé a bheith ina chlib eiliminte, ina ainm ranga, ina ainm aitheantais, ina chlibeanna iolracha a thaispeánann an t-ordlathas, etc. Cuimsíonn dearbhú an sainmhíniú ar stíl a chuimsíonn maoin agus luach. Aithníonn an mhaoin maoin na heiliminte ar mian leat a athrú agus sainmhíníonn an luach a luach nua. Is féidir le dearbhuithe iolracha a bheith ag gach riail CSS. Seo a leanas sampla de riail CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Sa sampla thuas, tá an **h1** againn mar roghnóir a roghnaíonn na clibeanna h1 go léir sa doiciméad HTML. Tá dhá dhearbhú sa riail, ceann amháin le haghaidh cló-mheáchan agus an ceann eile maidir le dath. Is airíonna iad *cló-mheáchan* agus *dath* agus is iad *700* agus *forestgreen* a luachanna faoi seach.

## Sampla Úsáide CSS ##

Taispeánann an méid seo a leanas an doiciméad HTML samplach agus an stílbhileog a úsáideadh chun é a stíliú. Cuirtear an íomhá comparáide leis freisin chun comparáid a dhéanamh idir na doiciméid HTML stílithe agus simplí

### Doiciméad HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### Stílbhileog CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Comparáid Aschuir ###

Taispeánann taobh clé na híomhá an doiciméad HTML gan na stíleanna a chuirtear i bhfeidhm agus taispeánann an taobh deas an doiciméad HTML leis na stíleanna a chuirtear i bhfeidhm.

{{< figure src="../CssExample.jpg" alt="Íomhá samplach" >}}

## Tagairtí ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

