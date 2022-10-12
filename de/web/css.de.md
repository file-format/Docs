---
date: 2019-10-11
keywords: "css, .css, CSS-Dateiformat, Öffnen von CSS-Dateien, Cascading Style Sheets"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "CSS-Dateiformat"
linktitle: "CSS"
description: "Erfahren Sie mehr über das CSS-Dateiformat und APIs, die CSS-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Was ist eine CSS-Datei? ##

CSS (Cascading Style Sheets) sind Dateien, die beschreiben, wie HTML-Elemente auf dem Bildschirm, Papier usw. angezeigt werden. Mit HTML können Sie entweder eingebettete Stile haben oder Stile können in einem externen Stylesheet definiert werden. Zum Einbetten der Stile wird das \ <style>\</style> Tags verwendet werden. Die externen Stylesheets werden in Dateien mit der Erweiterung .css gespeichert. Mit dem externen CSS können Sie es auf mehreren HTML-Seiten einfügen, um den Stil dieser Seiten zu aktualisieren. Sogar eine einzelne CSS-Datei kann verwendet werden, um eine komplette Website zu gestalten.

## Kurze Geschichte ##

CSS1 wurde 1996 mit Bert Bos als Co-Autor veröffentlicht. Die CSS-Arbeitsgruppe begann mit der Arbeit an den Themen, die in CSS1 nicht behandelt wurden. Dies führte im November 1997 zur Erstellung von CSS2, das am 12. Mai 1998 als W3C-Empfehlung veröffentlicht wurde. Diese Version fügte Unterstützung für medienspezifische Geräte wie Drucker, herunterladbare Schriftarten, Tabellen und Elementpositionierung hinzu. Im Juni 1999 wurde CSS3 zur Empfehlung des W3C. Dadurch wurde die Dokumentation in Module unterteilt, wobei jedes Modul in CSS2 definierte Erweiterungsfunktionen hatte.

## So verwenden Sie CSS-Dateien ##

Um eine CSS-Datei zu verwenden, fügen Sie sie in den Head-Abschnitt des HTML-Dokuments ein. Sie verwenden das Link-Tag, um die Datei wie unten gezeigt einzufügen.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

das Attribut *href* des Link-Tags enthält den Pfad zur CSS-Datei. Dadurch werden die in der mitgelieferten CSS-Datei enthaltenen zutreffenden Stile auf das HTML-Dokument angewendet.

## CSS-Syntax ##

Eine CSS-Regel besteht aus zwei Komponenten, einem Selektor und einer Deklaration. Ein Selektor zeigt auf ein Element im HTML-Dokument. Es kann entweder ein Element-Tag, ein Klassenname, ein ID-Name, mehrere Tags sein, die die Hierarchie anzeigen usw. Eine Deklaration enthält die Stildefinition, die aus Eigenschaft und Wert besteht. Die Eigenschaft identifiziert die Eigenschaft des Elements, das Sie ändern möchten, und der Wert definiert seinen neuen Wert. Jede CSS-Regel kann mehrere Deklarationen haben. Das Folgende ist ein Beispiel für eine CSS-Regel.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Im obigen Beispiel haben wir **h1** als Selektor, der alle h1-Tags im HTML-Dokument auswählt. Die Regel hat zwei Deklarationen, eine für die Schriftstärke und die andere für die Farbe. *font-weight* und *color* sind Eigenschaften und *700* und *forestgreen* sind ihre jeweiligen Werte.

## CSS-Verwendungsbeispiel ##

Im Folgenden sehen Sie das HTML-Beispieldokument und das Stylesheet, mit dem es formatiert wurde. Das Vergleichsbild wird auch hinzugefügt, um die formatierten und einfachen HTML-Dokumente zu vergleichen

### HTML-Dokument ###

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

### CSS-Stylesheet ###

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

### Ausgangsvergleich ###

Die linke Seite des Bildes zeigt das HTML-Dokument ohne die angewendeten Stile und die rechte Seite zeigt das HTML-Dokument mit den angewendeten Stilen.

{{< figure src="../CssExample.jpg" alt="Beispielbild" >}}

## Verweise ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

