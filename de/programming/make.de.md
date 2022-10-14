{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Datei erstellen - Xcode-Makefile-Skriptdatei",
  "description":"Erfahren Sie mehr über das XCode-MakeFile-Format und APIs, die MakeFile-Dateien erstellen und öffnen können.",
  "linktitle" :"MACHEN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Was ist eine MAKE-Datei?

Eine MAKE-Datei ist eine XCode-Skriptdatei, die die Kompilierung von Code organisiert. Es wird verwendet, um Programme aus mehreren Quellcodedateien zu kompilieren und zu verknüpfen. Dies hilft bei der Entscheidung, welche Teile einer großen Anwendung neu kompiliert werden müssen, wenn die Anwendung aktualisiert werden muss. Lassen Sie Dateien eine Reihe von Anweisungen verwenden, die ausgeführt werden, je nachdem, welche Dateien sich geändert haben.

## Beispiel für ein MAKE-Dateiformat

Der folgende Inhalt wird unter Verwendung des Make-Dienstprogramms ausgeführt und die Ausgaben sind wie folgt.

```
hello:
	echo "hello world"
```
**Ausgabe erstellen**

```
$ make
echo "hello world"
hello world
```

## Verweise
* [XCode und Make – Apple-Foren](https://developer.apple.com/forums/thread/657458)
* [Objekt-C-Anleitung](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

