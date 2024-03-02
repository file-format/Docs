---
date: 2019-10-11
keywords: scss, .scss, scss file format, how to open scss files, syntactically awesome stylesheet, css preprocessor, sass
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SFormáid Chomhaid CSS - Stíl Chascáideacha Sass Sheet
linktitle: SCSS
description: Ltuilleamh faoi fhormáid comhaid SCSS agus APIs ar féidir leo comhad SCSS a chruthú agus a oscailts.
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Cad is comhad SCSS ann? ##

Is é SCSS an dara comhréir de Sass (Stílbhileog Uafásach Go Synctach) a úsáideann lúibíní in ionad eangú. Dearadh SCSS sa chaoi is gur comhad bailí SCSS é comhad bailí CSS3 freisin. Stóráiltear comhaid SCSS leis an síneadh .scss.

## Cén fáth a n-úsáideann SCSS ##

De réir mar a bhíonn dearadh suíomhanna gréasáin ag éirí casta as a dtagann comhaid mhóra [CSS](/web/css/). Tá sé níos deacra comhaid den sórt sin a choinneáil. Seo an áit a dtagann SCSS isteach. Tugann SCSS isteach athróga, neadú, meascáin, allmhairí, agus oidhreacht roghnóir i bhforbairt CSS. Cuireann na breisithe seo i bhfad níos mó spraoi le hoibriú le dearadh.

## Conas comhaid SCSS a úsáid ##

Níl comhaid SCSS san áireamh go díreach sa doiciméad [HTML](/web/html/) ar nós CSS. Ina áit sin, déantar comhaid SCSS a thiontú go comhaid CSS a chuimsítear i gcomhaid HTML. Chun SCSS a shuiteáil ar do chóras, lean na treoracha a thugtar ar an [Official Sass Site](https://sass-lang.com/install).
Chun SCSS a thiontú go CSS, is féidir leat comhad SCSS atá sábháilte cheana féin a thiontú nó féachaint le haghaidh athruithe agus é a thiontú de réir mar a shábháiltear an comhad. Tugtar na horduithe don dá cheann thíos.

### Tiontaigh Uair ###

Is é an chéad pharaiméadar an comhad SCSS foinse agus is é an dara paraiméadar an comhad CSS aschuir.

```cmd
sass main.scss main.css
```

### Bí ag faire le haghaidh Athruithe ###

Tá bratach *watch** breise ag an ordú a choinníonn an t-ordú ag rith agus a luaithe a shábhálfar an comhad SCSS, gintear CSS aschuir.

```cmd
sass --watch main.scss main.css
```

## Comhréir SCSS ##

Tacaíonn SCSS le hathróga, le neadú, le meascáin, le hallmhairí, le hoidhreacht roghnóirí, etc. Tugtar samplaí de na gnéithe seo thíos.

### Athróga ###

Trí athróga a úsáid, is féidir leat faisnéis ath-inúsáidte a shocrú, mar shampla dath príomhúil nó dath cúlra don chnaipe sábhála. Tá sé seo úsáideach más gá duit an fhaisnéis sin a athrú, ní gá duit ach é a athrú in aon áit amháin agus déanann sé nuashonrú ar aon áit a n-úsáidtear í.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Is féidir leat na roghnóirí CSS a neadú cosúil leis an ordlathas HTML. Sa sampla a thugtar thíos, tá an réise neadaithe laistigh den bhloc h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Is féidir meascáin a úsáid chun airíonna cosúla a ghrúpáil le chéile a úsáidtear le chéile in áiteanna iolracha. Is féidir leat paraiméadair a chur ar aghaidh chuig meascáin freisin.

**SCSS**

**meascán á dhearbhú**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

** Ag baint úsáide as meascthóir**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

Tá Leathnú/Oidhreacht úsáideach i gcásanna inar gá airíonna roghnóra amháin a roinnt le roghnóir eile. Sa sampla thíos, glacann an roghnóir *.error- notice* airíonna uile an roghnóir *.error-text* agus cuireann sé airíonna teorann agus stuála.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

Is féidir le hiompórtáil a bheith úsáideach chun ábhair imní a scaradh. Is féidir leat na stíleanna a roinnt sa chaoi is go bhfuil na stíleanna ceanntásc i gcomhad ar leith, go bhfuil na stíleanna buntásc i gcomhad ar leith, is féidir na hathróga datha go léir a úsáidtear sna stíleanna a bheith i gcomhad ar leith, etc. Ag baint úsáide as an teicníc seo, an Fanann stíleanna eagraithe. Níl ort ach na comhaid a allmhairiú i do phríomhchomhad SCSS mar a thaispeántar sa sampla thíos. Ní gá duit an síneadh comhad a shonrú sa treoir allmhairithe. Tiomsaíonn Sass gach comhad SCSS go díreach. Chun comhaid iompórtála a sheachaint le tiomsú go díreach, is féidir leat codanna páirteacha a dhéanamh díobh trí bhéim(_) a chur roimh a n-ainm. Is féidir leat codanna atá cosúil le gnáthchomhaid SCSS a allmhairiú gan an foscór.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Beidh na stíleanna ó na comhaid iompórtáilte go léir ag an CSS aschuir.

## Tagairtí ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

