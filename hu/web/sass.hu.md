---
date: 2019-10-11
keywords: sass, .sass, sass fájlformátum, sass fájlok megnyitása, szintaktikailag fantasztikus stíluslap, css előfeldolgozó, sass
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass fájlformátum
linktitle: Sass
description: "Ismerje meg a Sass fájlformátumot és az API-kat, amelyekkel Sass fájlokat hozhat létre és nyithat meg."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Mi az a SASS fájl? ##

A Sass (szintaktikailag fantasztikus stíluslapok) egy előfeldolgozó szkriptnyelv. Ez a [CSS](/hu/web/css/) formátumba van fordítva, és a .sass kiterjesztéssel kerül tárolásra. A Sass két szintaxisból áll, az eredeti a .sass kiterjesztést használó behúzásokon alapul, az újabb SCSS pedig blokkformázással, például a CSS, amely az .scss kiterjesztést használja.

## Miért érdemes Sass ##

A Sass nagyon hasznos a stílusok karbantartásában, mivel számos olyan funkciót kínál, mint például változók bevezetése, egymásba ágyazás, mixin, import és választó öröklése, amelyek szórakoztatóvá teszik a stílusokkal való munkát.

## A SASS fájlok használata ##

A SASS-fájlok nem szerepelnek közvetlenül a [HTML](/hu/web/html/) dokumentumban, hanem CSS-fájlokká konvertálják őket, amelyeket a HTML-fájlok tartalmaznak. A Sass-t a [hivatalos Sass webhelyen] (https://sass-lang.com/install) megadott utasítások követésével telepítheti rendszerére.

A Sass konvertálható CSS-vé egy már mentett SASS-fájl konvertálásával, vagy a változások figyelésével és a fájl mentése közbeni konvertálásával. A parancsok mindkettőhöz alább találhatók.

### Egyszer konvertálni ###

A parancs első paramétere a forrás SASS fájl, a második paraméter pedig a kimeneti CSS fájl.

```cmd
sass main.sass main.css
```

### Figyelje a változásokat ###

A fenti parancs futtatható egy további *watch* jelzővel, amely folyamatosan futtatja a parancsot, és amint a Sass fájl mentésre kerül, létrejön a kimeneti CSS.

```cmd
sass --watch main.sass main.css
```

## Sass szintaxis ##

A Sass támogatja a változókat, a beágyazást, a mixineket, az importálást, a szelektor öröklését stb. Az alábbiakban ezekre a szolgáltatásokra mutatunk be példákat.

### Változók ###

Változók használhatók az újrafelhasználható információk, például a gomb elsődleges színének vagy kitöltésének beállítására. Ez hasznosnak bizonyulhat, ha a jövőben meg kell változtatnia ezeket az információkat, csak egy helyen módosítja, és mindenhol frissül.

**Sass**

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

**Létrehozott CSS**

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

### Fészekrakás ###

A CSS-választók a HTML hierarchiájához hasonlóan egymásba ágyazhatók. A következő példában a span a h1 blokkba van beágyazva.

**Sass**

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

**Létrehozott CSS**

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

### Mixinek ###

A mixineket a több helyen használt hasonló tulajdonságok csoportosítására használják. A mixek is támogatják a paramétereket.

**Sass**

**Keverés bejelentése**

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

**Mixin használata**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**Létrehozott CSS**

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

### Kiterjeszt ###

Az Extend/Inheritance hasznosnak bizonyulhat olyan esetekben, amikor egy szelektor tulajdonságait meg kell osztani egy másik szelektorral. Az alábbi példában az *.error-notice* választó átveszi az *.error-text* választó összes tulajdonságát, és hozzáadja a szegély és a kitöltés tulajdonságait.

**Sass**

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

**Létrehozott CSS**

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

### Importálás ###

Az importálás hasznos lehet, ha a stílusokat a funkcionalitás vagy bármely más követett struktúra alapján különböző fájlokba strukturálja. Ezeket a fájlokat importálhatja egy elsődleges SASS-fájlba, amelyet később CSS-vé alakítanak. Az importálás során nem kell megadni a fájl kiterjesztését az importálási utasításban. A Sass közvetlenül fordítja le az összes SASS fájlt. Annak elkerülése érdekében, hogy az importfájlokat közvetlenül lefordítsák, részlegessé teheti őket az aláhúzás (_) hozzáadásával a nevük elejére. A részek importálása a normál Sass-fájlokhoz hasonlóan történik.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

A kimeneti CSS az összes importált fájl stílusát tartalmazza.

## Referenciák ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

