{
  "date" : "2020-03-16",
  "keywords" :[ "PAT-Datei", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das PAT-Dateiformat und APIs, die PAT-Dateien erstellen und öffnen können.",
  "title" :"PAT-Dateiformat",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Was ist eine PAT-Datei?

Eine Datei mit der Erweiterung .pat ist eine CAD-Datei, die von der AutoCAD-Software verwendet wird. Anwendungen, die PAT-Dateien öffnen können, verwenden das in diesen Dateien gespeicherte Schraffurmuster, um Informationen über die Textur/Füllung eines Bereichs zu erhalten. Die enthaltenen Muster geben Auskunft über das Aussehen von Material an gezeichneten Objekten. PAT-Dateien können in Anwendungen wie Autodesk AutoCAD, CorelDRAW Graphics Suite und Ketron Software geöffnet werden. PAT-Dateien können in verschiedene Bildformate wie JPG, PNG, BMP usw. konvertiert werden.

## PAT-Dateiformat

PAT-Dateien sind im Nur-Text-Format geschrieben und können in jedem Texteditor geöffnet werden. Die Schraffurmuster in diesen Dateien sind vektorbasiert und folgen der in der AutoCAD-Dokumentation beschriebenen Syntax.

Alle Muster beginnen am Punkt 0,0, das Muster wird so berechnet, dass es die Schraffurgrenze abdeckt.

### Musterdefinition

Alle Musterdefinitionen bestehen aus den folgenden Feldern:
* Ein führendes '\*'
* Ein Name – Der Name darf keine Leerzeichen, Satzzeichen, Klammern oder Schrägstriche enthalten.
* Eine Beschreibung

Das Standardformat für Schraffurmuster ist `<\*><name> <, Beschreibung>`. Der Name und die Beschreibung werden durch ein Komma getrennt und Beschreibungen dürfen die Zeilenlänge von 80 Zeichen nicht überschreiten. Die Schraffurmuster werden nach diesen Informationen definiert.

### Beispiele für Schraffurmuster
Es folgt ein Beispiel für ein quadratisches Muster
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Ein weiteres Beispiel, das ein Parallelogrammmuster zeigt, ist wie folgt.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Verweise ##

* [Hash-Muster von Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

