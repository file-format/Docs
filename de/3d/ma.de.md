{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma-Datei", "ma-Dateiformat", "Dateiformat", "3d", "ma-Datei-Download", ".ma-Datei", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das MA-Dateiformat und APIs, die MA-Dateien öffnen und erstellen können.",
  "title" :"MA-Dateiformat",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Was ist eine MA-Datei?

Eine Datei mit der Erweiterung .ma ist eine 3D-Projektdatei, die mit der Anwendung Autodesk Maya erstellt wurde. Es enthält eine große Liste von Textbefehlen, um Informationen über die Datei anzugeben. Eine **.ma-Datei** kann in jedem Texteditor geöffnet und bearbeitet werden, um Probleme mit den Befehlen zu beheben, falls eine Datei beschädigt wird. Diese Dateien enthalten Informationen zum Definieren der 3D-Szeneninformationen wie Geometrie, Beleuchtung, Animation und Rendering.

## MA-Dateiformat

MA-Dateien werden im ASCII-Textformat auf Disc gespeichert, im Gegensatz zu MB-Dateien, die im Binärdateiformat auf Disc gespeichert werden. Eine ausführliche Referenz für das MA-Dateiformat ist in der [Autodesk Maya-Dokumentation] (https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) verfügbar und kann nachgeschlagen werden bis als Entwicklerreferenz.

### Kopfzeile der MA-Datei

Der Header der MA-Datei beginnt mit einem Abschnitt mit Kommentaren, der die Erstellungsinformationen der Datei und das Änderungsdatum enthält. Maya-Dateileser ignorieren diesen Block, da er nur zu Informationszwecken verwendet wird. Ein Header muss jedoch mit den ersten sechs Zeichen als „//Maya“ beginnen.

Der ASCII-Dateikopf sieht wie folgt aus.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Dateireferenzen

Der Dateiverweisabschnitt einer .ma-Datei enthält Informationen zu allen anderen Maya-Dateien, auf die in dieser Datei verwiesen wird. Jede referenzierte Datei kann mit einem einzigen Dateibefehl gelesen werden, der in derselben Datei enthalten ist. Die Syntax des Dateibefehls, wenn er zum Referenzieren verwendet wird, lautet:

```
file -r -rpr prefixString fileName;
```
oder

```
file -r -ns nameSpace fileName
```
Hier ist eine Beispielzeichenfolge.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Dieses Beispiel zeigt, dass das in der Datei "solar" enthaltene Sonnenobjekt in dieser Datei unter dem Namen "solar_sun" erreichbar wäre.

### Anforderungen

Der Anforderungsabschnitt einer .ma-Datei besteht aus einer Reihe von erforderlichen Befehlen und teilt May-Informationen wie Versions- und Plugin-Informationen mit, die zum Lesen der Dateien erforderlich sind. Ein Beispiel für den Anforderungsabschnitt ist wie folgt.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Der nächste Abschnitt legt die Anforderungen fest. Diese besteht aus einer Reihe von require-Befehlen. Dieser Abschnitt der Datei teilt Maya mit, welche Software benötigt wird, um die Datei richtig zu laden. Insbesondere welche Version von Maya und welche Plug-Ins.

## MA-Datei herunterladen
Es ist etwas schwierig, die MA-Datei eines 3D-Modells zu finden und herunterzuladen. Daher können Sie hier eine Beispiel-MA-Datei herunterladen:

- [Muster.ma](../Muster.ma)


## Verweise

* [Organisation von Maya-ASCII-Dateien – Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

