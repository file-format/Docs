{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","apkg-Datei", "apkg-Dateiformat", "apkg-Dateityp", "Datei", "Typ", "Was ist eine APKG-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki Flashcard Deck-Dateiformat",
  "description" :"Erfahren Sie, was eine APKG-Datei und APIs sind, die sie erstellen und öffnen können.",
  "linktitle" :"APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Was ist eine APKG-Datei?

Eine Datei mit der Erweiterung .apkg ist ein Stapel von Karteikarten, die für die Verwendung in der Softwareanwendung [Anki](https://ankiweb.net/about) erstellt wurden, bei der es sich um ein auf Karteikarten basierendes Lernprogramm handelt. Es enthält [HTML](/de/web/html/)-Text, der in der Anki-Anwendung geladen und angezeigt werden soll, und kann zusätzlich Bilder und Töne für visuelles und hörbares Lernen enthalten. Anki ermöglicht es Benutzern, ihre eigenen Anki-Lernkarten-Decks zu erstellen sowie die Lernkarten-Decks anderer Benutzer zu importieren.

## APKG-Dateiformat

Anki-Kartenspiele werden aus Vorlagen erstellt, die in HTML geschrieben sind, einer bekannten und verbreiteten Sprache zum Erstellen von Webseiten. Das Styling von Deckkarten erfolgt mit CSS, der Sprache, die zum Gestalten von Webseiten verwendet wird. Das Styling umfasst Änderungen an:

* font-family - Der Name der Schriftart, die auf der Karte verwendet werden soll.
* font-size - Die Größe der Schrift in Pixel.
* text-align - Legt fest, ob der Text zentriert, links oder rechts ausgerichtet werden soll.
* Farbe - Definiert die Farbe des Textes, die einfache Farbnamen wie "blau", "rot" usw. oder HTML-Farbcodes sein können.
* background-color - Definiert die Hintergrundfarbe der Karte

Die Gestaltungsinformationen werden von allen Karten gemeinsam genutzt und wirken sich auf alle Karten aus, wenn eine Änderung vorgenommen wird. Das folgende Beispiel verwendet einen gelben Hintergrund auf allen Karten außer der ersten:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Die Größenänderung von Bildern in einer Anki-Karte kann wie folgt gesteuert werden.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Einbetten von Javascript in Anki-Karten

Es ist möglich, [Javascript](/de/web/js/) mithilfe der Kartenvorlagen in eine Anki-Karte einzubetten. Aufgrund der fortgeschrittenen Stufe von Javascript wird jedoch keine Unterstützung bereitgestellt. Darüber hinaus können Rendering-Geräte die Implementierungseffekte von Javascript in der Karte unterschiedlich anzeigen, was dazu führt, dass die Implementierung auf allen Geräten getestet werden muss. Bestimmte Javascript-Funktionen wie window.alert erschweren das Debuggen des von Ihnen geschriebenen Javascript-Codes.

## Verweise ##

* [Anki-Dokumentation](https://docs.ankiweb.net/intro.html)

