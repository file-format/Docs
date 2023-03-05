---
date: 2019-10-11
keywords: scss, .scss, scss fájlformátum, scss fájlok megnyitása, szintaktikailag fantasztikus stíluslap, css előfeldolgozó, sass
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS fájlformátum - Sass lépcsőzetes stíluslap
linktitle: SCSS
description: "Ismerje meg az SCSS fájlformátumot és az API-kat, amelyek SCSS-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Mi az SCSS fájl? ##

Az SCSS a Sass (Syntactically Awesome Stylesheet) második szintaxisa, amely behúzás helyett zárójeleket használ. Az SCSS-t úgy tervezték meg, hogy az érvényes CSS3 fájl egyben érvényes SCSS fájl is legyen. Az SCSS-fájlok tárolása .scss kiterjesztéssel történik.

## Miért használja az SCSS-t ##

Mivel a webhelyek kialakítása egyre bonyolultabbá válik, ami nagy [CSS](/hu/web/css/) fájlokat eredményez. Az ilyen fájlokat nehezebb karbantartani. Itt jön be az SCSS. Az SCSS változókat, egymásba ágyazást, mixineket, importálást és szelektor öröklődést vezet be a CSS-fejlesztésben. Ezek a kiegészítések sokkal szórakoztatóbbá teszik a tervezéssel való munkát.

## Az SCSS-fájlok használata ##

Az SCSS-fájlok nem szerepelnek közvetlenül a [HTML](/hu/web/html/) dokumentumban, például a CSS-ben. Ehelyett az SCSS-fájlok CSS-fájlokká konvertálódnak, amelyeket a HTML-fájlok tartalmaznak. Az SCSS rendszerére való telepítéséhez kövesse a [Official Sass Site](https://sass-lang.com/install) utasításait.
Az SCSS CSS-vé konvertálásához vagy konvertálhat egy már mentett SCSS-fájlt, vagy figyelheti a változásokat, és konvertálhat a fájl mentése közben. A parancsok mindkettőhöz alább találhatók.

### Egyszer konvertálni ###

Az első paraméter a forrás SCSS fájl, a második paraméter pedig a kimeneti CSS fájl.

```cmd
sass main.scss main.css
```

### Figyelje a változásokat ###

A parancsnak van egy további *watch** jelzője, amely a parancs futtatását tartja, és amint az SCSS-fájl mentésre kerül, a kimeneti CSS generálódik.

```cmd
sass --watch main.scss main.css
```

## SCSS szintaxis ##

Az SCSS támogatja a változókat, a beágyazást, a mixineket, az importálást, a szelektor öröklését stb. Az alábbiakban ezekre a szolgáltatásokra mutatunk be példákat.

### Változók ###

Változók használatával beállíthatja az újrafelhasználható információkat, például a mentés gomb elsődleges színét vagy háttérszínét. Ez akkor hasznos, ha módosítania kell ezeket az információkat, csak egy helyen módosítja, és minden alkalommal frissül, ahol használják.

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

**Generált CSS**

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

A CSS-választókat a HTML hierarchiájához hasonlóan egymásba ágyazhatja. Az alábbi példában a span a h1 blokkba van beágyazva.

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

**Generált CSS**

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

A mixinek segítségével csoportosíthatók a több helyen együtt használt hasonló tulajdonságok. Paramétereket is átadhat a mixineknek.

**SCSS**

**Keverés bejelentése**

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

**Mixin használata**

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

**Generált CSS**

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

Az Extend/Inheritance olyan esetekben hasznos, amikor egy szelektor tulajdonságait meg kell osztani egy másik szelektorral. Az alábbi példában az *.error-notice* választó átveszi az *.error-text* választó összes tulajdonságát, és hozzáadja a szegély és a kitöltés tulajdonságait.

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

**Generált CSS**

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

Az importálás hasznos lehet a problémák szétválasztásában. A stílusokat feloszthatja úgy, hogy a fejlécstílusok külön fájlban, a láblécstílusok külön fájlban legyenek, a stílusokban használt színváltozók külön fájlban legyenek stb. Ezzel a technikával a a stílusok rendszerezettek maradnak. Csak importálja a fájlokat a fő SCSS-fájlba az alábbi példában látható módon. Az importálási utasításban nem kell megadnia a fájl kiterjesztését. A Sass közvetlenül fordítja le az összes SCSS-fájlt. Annak elkerülése érdekében, hogy az importfájlokat közvetlenül lehessen fordítani, részlegessé teheti őket úgy, hogy aláhúzásjelet (_) ír a nevük elé. A normál SCSS-fájlokhoz hasonló részeket importálhat aláhúzás nélkül.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

A kimeneti CSS az összes importált fájl stílusát tartalmazza.

## Referenciák ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

