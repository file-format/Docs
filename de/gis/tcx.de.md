{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX-Dateiformat – Training Center XML-Datei",
  "description":"Erfahren Sie mehr über das TCX-Dateiformat und APIs, die TCX-Dateien erstellen und öffnen können.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
"identifier": "gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Was ist eine TCX-Datei?

Eine TCX-Datei (Training Center XML) ist ein Datenaustauschformat, das verwendet wird, um Daten zwischen Fitnessgeräten auszutauschen. Es wurde 2008 mit dem Produkt Training Center von Garmin eingeführt. Trainingsdaten wie Herzfrequenz, Trittfrequenz beim Laufen, Trittfrequenz beim Radfahren, Kalorien und Rundenzeit werden im Format [XML](/de/web/xml/) in der TCX-Datei gespeichert. Darüber hinaus sind in der TCX-Datei zusammenfassende Daten über die Trainingsstrecke enthalten. TCX-Dateien ähneln [FIT](/de/gis/fit/)-Dateien, die mit Garmin Sports Wearables erstellt werden.

## TCX-Dateiformat - Weitere Informationen

TCX-Dateien werden als XML-Dateien auf der Disc gespeichert, wobei jeder Datensatz als Aktivität gespeichert wird. Eine Aktivität umfasst alle Daten eines Trainings wie Zeit, Rundenzeit, Id, Herzfrequenz, Intensität, Trittfrequenz und Trackinformationen, die die Positionspaare zusammen mit dem Zeitstempel für diese Lat-Long-Position enthalten, ähnlich dem [GPX] (/de/gis/gpx/) Dateien.

### Versionen des TCX-Dateiformats

Es gibt zwei Versionen dieses Formats mit eigenen XML-Schemata, die von Garmin gehostet werden. Im Folgenden sind einige davon aufgeführt:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX-Datenprotokoll

Eine schnelle Version des TCX-XML-Formats ist auf Github als [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol) verfügbar.

## Verweise ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX-Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

