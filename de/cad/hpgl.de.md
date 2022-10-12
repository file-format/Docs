{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Dateiformat", "Öffnen", "Lesen", "Erstellen", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das HPGL-Dateiformat und APIs, die HPGL-Dateien erstellen und öffnen können.",
  "title" :"HPGL-Dateiformat - Lernen Sie von Dateiformatexperten!",
  "linktitle" :"HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Was ist eine HPGL-Datei?

Eine HPGFL-Datei (Hewlett-Packard Graphics Language) enthält einen von HP entwickelten Befehlssatz für die Plottersteuerung. HP-Plotter verwenden diese Datei zum Zeichnen und Drucken von Vektor- und Rasterinhalten auf dem Papier.

### HPGL-Befehl

Ein HPGL-Befehl besteht aus Folgendem.
* Ein Befehlsabschnitt des Alphabets aus zwei Zeichen
* Ein Parameterabschnitt
* Terminator-Sektion

Bei mehreren Parametern muss jeder Parameter in der Datei durch ein Trennzeichen getrennt werden.

### HPGL-Befehlsbeispiel

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Koordinatensystem

Koordinatensysteme bestehen aus zweidimensionalen Messindikatoren, um einen bestimmten Ort zu lokalisieren. Die HPGL verwendet zu diesem Zweck sowohl das Plotterkoordinaten- als auch das Benutzerkoordinatensystem.

#### Plotterkoordinatensystem

Dieses Koordinatensystem wird verwendet, um Zeichnungen basierend auf der Plotterbewegung zu plotten. Eine typische XY-Einheit der minimalen Plotterbewegung ist 0,025 mm. Der mögliche Zeichnungsbereich ändert sich bei Plotterarten.

#### Benutzerkoordinatensystem

Ein benutzerdefiniertes Koordinatensystem kann unter Verwendung von Maßstab und Ursprung eingerichtet werden. Diese werden mit dem IP-Befehl und dem SC-Befehl in Plotterkoordinaten umgewandelt. Ohne diese Umrechnung werden standardmäßig Plottersystemkoordinaten verwendet.

## HPGL-Dateiformat
HPGL-Dateien sind im ASCII-Format (Textdatei) und beginnen mit wenigen Setup-Befehlen. Dies richtet bestimmte Parameter für den Plotter zum Plotten ein. Eine typische HPGL-Datei sieht wie folgt aus.

|Befehl|Bedeutung
---|---|
|IN;|initialisieren, Plotauftrag starten|
|IP;|setzen Sie die Skalierungspunkte (P1 und P2) auf ihre Standardpositionen|
|SP1;|Stift 1 auswählen|
|PU0,0;|Stift nach oben heben und zum Startpunkt für die nächste Aktion bewegen|
|PD100,0,100,100,0,100,0,0;|Legen Sie den Stift ab und bewegen Sie sich zu den folgenden Stellen (ziehen Sie einen Rahmen um die Seite)|
|PU50,50;|Stift nach oben und zu den X-, Y-Koordinaten 50,50| bewegen
|CI25;|zeichne einen Kreis mit Radius 25|
|SS;|Wählen Sie den Standardzeichensatz|
|DT*,1;|Setze das Texttrennzeichen auf das Sternchen und drucke sie nicht (die 1, was "wahr" bedeutet)|
|PU20,80;|den Stift anheben und auf 20,80 bewegen|
|LBHallo Welt*;|eine Beschriftung zeichnen|

## Verweise
* [HPGL von Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [HPGL-Referenzhandbuch](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

