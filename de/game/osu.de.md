{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das OSU-Dateiformat und APIs, die OSU-Dateien erstellen und öffnen können.",
  "title" :"OSU-Datei - Osu! Skriptdateiformat",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Was ist eine OSU-Datei?

Eine OSU-Datei ist ein Spielskript, das für osu geschrieben wurde! Rhythmus-Spiel. Es enthält Informationen über eine im Spiel verwendete Beatmap, wie z. B. den Schwierigkeitsgrad, das zu spielende Lied und das Timing der getroffenen Objekte, mit denen sich der Spieler mit der Musik synchronisieren muss. Es ermöglicht Rhythmusspielern, benutzerdefinierte Herausforderungen zu entwickeln und mit der Spielgemeinschaft zu teilen.

**MIME-Typ des OSR-Dateiformats:** x-osu-beatmap

## OSU-Dateiformat

OSU-Dateien werden als reine Textdateien auf Disc gespeichert und ihre Struktur ist sehr klar im [OSU-Dateiformat](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) von definiert oh!.

### Abschnitte in der OSU-Datei

Eine typische OSU-Datei hat die folgenden Abschnitte.

|Abschnitt |Beschreibung |Inhaltstyp|
---|---|---|
|[Allgemein]| Allgemeine Informationen zur Beatmap| Schlüssel: Wertepaare|
|[Herausgeber]| Gespeicherte Einstellungen für den Beatmap-Editor| Schlüssel: Wertepaare|
|[Metadaten] |Informationen zur Identifizierung der Beatmap| Schlüssel:Wert-Paare|
|[Schwierigkeit] |Schwierigkeitseinstellungen| Schlüssel:Wert-Paare|
|[Ereignisse]| Beatmap- und Storyboard-Grafikereignisse| Kommagetrennte Listen|
|[TimingPoints]| Zeitmessung und Kontrollpunkte| Kommagetrennte Listen|
|[Farben]| Kombi- und Hautfarben| Schlüssel : Wertepaare|
|[Trefferobjekte]| Objekte treffen| Kommagetrennte Listen|

## Verweise

* [OSU! Rhythmusspiel](https://osu.ppy.sh/home)
* [OSU-Dateiformat](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)

