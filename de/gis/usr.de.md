{
"Datum": "03.08.2023",
  "keywords": [
"usr",
"usr-Datei",
"Was ist eine USR-Datei",
"Wie öffnet man eine USR-Datei",
"Datei",
"usr-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "USR-Dateiformat – Lowrance GPS-Datendatei",
  "description":"Erfahren Sie mehr über das USR-Format und APIs, mit denen USR-Dateien erstellt und geöffnet werden können.",
"linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
"parent": "gis"
}
},
"lastmod": "03.08.2023"
}

## Was ist eine USR-Datei?

Die Dateierweiterung ".usr" bezieht sich auch auf Lowrance GPS-Geräte. Insbesondere wird es zum Speichern von GPS-Daten in einem Format verwendet, das als "User Data Format" (USR-Format) bekannt ist und von Lowrance GPS-Geräten verwendet wird.

Wenn Sie ein Lowrance-GPS-Gerät verwenden, können Sie Ihre Wegpunkte, Tracks und Routen als ".usr"-Dateien speichern. Diese Dateien enthalten normalerweise Informationen wie Breitengrad, Längengrad, Höhe, Zeitstempel und andere Daten im Zusammenhang mit Ihren GPS-Aktivitäten.

Hier sind einige häufige Verwendungen von .usr-Dateien mit Lowrance GPS-Geräten:

- **Wegpunkte:** Wegpunkte sind bestimmte im GPS markierte Orte, z. B. Sehenswürdigkeiten, beliebte Angelplätze oder Sehenswürdigkeiten. Sie können diese Standorte als .usr-Dateien speichern und sie können importiert, exportiert oder mit anderen Lowrance GPS-Benutzern geteilt werden.

- **Tracks:** Tracks stellen den aufgezeichneten Weg Ihrer GPS-Bewegungen dar. Sie können Ihre Streckenaufzeichnungen als .usr-Dateien speichern, sodass Sie Ihre Routen später überprüfen und analysieren oder sie mit anderen teilen können.

- **Routen:** Routen sind vordefinierte Pfade, die Sie erstellen und auf Ihrem GPS-Gerät speichern können. Diese Routen können auch als .usr-Dateien zur späteren Verwendung oder Weitergabe gespeichert werden.

Um .usr-Dateien auf Ihrem Lowrance-GPS-Gerät zu verwalten, verwenden Sie normalerweise Software wie "Insight Planner" oder "Lowrance GPS Utility" von Lowrance, um Ihre GPS-Daten zu importieren, zu exportieren und zu bearbeiten.

## USR-Dateiformat – Weitere Informationen

Bei Lowrance iFinder GPS-Geräten werden die .usr-Dateien erstellt und auf der im Gerät eingesetzten MultiMediaCard (MMC)-Speicherkarte gespeichert. Diese Dateien enthalten Benutzerdaten wie Wegpunkte, Tracks und Routen.

Um die .usr-Dateien von der MMC auf einen Computer zu übertragen, können Sie die folgenden Schritte ausführen:

- **Entfernen Sie die MMC:** Entfernen Sie vorsichtig die MultiMediaCard (MMC) aus dem Lowrance iFinder GPS-Gerät.

- **MMC in den Computer einlegen:** Verwenden Sie einen geeigneten MMC-Kartenleser, um die Speicherkarte in den Kartenlesersteckplatz Ihres Computers einzuführen.

- **.usr-Dateien suchen:** Sobald die MMC von Ihrem Computer erkannt wird, sollten Sie auf die darauf gespeicherten Dateien zugreifen können. Suchen Sie nach den .usr-Dateien, die Ihre GPS-Daten enthalten.

- **Konvertierung mit GPSBabel:** Um die .usr-Dateien in ein anderes GPS-Format zu konvertieren, können Sie GPSBabel verwenden, ein kostenloses Open-Source-Tool für die Arbeit mit verschiedenen GPS-Dateiformaten. GPSBabel unterstützt eine Vielzahl von Eingabe- und Ausgabeformaten, sodass Sie die .usr-Dateien in Formate konvertieren können, die mit anderer GPS-Software oder -Geräten kompatibel sind.

Sie können GPSBabel von der offiziellen Website (http://www.gpsbabel.org/) herunterladen und auf Ihrem Computer installieren. Nach der Installation können Sie die Konvertierung über die Befehlszeilenschnittstelle oder die grafische Benutzeroberfläche (sofern verfügbar) der Software durchführen.

Wenn Sie beispielsweise .usr-Dateien in das GPX-Format konvertieren möchten, können Sie einen Befehl wie den folgenden verwenden:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Der obige Befehl weist GPSBabel an, die Eingabedatei "input.usr" im Lowrance USR-Format zu lesen und die Ausgabedatei "output.gpx" im GPX-Format zu schreiben.

- **Konvertierte Dateien importieren/verwenden:** Nach der Konvertierung liegen Ihre GPS-Daten im neuen Format (z. B. GPX) vor, das Sie mit anderer GPS-Software oder Geräten verwenden können, die dieses Format unterstützen.

## Wie öffne ich eine USR-Datei?

Zu den Programmen, die USR-Dateien öffnen oder darauf verweisen, gehören:

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Verweise
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)

