{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE-Datei – Was ist eine .gcode-Datei und wie öffnet man sie?",
   "description":"Erfahren Sie mehr über das GCODE-Dateiformat und APIs, mit denen GCODE-Dateien erstellt und geöffnet werden können.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## Was ist eine GCODE-Datei?

Eine **GCODE-Datei** ist eine reine Textdatei, die Anweisungen zur Steuerung computergestützter Werkzeugmaschinen und 3D-Drucker enthält; G-Code oder Geometrischer Code ist eine Sprache, die zur Steuerung von Bewegungen und Aktionen von **CNC-Maschinen (Computer Numerical Control)** verwendet wird; Zu den CNC-Maschinen zählen Fräsmaschinen, Drehmaschinen, Oberfräsen und 3D-Drucker.

G-Code-Befehle werden in einer bestimmten Syntax geschrieben, die typischerweise aus Buchstaben und Zahlen besteht; Jeder Befehl weist die Maschine an, eine bestimmte Aktion auszuführen, z. B. das Werkzeug in eine bestimmte Position zu bewegen, das Werkzeug zu wechseln oder die Geschwindigkeit anzupassen.

G-Code wird oft mit **CAM-Software (Computer-Aided Manufacturing)** generiert; CAM-Software nimmt 3D-Modelle oder 2D-Entwürfe und generiert entsprechende Werkzeugwege und G-Code-Anweisungen; Die G-Code-Datei wird dann zur Ausführung in eine CNC-Maschine oder einen 3D-Drucker geladen.

G-Code-Dateien haben normalerweise die Dateierweiterung .nc oder .gcode, zum Beispiel program.nc oder print.gcode.

## GCODE-Dateistruktur:

GCODE-Dateien sind reine Textdateien, in denen jede Zeile einen bestimmten Befehl enthält. Diese Befehle reichen von der Steuerung der Maschinenbewegung bis zur Einstellung von Temperatur, Geschwindigkeit und anderen Parametern, die für die Herstellung eines Objekts entscheidend sind.

Die Syntax von GCODE umfasst eine Kombination aus Buchstaben und Zahlen; jedes stellt eine bestimmte Aktion oder einen bestimmten Parameter dar; Zu den gängigen Befehlen gehören G0 und G1 für die Bewegung, M3 und M5 für die Spindelsteuerung sowie S und F für die Geschwindigkeits- bzw. Vorschubgeschwindigkeitsanpassung.

## GCODE-Generierung:

Slicing-Software wie **Simplify3D** und **Slic3r** übersetzt CAD-Zeichnungen (Computer-Aided Design) in GCODE; Mithilfe von CAD-Software werden 3D-Modelle erstellt, die dann in Formate wie STL exportiert werden. Die Slicing-Software nimmt diese Modelle und generiert eine GCODE-Datei, die Details wie Schichthöhe, Druckgeschwindigkeit und Temperatureinstellungen angibt.

## GCODE-Beispiel

Hier ist ein einfaches Beispiel für einen G-Code zum Bewegen einer CNC-Maschine:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## Wie öffne ich eine GCODE-Datei?

Zum Öffnen einer G-Code-Datei können Sie je nach Bedarf verschiedene Arten von Software verwenden.

Wenn Sie einen G-Code für den 3D-Drucker generiert haben; Sie können es mit der Software öffnen, die mit Ihrem 3D-Drucker geliefert wurde, oder mit einer speziellen Schneidesoftware. Beispiele sind **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** oder **Repetier-Host**; Diese Programme verfügen häufig über eine benutzerfreundliche Oberfläche, mit der Sie G-Code laden und visualisieren können.

GCODE-Dateien sind reine Textdateien, sodass Sie sie mit jedem Texteditor öffnen können. Zu den gängigen Texteditoren gehören **Notepad (unter Windows)**, **TextEdit (unter macOS)** oder **Gedit (unter Linux)**; Klicken Sie einfach mit der rechten Maustaste auf die G-Code-Datei, wählen Sie Öffnen mit und wählen Sie einen Texteditor aus.

