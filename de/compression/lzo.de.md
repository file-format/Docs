{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Komprimiert", "Datei", "Erweiterung", "Dateiformat", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZO-Dateiformat",
  "description":"Erfahren Sie mehr über das LZO-Dateiformat und APIs, die LZO-Dateien erstellen und öffnen können.",
  "linktitle" :"LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Was ist eine LZO-Datei? ##

Eine Datei mit der Erweiterung .lzo wird mit Dateiarchivierungsfunktionen kombiniert, die die Größe aller Dateien in der komprimierten Datei verringern können. Alle komprimierten Dateien können eine oder mehrere Dateien oder sogar Ordnergruppen mit mehreren Dateien unterschiedlicher Art und Größe umfassen. Die Größe einer komprimierten Datei ist kleiner als die gemeinsame Größe aller Dateien und Ordner, die in einer komprimierten LZO-Datei gespeichert sind. Alle LZO-komprimierten Dateien werden im LZO-Format gespeichert und explizit mit Komprimierungsfunktionen ausgeführt, die von der LZOP-Dateikomprimierungs- und Dekomprimierungssoftware verwendet werden. Alle Komprimierungsspezifikationen werden in diesem Dateikomprimierungs- und Dekomprimierungsprogramm kombiniert, das aus der Lempel-Ziv-Oberhume-Dateikomprimierungsbibliothek stammt. Schnellere Dekomprimierungsgeschwindigkeit und entwickelte Komprimierungsverhältnisse werden ebenfalls in diesen LZO-Dateien kombiniert.

## LZO-Spezifikation ##

Markus Franz Xaver Johannes Oberhumer entwickelte 1996 den ursprünglichen "lzop"-Algorithmus, basierend auf früheren Algorithmen von Abraham Lempel und Jacob Ziv. Diese Bibliothek implementiert eine Vielzahl von Algorithmen mit den folgenden Eigenschaften:

* Schnellere Komprimierung als DEFLATE
* Schnelle Dekompression
* Zusätzliche Puffer, die während der Komprimierung benötigt werden (mit einer Größe von 8 KB oder 64 KB, je nach Komprimierungsstufe)
* Die Quell- und Zielpuffer sind der gesamte Speicher, der für die Dekomprimierung erforderlich ist
* Bietet Kontrolle über das Kompressionsverhältnis und die Kompressionsgeschwindigkeit

Als Blockkomprimierungsalgorithmus führt LZO sowohl eine überlappende Komprimierung als auch eine In-Place-Dekomprimierung durch. Um eine überlappende Komprimierung zu erreichen, muss die Blockgröße sowohl der Komprimierung als auch der Dekomprimierung übereinstimmen. Der LZO-Komprimierungsalgorithmus teilt die Eingabedaten in Übereinstimmungen (ein gleitendes Wörterbuch) und Literale, die nicht übereinstimmen, und liefert gute Ergebnisse mit hochgradig redundanten Daten und akzeptable Ergebnisse mit nicht komprimierbaren Daten, wobei nicht komprimierbare Daten nur um 1/64 des Originals erhöht werden Größe.

## Probleme beim Öffnen einer LZO-Datei ##

Im Folgenden sind die wenigen Probleme aufgeführt, die zu einer schlechten Funktion des LZO-Dateiformats führen können:
  


* Die Datei ist möglicherweise beschädigt. Um dieses Problem zu lösen, laden Sie die Datei erneut herunter oder bitten Sie den Absender, die Datei erneut zu senden
* Der zweite Grund ist eine infizierte Datei. In diesem Fall scannen Sie die Datei richtig
* Falsche Links zur LZO-Datei
* Entfernung der Beschreibung des LZO
* Nicht genügend Hardwareressourcen
* Veraltete Gerätetreiber
  


## Verweise ##

* [LZO – Von Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

