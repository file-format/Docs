---
date: 2019-10-11
keywords: "js, .js, js-Dateiformat, wie man js-Dateien öffnet, Javascript-Dateien"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "JS-Dateiformat"
linktitle: "JS"
description: "Erfahren Sie mehr über das JS-Dateiformat und APIs, die JS-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Was ist eine JS-Datei? ##

JS (JavaScript) sind Dateien, die JavaScript-Code zur Ausführung auf Webseiten enthalten. JavaScript-Dateien werden mit der Erweiterung .js gespeichert. Innerhalb des Dokuments [HTML](/de/web/html/) können Sie den JavaScript-Code entweder mit dem \ <script>\</script> -Tags oder fügen Sie eine JS-Datei hinzu. Ähnlich wie [CSS](/de/web/css/)-Dateien können JS-Dateien zur Wiederverwendbarkeit von Code in mehrere HTML-Dokumente eingefügt werden. JavaScript kann verwendet werden, um das HTML-DOM zu manipulieren.

## Kurze Geschichte ##

JavaScript wurde erstmals im September 1995 als Teil des Navigator-Browsers unter dem Namen LiveScript von Netscape ausgeliefert. Drei Monate später wurde es in JavaScript umbenannt. 1996 hat Microsoft den Interpreter von Navigator rückentwickelt, um JScript zu erstellen. JScript wurde mit Internet Explorer veröffentlicht und unterschied sich stark von JavaScript.

Netscape reichte JavaScript bei ECMA International ein, was 1997 zur offiziellen Veröffentlichung der ersten ECMAScript-Spezifikation führte. ECMAScript 2 wurde 1998 veröffentlicht, ECMAScript 3 1999, und die Arbeit an ECMAScript 4 begann im Jahr 2000, wurde jedoch nie verwirklicht.

Jesse James Garrett veröffentlichte 2005 ein Whitepaper, in dem er den Begriff *Ajax* prägte. Dabei wurde JavaScript als Rückgrat verwendet, um Webanwendungen zu erstellen, die Daten im Hintergrund laden und das Neuladen ganzer Seiten vermeiden. Dies führte zur Erstellung von Bibliotheken wie JQuery, Prototype, Dojo usw.

Google veröffentlichte 2008 den Chrome-Browser mit der V8-JavaScript-Engine. Anfang 2009 wurde vereinbart, alle relevanten Arbeiten zu bündeln und JavaScript voranzutreiben. Dies führte im Dezember 2009 zur Veröffentlichung des ECMAScript 5-Standards.

## So verwenden Sie JS-Dateien ##

Um eine JS-Datei zu verwenden, binden Sie sie in das HTML-Dokument ein. Sie verwenden das Link-Tag, um die Datei wie unten gezeigt einzufügen.

```html
<script src="site.js"></script>
```

Das *src*-Attribut des *script*-Tags enthält den Pfad zur JS-Datei. Dadurch wird dem HTML-Dokument die JS-Funktionalität hinzugefügt.

## JS-Syntax ##

JavaScript-Dateien können Variablen, Operatoren, Funktionen, Bedingungen, Schleifen, Arrays, Objekte usw. enthalten. Nachfolgend finden Sie einen kurzen Überblick über die Syntax von JavaScript.

- Jeder Befehl endet mit einem Semikolon (;).
- Verwenden Sie das Schlüsselwort *var*, um Variablen zu deklarieren.
- Unterstützt arithmetische Operatoren ( + - * / ) zur Berechnung von Werten.
- Einzeilige Kommentare werden mit // hinzugefügt und mehrzeilige Kommentare werden von /* und */ umgeben.
- Bei allen Bezeichnern wird zwischen Groß- und Kleinschreibung unterschieden, dh *modelNo* und *modelno* sind zwei verschiedene Variablen.
- Funktionen werden mit dem Schlüsselwort *function* definiert.
- Arrays können mit eckigen Klammern [] definiert werden.
- JS unterstützt Vergleichsoperatoren wie ==, != , >=, !== usw.
- Klassen können mit dem Schlüsselwort *class* definiert werden.

## JS-Nutzungsbeispiel ##

Das folgende Beispiel zeigt eine JavaScript-Datei mit einem einfachen Verwendungsbeispiel.

### HTML-Dokument ###

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

### JS-Code ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Verweise ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

