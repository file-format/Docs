---
date: 2019-10-11
keywords: "sass, .sass, sass-Dateiformat, wie man sass-Dateien öffnet, syntaktisch tolles Stylesheet, CSS-Präprozessor, sass"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "Sass-Dateiformat"
linktitle: "Sass"
description: "Erfahren Sie mehr über das Sass-Dateiformat und APIs, die Sass-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Was ist eine SASS-Datei? ##

Sass (syntaktisch großartige Stylesheets) ist eine Präprozessor-Skriptsprache. Es wird in [CSS](/de/web/css/) kompiliert und mit der Erweiterung .sass gespeichert. Sass besteht aus zwei Syntaxen, dem Original, das auf Einrückungen basiert und die Erweiterung .sass verwendet, und dem neueren SCSS mit Blockformatierung wie CSS, das die Erweiterung .scss verwendet.

## Warum Sass ## verwenden

Sass ist wirklich hilfreich bei der Pflege von Stilen, da es viele Funktionen wie das Einführen von Variablen, Verschachteln, Mixins, Importe und Selektorvererbung bietet, die das Arbeiten mit Stilen zum Vergnügen machen.

## So verwenden Sie SASS-Dateien ##

SASS-Dateien sind nicht direkt im [HTML](/de/web/html/)-Dokument enthalten, sondern werden in CSS-Dateien konvertiert, die in HTML-Dateien enthalten sind. Sie können Sass auf Ihrem System installieren, indem Sie den Anweisungen auf der [offiziellen Sass-Website] (https://sass-lang.com/install) folgen.

Sass kann in CSS konvertiert werden, indem entweder eine bereits gespeicherte SASS-Datei konvertiert wird oder indem auf Änderungen geachtet und beim Speichern der Datei konvertiert wird. Die Befehle für beide sind unten angegeben.

### Einmal konvertieren ###

Der erste Parameter des Befehls ist die SASS-Quelldatei und der zweite Parameter ist die CSS-Ausgabedatei.

```cmd
sass main.sass main.css
```

### Auf Änderungen achten ###

Der obige Befehl kann mit einem zusätzlichen *watch*-Flag ausgeführt werden, das den Befehl am Laufen hält und sobald die Sass-Datei gespeichert ist, wird Ausgabe-CSS generiert.

```cmd
sass --watch main.sass main.css
```

## Sass-Syntax ##

Sass unterstützt Variablen, Verschachtelung, Mixins, Importe, Selektorvererbung usw. Nachfolgend sind Beispiele für diese Funktionen aufgeführt.

### Variablen ###

Variablen können verwendet werden, um wiederverwendbare Informationen wie Primärfarbe oder Polsterung für eine Schaltfläche festzulegen. Dies kann sich als nützlich erweisen, wenn Sie diese Informationen in Zukunft ändern müssen, Sie ändern sie einfach an einem Ort und sie werden überall aktualisiert.

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

**Generiertes CSS**

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

### Verschachtelung ###

CSS-Selektoren können ähnlich wie die Hierarchie von HTML verschachtelt werden. Im folgenden Beispiel ist die Spanne im h1-Block verschachtelt.

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

**Generiertes CSS**

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

### Mixins ###

Mixins werden verwendet, um ähnliche Eigenschaften zu gruppieren, die an mehreren Stellen verwendet werden. Mixins unterstützen auch Parameter.

**Sass**

**Mischung deklarieren**

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

**Mit einem Mixin**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**Generiertes CSS**

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

### Erweitern ###

Erweitern/Vererbung kann sich als nützlich erweisen, wenn die Eigenschaften eines Selektors mit einem anderen Selektor geteilt werden müssen. Im folgenden Beispiel übernimmt der *.error-notice*-Selektor alle Eigenschaften des *.error-text*-Selektors und fügt Rand- und Polsterungseigenschaften hinzu.

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

**Generiertes CSS**

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

### Importieren ###

Das Importieren kann nützlich sein, wenn Sie Ihre Stile basierend auf der Funktionalität oder einer anderen Struktur, der Sie folgen, in verschiedene Dateien strukturieren. Sie können alle diese Dateien in eine primäre SASS-Datei importieren, die später in CSS konvertiert wird. Während des Imports müssen Sie die Dateierweiterung nicht in der Importanweisung angeben. Sass kompiliert alle SASS-Dateien direkt. Um zu vermeiden, dass Importdateien direkt kompiliert werden, können Sie sie zu Teildateien machen, indem Sie ihrem Namen einen Unterstrich (_) voranstellen. Partials werden ähnlich wie normale Sass-Dateien importiert.

**Sass**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Das Ausgabe-CSS enthält die Stile aller importierten Dateien.

## Verweise ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

