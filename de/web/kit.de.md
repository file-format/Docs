{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das KIT-Dateiformat und APIs, die KIT-Dateien erstellen und öffnen können.",
  "title" :"KIT-Dateiformat - CodeKit-Datei",
  "linktitle" :"SET",
  "menu" : {
    "docs" : {
"identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Was ist eine KIT-Datei?

Eine Datei mit der Erweiterung .kit ist eine HTML-Datei, die mit der Programmiersprachenanwendung [CodeKit](https://codekitapp.com/) erstellt wird. Es enthält `Importe` und `Variablen` zusätzlich zu bestehenden [HTML](/de/web/html/)-Dateien, was es ideal für statische Sites macht. CodeKit kompiliert KIT-Dateien in HTML, die problemlos als statische Website-Dateien verwendet werden können.

## KIT-Dateiformat

KIT-Dateien sind HTML-Dateien, die zusätzlich Importe und Variablen enthalten. Diese werden als einfache Textdateien gespeichert und können mit jedem Texteditor oder Webdateieditor geöffnet werden.

### Importieren von KIT-Dateien

Nahezu jeder Dateityp kann in eine Kit-Datei importiert werden. Es folgt die Importsyntax, die zum Importieren von Dateien in eine .kit-Datei verwendet wird.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Wenn ein Import zu einer KIT-Datei hinzugefügt und gespeichert wird, wird er durch den Text der importierten Datei ersetzt. Sie können auch @include anstelle von @import verwenden.

### Mehrere Importe in eine KIT-Datei

Sie können auch mehrere Dateien gleichzeitig importieren, indem Sie eine durch Kommas getrennte Liste verwenden:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Verweise

* [Was ist Kit?](https://codekitapp.com/help/kit/)

