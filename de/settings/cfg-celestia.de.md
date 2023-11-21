{
"Datum": "27.09.2023",
  "keywords": [
"cfg",
"cfg-Datei",
"cfg celestia Konfigurationsdatei",
"Was ist eine CFG-Datei",
"Wie öffnet man eine CFG-Datei",
"Datei",
"cfg-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CFG-Dateiformat – Celestia-Konfigurationsdatei",
  "description":"Erfahren Sie mehr über das CFG Celestia-Konfigurationsdateiformat und die APIs, mit denen CFG-Dateien erstellt und geöffnet werden können.",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent": "Einstellungen"
}
},
"lastmod": "27.09.2023"
}

## Was ist eine CFG-Datei?

Eine Celestia-Konfigurationsdatei ist eine reine Textdatei, die von Celestia, dem 3D-Universumssimulationsprogramm, verwendet wird. Diese Dateien sind wichtig für die Anpassung des Verhaltens von Celestia, der angezeigten Himmelsobjekte und der Darstellung des Programms. Die Bearbeitung dieser Dateien erfordert jedoch sorgfältige Aufmerksamkeit, da unsachgemäße Änderungen den Ladevorgang von Celestia unterbrechen und die ordnungsgemäße Ausführung verhindern können.

## Celestia

Celestia ist eine kostenlose Open-Source-3D-Astronomie-Simulationssoftware, die es Benutzern ermöglicht, das Universum auf äußerst realistische und interaktive Weise zu erkunden und zu visualisieren. Es wurde von Chris Laurel entwickelt und erstmals Anfang der 2000er Jahre veröffentlicht. Celestia ist für die Betriebssysteme Windows, macOS und Linux verfügbar.

Zu den wichtigsten Funktionen und Aspekten von Celestia gehören:

- **Realistische 3D-Visualisierung:** Celestia bietet eine detaillierte und genaue Darstellung unseres Sonnensystems sowie von Sternen, Galaxien und anderen Himmelsobjekten. Es verwendet hochwertige 3D-Modelle und Texturen, um ein visuell beeindruckendes Erlebnis zu schaffen.

- **Umfangreiche Himmelsdatenbank:** Die Software verfügt über eine umfangreiche integrierte Datenbank bekannter Himmelsobjekte, darunter Sterne, Planeten, Monde, Asteroiden, Kometen und Raumfahrzeuge. Benutzer können diese Objekte leicht lokalisieren und erkunden.

- **Wissenschaftliche Genauigkeit:** Obwohl Celestia ein Visualisierungstool ist, zielt es darauf ab, Himmelsobjekte und -phänomene auf der Grundlage verfügbarer wissenschaftlicher Daten so genau wie möglich darzustellen.

## Von Celestia verwendete Dateiformate

Celestia nutzt verschiedene Dateiformate für verschiedene Aspekte seiner 3D-Astronomiesimulation. Hier sind einige der wichtigsten von Celestia verwendeten Dateiformate:

1. **Konfigurationsdateien (.cel)**
- *Beschreibung*: Nur-Text-Dateien, die es Benutzern ermöglichen, das Verhalten, das Erscheinungsbild und den Inhalt von Celestia anzupassen.
- *Zweck*: Anpassen von Einstellungen, Definieren von Standorten und Spezifizieren von Himmelsobjekten.

2. **3D-Modelle und Netze**
- *Formate*: [.3ds](/3d/3ds/), [.obj](/3d/obj/), [.dae](/3d/dae/), .ac
- *Beschreibung*: Unterstützte 3D-Modelldateiformate, die zum Rendern von Himmelskörpern und Raumfahrzeugen verwendet werden.
- *Zweck*: Anzeige von 3D-Objekten in Celestia.

3. **Texturdateien**
- *Formate*: [.jpg](/image/jpeg/), [.png](/image/png/), [.dds](/image/dds/)
- *Beschreibung*: Diese Dateien stellen Oberflächentexturen für Himmelskörper bereit.
- *Zweck*: Texturen auf 3D-Modelle abbilden, um ein realistisches Erscheinungsbild zu erzielen.

4. **Star-Kataloge und Datendateien**
- *Formate*: Benutzerdefinierte Formate, [.csv](/spreadsheet/csv/), [.tsv](/spreadsheet/tsv/)
- *Beschreibung*: Datendateien zur Darstellung von Sternen und anderen Himmelsobjekten, um eine genaue Simulation zu gewährleisten.
- *Zweck*: Genaue Darstellung von Himmelsobjekten.

5. **Texturwürfelkarten**
- *Beschreibung*: Würfelkarten werden verwendet, um das Aussehen entfernter Himmelsobjekte wie Galaxien zu simulieren.
- *Zweck*: Entfernte Objekte mit realistischen Texturen rendern.

6. **Skriptdateien**
- *Beschreibung*: Diese Dateien enthalten benutzerdefinierte Skripte, die in der Skriptsprache von Celestia geschrieben sind.
- *Zweck*: Benutzern die Erstellung dynamischer Ereignisse und Animationen im Celestia-Universum ermöglichen.

## Celestia-Konfigurationsdatei

Hier ist ein grundlegender Überblick darüber, was Sie mit der Celestia-Konfigurationsdatei tun können:

1. **Festlegen Ihres Standorts**: Sie können Ihren Standort auf der Erde mithilfe der Parameter Breitengrad, Längengrad und Höhe angeben. Dadurch kann Celestia den Nachthimmel von Ihrer Position aus genau anzeigen.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Anpassen Ihrer Anzeigeoptionen:** Sie können verschiedene Anzeigeoptionen wie Sichtfeld, Zeiteinstellungen und Rendering-Einstellungen anpassen.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Himmelsobjekte laden:** Sie können Ihrer Simulation Himmelsobjekte wie Sterne, Planeten, Asteroiden, Raumschiffe und mehr hinzufügen. Jedes Objekt ist in der Konfigurationsdatei mit seinen Eigenschaften definiert.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Raumschiffe definieren:** Sie können Ihr eigenes fiktives Raumschiff erstellen oder echte Raumschiffe verwenden, indem Sie deren Parameter wie Position, Ausrichtung und 3D-Modelle angeben.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Skripte erstellen:** Sie können Skripte in der benutzerdefinierten Skriptsprache von Celestia schreiben, um dynamische Ereignisse und Animationen zu erstellen.

## Wie öffne ich eine CFG-Datei?

Programme, die CFG-Dateien öffnen oder darauf verweisen

- Celestia (kostenlos) für (Windows, Mac, Linux)

## Andere CFG-Dateien

Hier sind andere Dateitypen, die die Dateierweiterung **.cfg** verwenden.

**Einstellungen**
- [CFG – Celestia-Konfigurationsdatei](/settings/cfg-celestia/)
- [CFG – Citrix Server-Verbindungsdatei](/settings/cfg-citrix/)
- [CFG – MAME-Konfigurationsdatei](/settings/cfg-mame/)
- [CFG – LightWave-Konfigurationsdatei](/settings/cfg-lightwave/)

**Spiel**
- [CFG – Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG – MUGEN-Konfigurationsdatei](/game/cfg-mugen/)
- [CFG – Quell-Engine-Konfigurationsdatei](/game/cfg-sourceengine/)

**System & Sonstiges**
- [CFG – CFG-Datei](/system/cfg/)
- [CFG – Cal3D-Modellkonfigurationsdatei](/misc/cfg-cal3d/)

## Verweise
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

