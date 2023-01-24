{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das OSZ-Dateiformat und APIs, die OSZ-Dateien erstellen und öffnen können.",
  "title" :"OSZ-Datei - osu! Beatmap-Dateiformat",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Was ist eine OSZ-Datei?

Eine OSZ-Datei ist ein komprimiertes Dateiformat, das vom Rhythmusspiel osu! um Beatmap-Daten zu speichern. Beatmaps sind im Wesentlichen Ebenen für das Spiel und enthalten Informationen wie den Song, das Beat-Timing und die Platzierung von getroffenen Objekten auf dem Spielbildschirm. OSZ-Dateien ermöglichen eine einfache Verteilung von Beatmaps und werden normalerweise aus dem Internet heruntergeladen und in das Spiel importiert. OSU! hat auch das Dateiformat [OSR](/de/game/osr/), das eine Spielwiederholungsdatei ist und von Spielern wiedergegeben werden kann.

**MIME-Typ des OSR-Dateiformats:** x-osu-replay

## OSZ-Dateiformat

Die internen Dateiformatdetails von OSZ-Dateitypen sind nicht öffentlich verfügbar. Es enthält [ZIP](/de/compression/zip/)-komprimierte Daten mit Informationen zum Abspielen der Musik, zum Anzeigen von Grafiken und zum Anzeigen von Spielern über die Ereignisse, wenn sie mit dem Spiel interagieren müssen.

## Wie erstelle ich eine OSZ-Datei?

OSU! enthält detaillierte Anweisungen zum [Erstellen von OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files
) und OSK-Dateien. Die folgenden Schritte können verwendet werden, um eine OSZ-Datei mit OSU! zu erstellen.

1. Öffnen Sie eine Beatmap über den Editor.
1. Wählen Sie im oberen Menü Datei > Paket exportieren....
1. Das .osz-Archiv wird im Ordner „Exports“ im osu abgelegt! Mappe.

## Verweise

* [OSU! Rhythmusspiel](https://osu.ppy.sh/home)
* [OSZ-Dateiformat](https://osu.ppy.sh/wiki/en/Client/File_formats/Osz_%28file_format%29https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format %29#Datentypen)

