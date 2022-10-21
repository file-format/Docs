---
date: 2019-10-11
keywords: "scss, .scss, scss-Dateiformat, wie man scss-Dateien öffnet, syntaktisch geniales Stylesheet, CSS-Präprozessor, sass"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "SCSS-Dateiformat - Sass Cascading Style Sheet"
linktitle: "SCSS"
description: "Erfahren Sie mehr über das SCSS-Dateiformat und APIs, die SCSS-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Was ist eine SCSS-Datei? ##

SCSS ist die zweite Syntax von Sass (Syntactically Awesome Stylesheet), die Klammern anstelle von Einrückungen verwendet. SCSS wurde so konzipiert, dass eine gültige CSS3-Datei auch eine gültige SCSS-Datei ist. SCSS-Dateien werden mit der Erweiterung .scss gespeichert.

## Warum SCSS ## verwenden

Da die Designs von Websites immer komplexer werden, entstehen große [CSS](/de/web/css/)-Dateien. Solche Dateien sind schwieriger zu pflegen. Hier kommt SCSS ins Spiel. SCSS führt Variablen, Verschachtelungen, Mixins, Importe und Selektorvererbung in die CSS-Entwicklung ein. Diese Ergänzungen machen die Arbeit mit Design viel mehr Spaß.

## So verwenden Sie SCSS-Dateien ##

SCSS-Dateien sind nicht wie CSS direkt im [HTML](/de/web/html/)-Dokument enthalten. Stattdessen werden SCSS-Dateien in CSS-Dateien konvertiert, die in HTML-Dateien enthalten sind. Um SCSS auf Ihrem System zu installieren, befolgen Sie die Anweisungen auf der [offiziellen Sass-Website] (https://sass-lang.com/install).
Um SCSS in CSS zu konvertieren, können Sie entweder eine bereits gespeicherte SCSS-Datei konvertieren oder auf Änderungen achten und konvertieren, während die Datei gespeichert wird. Die Befehle für beide sind unten angegeben.

### Einmal konvertieren ###

Der erste Parameter ist die Quell-SCSS-Datei und der zweite Parameter ist die Ausgabe-CSS-Datei.

```cmd
sass main.scss main.css
```

### Auf Änderungen achten ###

Der Befehl hat ein zusätzliches *watch**-Flag, das den Befehl am Laufen hält und sobald die SCSS-Datei gespeichert wird, wird Ausgabe-CSS generiert.

```cmd
sass --watch main.scss main.css
```

## SCSS-Syntax ##

SCSS unterstützt Variablen, Verschachtelung, Mixins, Importe, Selektorvererbung usw. Nachfolgend finden Sie Beispiele für diese Funktionen.

### Variablen ###

Durch die Verwendung von Variablen können Sie wiederverwendbare Informationen wie Primärfarbe oder Hintergrundfarbe für den Speichern-Button festlegen. Dies ist nützlich, wenn Sie diese Informationen ändern müssen, Sie ändern sie einfach an einer Stelle und sie werden aktualisiert, wo immer sie verwendet werden.

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

Sie können die CSS-Selektoren ähnlich der Hierarchie von HTML verschachteln. In dem unten angegebenen Beispiel ist die Spanne innerhalb des h1-Blocks verschachtelt.

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

Mixins können verwendet werden, um ähnliche Eigenschaften zu gruppieren, die an mehreren Stellen zusammen verwendet werden. Sie können Mixins auch Parameter übergeben.

**SCSS**

**Mischung deklarieren**

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

**Mit einem Mixin**

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

Erweitern/Vererbung ist in Fällen nützlich, in denen die Eigenschaften eines Selektors mit einem anderen Selektor geteilt werden müssen. Im folgenden Beispiel übernimmt der *.error-notice*-Selektor alle Eigenschaften des *.error-text*-Selektors und fügt Rand- und Polsterungseigenschaften hinzu.

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

Das Importieren kann bei der Trennung von Bedenken nützlich sein. Sie können die Stile so aufteilen, dass sich die Kopfzeilenstile in einer separaten Datei befinden, die Fußzeilenstile in einer separaten Datei, alle in den Stilen verwendeten Farbvariablen in einer separaten Datei usw. Mit dieser Technik können die Stile bleiben organisiert. Sie importieren einfach die Dateien in Ihre Haupt-SCSS-Datei, wie im folgenden Beispiel gezeigt. Sie müssen die Dateierweiterung nicht in der Importanweisung angeben. Sass kompiliert alle SCSS-Dateien direkt. Um zu vermeiden, dass Importdateien direkt kompiliert werden, können Sie sie zu Teildateien machen, indem Sie ihrem Namen einen Unterstrich (_) voranstellen. Sie können Teiltöne ähnlich wie bei normalen SCSS-Dateien ohne den Unterstrich importieren.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Das Ausgabe-CSS enthält die Stile aller importierten Dateien.

## Verweise ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

