---
date: 2019-10-11
keywords: sass, .sass, formát souboru sass, jak otevřít soubory sass, syntakticky úžasný styl, css preprocesor, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru Sass
linktitle: Sass
description: "Přečtěte si o formátu souboru Sass a rozhraních API, která mohou vytvářet a otevírat soubory Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Co je soubor SASS? ##

Sass (syntakticky úžasné styly) je preprocesorový skriptovací jazyk. Je zkompilován do [CSS](/cs/web/css/) a je uložen s příponou .sass. Sass se skládá ze dvou syntaxí, původní založené na odsazení, které používá příponu .sass, a novější SCSS s blokovým formátováním jako CSS, které používá příponu .scss.

## Proč používat Sass ##

Sass je opravdu užitečný při udržování stylů, protože poskytuje mnoho funkcí, jako je zavádění proměnných, vnořování, mixiny, importy a dědění selektoru, díky kterým je práce se styly zábavná.

## Jak používat soubory SASS ##

Soubory SASS nejsou obsaženy přímo v dokumentu [HTML](/cs/web/html/), ale jsou spíše převedeny na soubory CSS, které jsou součástí souborů HTML. Sass svého systému můžete nainstalovat podle pokynů uvedených na [oficiální stránce Sass] (https://sass-lang.com/install).

Sass lze převést na CSS buď převodem již uloženého souboru SASS, nebo sledováním změn a převodem při ukládání souboru. Příkazy pro oba jsou uvedeny níže.

### Převést jednou ###

Prvním parametrem příkazu je zdrojový soubor SASS a druhým parametrem výstupní soubor CSS.

```cmd
sass main.sass main.css
```

### Sledujte změny ###

Výše uvedený příkaz lze spustit s dalším příznakem *watch*, který udržuje příkaz spuštěný a jakmile je soubor Sass uložen, je vygenerován výstupní CSS.

```cmd
sass --watch main.sass main.css
```

## Sass syntaxe ##

Sass podporuje proměnné, vnoření, mixiny, importy, dědění selektoru atd. Níže jsou uvedeny příklady těchto funkcí.

### Proměnné ###

Proměnné lze použít k nastavení opakovaně použitelných informací, jako je primární barva nebo výplň tlačítka. To se může ukázat jako užitečné, pokud byste v budoucnu potřebovali tyto informace změnit, stačí je změnit na jednom místě a aktualizují se všude.

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

Selektory CSS mohou být vnořeny podobně jako hierarchie HTML. V následujícím příkladu je rozsah vnořen do bloku h1.

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

Mixiny se používají k seskupení podobných vlastností, které se používají na více místech. Mixiny také podporují parametry.

**Sass**

**Vyhlášení mixin**

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

**Použití mixinu**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Rozšíření/dědění se může ukázat jako užitečné v případech, kdy je třeba sdílet vlastnosti jednoho selektoru s jiným selektorem. V níže uvedeném příkladu selektor *.error-notice* přebírá všechny vlastnosti selektoru *.error-text* a přidává vlastnosti ohraničení a odsazení.

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

Import může být užitečný, pokud strukturujete své styly do různých souborů na základě funkčnosti nebo jakékoli jiné struktury, kterou dodržujete. Všechny tyto soubory můžete importovat do primárního souboru SASS, který je později převeden na CSS. Při importu nemusíte v pokynech pro import zadávat příponu souboru. Sass kompiluje všechny soubory SASS přímo. Abyste se vyhnuli přímému zkompilování importovaných souborů, můžete je změnit na částečné přidáním podtržítka(_) na začátek jejich názvu. Části se importují podobně jako běžné soubory Sass.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Výstupní CSS bude mít styly ze všech importovaných souborů.

## Reference ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

