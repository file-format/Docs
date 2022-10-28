{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MK3D-Dateiformat",
  "keywords" :[ "mk3d", "matroska video", "mkv format", "stereoscopic 3d", "StereoMode", "video", "file", "format" ],
  "description":"Erfahren Sie mehr über das MK3D-Dateiformat für stereoskopische 3D-Videos, die von Matroska erstellt wurden, und APIs, die MK3D-Dateien erstellen und öffnen können.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Was ist eine MK3D-Datei? ##

Die MK3D-Dateien gehören zur Familie der Matroska-Videoformate. Diese Dateien sind eigentlich **stereoskopische 3D**-Videos, die im Matroska 3D-Format erstellt wurden. Der MKV-Dateicontainer verwendet den Wert eines StereoMode-Felds, um den Typ des stereoskopischen 3D-Videomaterials zu definieren. Ein StereoMode-Wert ist auch verfügbar, um die alten Stereo-3D-Videos anzuzeigen, indem die Farben Cyan und Rot getrennt werden (AnaGlyph).

## Technische Details ##
Die 3D-Videos können auf zwei Arten komprimiert werden:

- Separate Spur für jedes Auge.
- Kombinieren Sie jedes Eyetracking zu einem einzigen Track.

Der MKV-Dateicontainer unterstützt beides.

Für die Single-Track-Videos, die mit dem darin enthaltenen 3D-Material einfacher sind, müssen Sie das Feld **StereoMode** einstellen, das entscheidet, ob die Flugzeuge in der Mono- oder in der Links-Rechts-Kombinationsspur montiert werden. Sie können einen der folgenden StereoMode-Feldwerte verwenden:

|Wert | Beschreibung |
|---|---|
|0| mono|
|1| nebeneinander (linkes Auge zuerst)|
|2| oben-unten (rechtes Auge zuerst)|
|3| oben-unten (linkes Auge zuerst)|
|4| Schachbrett (rechts ist zuerst)|
|5| Schachbrett (links ist zuerst)|
|6| Reihe verschachtelt (rechts ist zuerst)|
|7| Reihe verschachtelt (links ist zuerst)|
|8| Spalte verschachtelt (rechts ist zuerst)|
|9| Spalte verschachtelt (links ist zuerst)|
|10| Anaglyph (Cyan/Rot)|
|11| nebeneinander (rechtes Auge zuerst)|
|12| Anaglyph (grün/magenta)|
|13| beide Augen in einem Block geschnürt (linkes Auge zuerst) (Feldsequenzmodus)|
|14| beide Augen in einem Block geschnürt (rechtes Auge zuerst) (Feldsequenzmodus)|

Für die mehreren Spuren muss der MKV-Container die Funktionalität jeder Spur separat entscheiden. Die **TrackOperation** mit **TrackCombinePlanes** werden verwendet, um die Arbeit zu erledigen.


## Verweise ##

- [Matroska-Spezifikationshinweise] (https://www.matroska.org/technical/notes.html)
- [MKV File Container Support for Stereo 3D Video and the MK3D Files](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d- Dateien/)

