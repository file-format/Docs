{
"Datum": "09.11.2023",
   "keywords":[
"Zoo",
"Zoo-Datei",
"Zoo-komprimierte Datei",
"Wie öffnet man eine Zoo-Datei",
"Datei",
"Zoo-Dateierweiterung",
"Verlängerung",
"Datei"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title": "ZOO-Datei – Was ist eine .zoo-Datei und wie öffnet man sie?",
   "description":"Erfahren Sie mehr über das ZOO-komprimierte Dateiformat und die APIs, mit denen ZOO-Dateien erstellt und geöffnet werden können.",
"linktitle": "ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
"parent": "Komprimierung"
}
},
"lastmod": "09.11.2023"
}

## Was ist eine ZOO-Datei?

Eine ".zoo"-Datei ist ein Archivformat, das zum Komprimieren und Speichern von Dateien und Verzeichnissen verwendet wird; ähnelt anderen Archivformaten wie ".zip", ".tar" und ".rar". Das ".zoo"-Format war in den Anfängen der Computertechnik beliebt, ist aber in den letzten Jahren seltener geworden. Es wurde ursprünglich von **Rahul Dhesi** entwickelt und hauptsächlich auf Unix- und DOS-Systemen verwendet.

Eine ".zoo"-Datei enthält normalerweise eine oder mehrere Dateien und Verzeichnisse, die komprimiert und in einer einzigen Datei archiviert wurden. Sie können ".zoo"-Dateien mit verschiedenen Softwaretools erstellen und extrahieren, die dieses Format unterstützen.

ZOO-Archive verfügen über eine einzigartige Funktion, die es ihnen ermöglicht, mehrere Versionen derselben Datei zu speichern, vorausgesetzt, jede Version wurde an einem anderen Datum geändert. Dies bedeutet, dass ZOO-Benutzer frühere Dateiiterationen direkt aus dem ZOO-Archiv speichern und darauf zugreifen können. Mit dieser Funktion können Benutzer zu einer früheren Dateiversion zurückkehren oder eine ältere Version mit einer neueren Version vergleichen, was eine bequeme Möglichkeit bietet, Dateirevisionen und -änderungen im Laufe der Zeit zu verwalten.

## Allgemeine Operationen von ZOO-Dateien

Hier sind einige häufige Vorgänge im Zusammenhang mit ".zoo"-Dateien:

1. **Erstellen einer ".zoo"-Datei:** Sie können ein Befehlszeilenprogramm wie "zoo" verwenden, um eine ".zoo"-Datei zu erstellen. Mit dem folgenden Befehl wird beispielsweise das Archiv ".zoo" aus dem Verzeichnis erstellt:
    








`zoo a -c archive.zoo Verzeichnis/`
    








In diesem Befehl steht "a" für "add", "-c" gibt die Komprimierung an und "archive.zoo" ist der Name des Ausgabearchivs.
    








2. **Extrahieren von Dateien aus einer ".zoo"-Datei:** Um Inhalte des ".zoo"-Archivs zu extrahieren, können Sie einen Befehl wie diesen verwenden:
    








`zoo e archive.zoo`
    








Dieser Befehl extrahiert Dateien aus der Datei "archive.zoo".
    








3. **Auflisten des Inhalts einer ".zoo"-Datei:** Sie können den Inhalt eines ".zoo"-Archivs auflisten, ohne ihn mit der Option "l" zu extrahieren:
    








    








`zoo l archive.zoo`

## Wie öffne ich eine ZOO-Datei?

Zu den Programmen, die ZOO-Dateien öffnen, gehören:

- **zoo** (Kostenlos) für (Windows, Linux)

## Verweise
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
