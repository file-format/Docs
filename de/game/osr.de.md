{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das OSR-Dateiformat und APIs, die OSR-Dateien erstellen und öffnen können.",
  "title" :"OSR-Datei - osu! Replay-Dateiformat",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Was ist eine OSR-Datei?

Eine OSR-Datei ist eine Spielwiedergabedatei, die vom [osu! Spiel] (https://osu.ppy.sh/home). Okay! ist ein Rhythmusspiel, bei dem Benutzer Mausklicks mit der Musik abgleichen. Das vom Benutzer gespielte Lied, Hits und Misses, Zeit und Datum des gespielten Lieds und die Gesamtrangliste werden in der OSR-Datei aufgezeichnet. Diese OSR-Datei kann dann für Wiedergabezwecke mit anderen geteilt werden. Für die OSR-Datei muss die Beatmap-Datei im Ordner „Songs“ vorhanden sein.

**MIME-Typ des OSR-Dateiformats:** x-osu-replay

## OSR-Dateiformat

OSR-Dateien werden als Binärdateien mit Datenfeldern fester und variabler Länge gespeichert.

|Datentyp| Formatieren|
---|---|
|Byte |Spielmodus des Replays (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Integer |Version des Spiels, als die Wiederholung erstellt wurde (z. B. 20131216)|
|String |osu! Beatmap-MD5-Hash|
|Zeichenfolge| Spielername|
|Zeichenfolge| oh! Wiedergabe-MD5-Hash (enthält bestimmte Eigenschaften der Wiedergabe)|
|Kurz| Anzahl der 300er|
|Kurz| Anzahl der 100er in Standard, 150er in Taiko, 100er in CTB, 100er in Mania|
|Kurz| Anzahl der 50er in Standard, kleine Früchte in CTB, 50er in Manie|
|Kurz| Anzahl der Gekis im Standard, Max 300s im Wahnsinn|
|Kurz| Anzahl der Katus im Standard, 200er im Wahnsinn|
|Kurz| Anzahl der Fehlschüsse|
|Ganzzahl| Im Ergebnisbericht angezeigte Gesamtpunktzahl|
|Kurz| Größte Combo, die im Score-Bericht angezeigt wird|
|Byte| Perfekte/vollständige Kombination (1 = keine Fehler und keine Slider-Brüche und keine vorzeitig beendeten Slider)|
|Ganzzahl| Mods verwendet. Unten finden Sie eine Liste der Mod-Werte.|
|Zeichenfolge| Lebensbalkendiagramm: durch Komma getrennte Paare u/v, wobei u die Zeit in Millisekunden seit Beginn des Songs und v ein Fließkommawert von 0 bis 1 ist, der die Menge an Leben darstellt, die Sie zum gegebenen Zeitpunkt haben (0 = Lebensbalken ist leer, 1=Lebensbalken ist voll)|
|Lang| Zeitstempel (Windows-Ticks)|
|Ganzzahl| Länge der komprimierten Wiedergabedaten in Bytes|
|Byte |Array Komprimierte Wiedergabedaten|
|Lang| Online-Ergebnis-ID|
|Doppelt| Zusätzliche Mod-Informationen. Nur vorhanden, wenn Target Practice aktiviert ist.|

## Verweise

* [OSU! Rhythmusspiel](https://osu.ppy.sh/home)
* [OSR-Dateiformat](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)

