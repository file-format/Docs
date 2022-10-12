{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAML-Dateiformat - Haml-Quellcodedatei",
  "description":"Erfahren Sie mehr über das HAML-Dateiformat und APIs, die HAML-Dateien erstellen und öffnen können.",
  "linktitle" :"HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Was ist eine HAML-Datei?

Eine HAML-Datei ist eine HTML-Abstraktions-Markup-Sprachdatei, die Quellcode enthält, der in der Sprache [Haml](https://haml.info/) geschrieben ist. Es kann als Ersatz für das ERB (Ruby Template Scripts) verwendet werden. Die HAML-Datei enthält Vorlagenquellcode zum Generieren des HTML-Codes eines Webdokuments. ERB-Dateien können ersetzt werden, indem diese Dateien einfach im Ordner app/views durch Haml ersetzt werden, indem die Erweiterung der Datei geändert wird. HAML-Dateien können mit jedem Texteditor wie Microsoft Notepad, Notepad++, Apple TextEdit,

## HAML-Dateiformat

HAML-Dateien sind Quelldateien, die als reine Textdateien auf Disc gespeichert werden. Es enthält Code, der in HAML-Syntax geschrieben ist. HAML ersetzt die **<>**-Tags durch das **%**-Zeichen, um den Code einfacher und einfacher zu machen. ERB-Dateien können per Drop-in durch HAML ersetzt werden, wie im folgenden einfachen Beispiel gezeigt.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML-Beispiel

Im Folgenden finden Sie ein Hello-World-Beispiel für HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
was zur folgenden HTML-Ausgabe gerendert wird.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Verweise

* [HAML - Github](https://github.com/haml/haml)

