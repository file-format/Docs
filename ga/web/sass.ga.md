---
date: 2019-10-11
keywords: sass, .sass, sass file format, how to open sass files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SFoirm Comhad asalat
linktitle: Sass
description: Ltuilleamh faoi fhormáid comhaid Sass agus APIs ar féidir leo comhad Sass a chruthú agus a oscailts.
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Cad is comhad SASS ann? ##

Is teanga scriptithe réamhphróiseálaí é Sass (stílbhileoga comhréire atá uamhnach). Déantar é a thiomsú i [CSS](/web/css/) agus stóráiltear é leis an iarmhír .sass. Tá dhá chomhréir i Sass, an bunchóip bunaithe ar eangú a úsáideann an síneadh .sass agus an SCSS níos nuaí le formáidiú bloc cosúil le CSS a úsáideann an síneadh .scss.

## Cén fáth a n-úsáideann Sass ##

Tá Sass an-chabhrach maidir le stíleanna a chothabháil mar go soláthraíonn sé go leor gnéithe cosúil le hathróga, neadú, meascáin, allmhairí agus oidhreacht roghnóir a thabhairt isteach a dhéanann spraoi le hoibriú le stíleanna.

## Conas comhaid SASS a úsáid ##

Ní chuimsítear comhaid SASS go díreach sa doiciméad [HTML](/web/html/) ach déantar iad a thiontú go comhaid CSS atá san áireamh i gcomhaid HTML. Is féidir leat Sass de do chóras a shuiteáil trí na treoracha a thugtar ar an [Official Sass Site](https://sass-lang.com/install) a leanúint.

Is féidir Sass a thiontú go CSS trí chomhad SASS atá sábháilte cheana féin a thiontú nó trí breathnú ar athruithe agus é a thiontú de réir mar a shábháiltear an comhad. Tugtar na horduithe don dá cheann thíos.

### Tiontaigh Uair ###

Is é an chéad pharaiméadar den ordú an comhad foinse SASS agus is é an dara paraiméadar an comhad CSS aschuir.

```cmd
sass main.sass main.css
```

### Bí ag faire le haghaidh Athruithe ###

Is féidir an t-ordú thuas a rith le bratach * faire * breise a choinníonn an t-ordú ag rith agus a luaithe a shábháiltear an comhad Sass, gintear CSS aschuir.

```cmd
sass --watch main.sass main.css
```

## Comhréir Sass ##

Tacaíonn Sass le hathróga, le neadú, le meascáin, le hallmhairí, le hoidhreacht roghnóirí, etc. Tugtar samplaí de na gnéithe seo thíos.

### Athróga ###

Is féidir athróga a úsáid chun faisnéis ath-inúsáidte a shocrú cosúil le dath príomhúil nó stuáil le haghaidh cnaipe. D’fhéadfadh sé seo a bheith úsáideach má theastaíonn uait an fhaisnéis sin a athrú amach anseo, mura n-athraíonn tú ach ag áit amháin í agus go ndéanann sé nuashonrú i ngach áit.

**Sas**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS ginte**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### ag neadú ###

Is féidir roghnóir CSS a neadú cosúil leis an ordlathas HTML. Sa sampla seo a leanas, tá an réise neadaithe taobh istigh den bhloc h1.

**Sas**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS ginte**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### meascáin ###

Úsáidtear meascáin chun airíonna cosúla a ghrúpáil le chéile a úsáidtear in áiteanna iolracha. Tacaíonn meascáin le paraiméadair freisin.

**Sas**

**meascán á dhearbhú**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

** Ag baint úsáide as meascthóir**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**CSS ginte**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Leathnú ###

Is féidir le síneadh/Oidhreacht a bheith úsáideach i gcásanna inar gá airíonna roghnóir amháin a roinnt le roghnóir eile. Sa sampla thíos, glacann an roghnóir *.error- notice* airíonna uile an roghnóir *.error-text* agus cuireann sé airíonna teorann agus stuála.

**Sas**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**CSS ginte**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Iompórtáil ###

Is féidir le hiompórtáil a bheith úsáideach má dhéanann tú do stíleanna a struchtúrú i gcomhaid éagsúla bunaithe ar fheidhmiúlacht nó ar aon struchtúr eile a leanann tú. Is féidir leat na comhaid seo go léir a iompórtáil i gcomhad príomhúil SASS a thiontófar go CSS níos déanaí. Agus tú ag iompórtáil, ní gá duit an síneadh comhad a shonrú sa treoir allmhairithe. Tiomsaíonn Sass gach comhad SASS go díreach. Chun comhaid iompórtála a sheachaint le tiomsú go díreach, is féidir leat codanna páirteacha a dhéanamh díobh trí bhéim(_) a chur leis ag tús a n-ainm. Allmhairítear codanna cosúil le gnáthchomhaid Sass.

**Sas**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Beidh na stíleanna ó na comhaid iompórtáilte go léir ag an CSS aschuir.

## Tagairtí ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

