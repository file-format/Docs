{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","dhtml-Datei", "dhtml-Dateiformat", "dhtml-Dateityp", "Datei", "Typ", "was ist eine dhtml-Datei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Dynamisches HTML-Dateiformat",
  "description":"Erfahren Sie mehr über das DHTML-Dateiformat und APIs, die DHTML-Dateien erstellen und öffnen können.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine DHTML-Datei?

Eine Datei mit der Erweiterung .dhtml ist eine dynamische [HTML](/de/web/html/)-Datei, die zum Erstellen dynamischer Inhalte einer Webseite verwendet wird. Ein in DHTML erstelltes Webelement ist ereignisgesteuert und erfordert kein erneutes Laden der Seite. In den meisten Fällen wird eine DHTML-Datei verwendet, um die dynamischen Inhalte einer Webseite wie Dropdown-Menüs, schwebende Ebenen, Rollover-Schaltflächen und andere dynamische Inhalte zu erstellen. Dynamische HTML-Elemente begegnen Ihnen fast täglich in Ihrem Leben, wenn Sie mit der Maus über einen Menüpunkt fahren und sich weitere Untermenüoptionen öffnen. DHTML nutzt Webtechnologien wie [HTML](/de/web/html/), [Javascript](/de/web/js/), HTML DOM, HTML Events und [CSS](/de/web/css/), um die Dynamik zu erreichen Verhalten der Elemente.

## DHTML-Dateiformat

DHTML-Dateien sind einfache Textdateien, die DHTML-Code enthalten, um das dynamische Verhalten der Webelemente zu implementieren.


### DHTML-DOM

Das DHTML-Dokumentobjektmodell (DOM) basiert auf dem HTML-DOM, das eine Baumstruktur mit Elementen, Attributen und Text ist, wie in der folgenden Abbildung gezeigt.

{{< figure src="../dhtml.png" alt="HTML-DOM" >}}

Der „Dokument“-Knoten kann verwendet werden, um mehrere Funktionen aufzurufen, um unterschiedliche Funktionalitäten zu implementieren. Das folgende Beispiel verwendet einfach die Methode document.write() von JavaScript in DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Dieser Code schreibt den Text „Hello World“ zur Ausgabe im Browser.

### DHTML-Ereignisse

|S.Nr.|Ereignis|Ereignis|
---|---|---|
|1|onabort|Erscheint, wenn der Benutzer das Laden der Seite oder Mediendatei abbricht.|
|2|onblur|Erscheint, wenn der Benutzer ein HTML-Objekt verlässt.|
|3|onchange|Erscheint, wenn der Benutzer den Wert eines Objekts ändert oder aktualisiert.|
|4|onclick|Er tritt auf oder wird ausgelöst, wenn ein Benutzer auf ein HTML-Element klickt.|
|5|ondblclick|Erscheint, wenn der Benutzer zweimal gleichzeitig auf ein HTML-Element klickt.|
|6|onfocus|Erscheint, wenn der Benutzer sich auf ein HTML-Element konzentriert. Dieser Event-Handler arbeitet gegensätzlich zu onblur.|
|7|onkeydown|Es wird ausgelöst, wenn ein Benutzer eine Taste auf einem Tastaturgerät drückt. Dieser Ereignishandler funktioniert für alle Schlüssel.|
|8|onkeypress|Es wird ausgelöst, wenn der Benutzer eine Taste auf einer Tastatur drückt. Dieser Ereignishandler wird nicht für alle Schlüssel ausgelöst.|
|9|onkeyup|Es tritt auf, wenn ein Benutzer eine Taste von einer Tastatur loslässt, nachdem er auf ein Objekt oder Element gedrückt hat.|
|10|onload|Erscheint, wenn ein Objekt vollständig geladen ist.|
|11|onmousedown|Erscheint, wenn ein Benutzer die Taste einer Maus über einem HTML-Element drückt.|
|12|onmousemove|Erscheint, wenn ein Benutzer den Cursor auf ein HTML-Objekt bewegt.|
|13|onmouseover|Erscheint, wenn ein Benutzer den Cursor über ein HTML-Objekt bewegt.|
|14|onmouseout|Er tritt auf oder wird ausgelöst, wenn der Mauszeiger aus einem HTML-Element herausbewegt wird.|
|15|onmouseup|Er tritt auf oder wird ausgelöst, wenn die Maustaste über einem HTML-Element losgelassen wird.|
|16|onreset|Es wird vom Benutzer verwendet, um das Formular zurückzusetzen.|
|17|onselect|Erscheint, nachdem der Inhalt oder Text auf einer Webseite ausgewählt wurde.|
|18|onsubmit|Es wird ausgelöst, wenn der Benutzer nach dem Absenden eines Formulars auf eine Schaltfläche klickt.|
|19|onunload|Es wird ausgelöst, wenn der Benutzer eine Webseite schließt.|

## Verweise

* [Dynamisches HTML – Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

