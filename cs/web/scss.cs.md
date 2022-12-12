---
date: 2019-10-11
keywords: scss, .scss, formát souboru scss, jak otevřít soubory scss, syntakticky úžasná šablona stylů, css preprocesor, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru SCSS - kaskádové styly Sass
linktitle: SCSS
description: "Přečtěte si o formátu souboru SCSS a rozhraních API, která mohou vytvářet a otevírat soubory SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Co je soubor SCSS? ##

SCSS je druhá syntaxe Sass (Syntactically Awesome Stylesheet), která používá závorky místo odsazení. SCSS byl navržen tak, že platný soubor CSS3 je také platným souborem SCSS. Soubory SCSS jsou uloženy s příponou .scss.

## Proč používat SCSS ##

Vzhledem k tomu, že návrhy webových stránek se stávají složitými, výsledkem jsou velké soubory [CSS](/cs/web/css/). Takové soubory se obtížněji udržují. Zde přichází na řadu SCSS. SCSS zavádí proměnné, vnoření, mixiny, importy a dědičnost selektoru při vývoji CSS. Díky těmto doplňkům je práce s designem mnohem zábavnější.

## Jak používat soubory SCSS ##

Soubory SCSS nejsou obsaženy přímo v [HTML](/cs/web/html/) dokumentu, jako je CSS. Místo toho jsou soubory SCSS převedeny na soubory CSS, které jsou součástí souborů HTML. Chcete-li nainstalovat SCSS do vašeho systému, postupujte podle pokynů uvedených na [oficiální stránce Sass] (https://sass-lang.com/install).
Chcete-li převést SCSS na CSS, můžete buď převést již uložený soubor SCSS, nebo sledovat změny a převádět při ukládání souboru. Příkazy pro oba jsou uvedeny níže.

### Převést jednou ###

První parametr je zdrojový soubor SCSS a druhý parametr je výstupní soubor CSS.

```cmd
sass main.scss main.css
```

### Sledujte změny ###

Příkaz má další příznak *watch**, který udržuje příkaz spuštěný a jakmile je soubor SCSS uložen, je vygenerován výstupní CSS.

```cmd
sass --watch main.scss main.css
```

## SCSS syntaxe ##

SCSS podporuje proměnné, vnořování, mixiny, importy, dědění selektoru atd. Níže jsou uvedeny příklady těchto funkcí.

### Proměnné ###

Pomocí proměnných můžete nastavit znovu použitelné informace, jako je primární barva nebo barva pozadí pro tlačítko Uložit. To je užitečné, pokud potřebujete změnit tyto informace, stačí je změnit na jednom místě a aktualizují se, kdekoli jsou použity.

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

**Generované CSS**

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

### Hnízdění ###

Selektory CSS můžete vnořit podobně jako hierarchii HTML. V níže uvedeném příkladu je rozpětí vnořeno do bloku h1.

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

**Generované CSS**

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

### Mixy ###

Mixiny lze použít k seskupení podobných vlastností, které se používají společně na více místech. Můžete také předat parametry mixinům.

**SCSS**

**Vyhlášení mixin**

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

**Použití mixinu**

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

**Generované CSS**

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

### Prodloužit ###

Rozšíření/dědění je užitečné v případech, kdy je třeba sdílet vlastnosti jednoho selektoru s jiným selektorem. V níže uvedeném příkladu selektor *.error-notice* přebírá všechny vlastnosti selektoru *.error-text* a přidává vlastnosti ohraničení a odsazení.

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

**Generované CSS**

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

### Import ###

Import může být užitečný při oddělení obav. Styly můžete rozdělit tak, že styly záhlaví jsou v samostatném souboru, styly zápatí v samostatném souboru, všechny barevné proměnné použité ve stylech mohou být v samostatném souboru atd. Pomocí této techniky styly zůstávají organizované. Stačí importovat soubory do hlavního souboru SCSS, jak je znázorněno v příkladu níže. V pokynech pro import není nutné zadávat příponu souboru. Sass kompiluje všechny soubory SCSS přímo. Abyste se vyhnuli přímému zkompilování importovaných souborů, můžete je změnit na částečné přidáním podtržítka(_) před jejich název. Můžete importovat části podobné běžným souborům SCSS bez podtržítka.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Výstupní CSS bude mít styly ze všech importovaných souborů.

## Reference ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

