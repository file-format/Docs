{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FIT-Dateiformat - Garmin-Aktivitätsdatei",
  "description":"Erfahren Sie mehr über das FIT-Dateiformat und APIs, die FIT-Dateien erstellen und öffnen können.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Was ist eine FIT-Datei?

Eine FIT-Datei ist eine GIS-Datei, die von Garmin Sports Wearables erstellt wurde. Es wird verwendet, um die Aktivitäten der Person aufzuzeichnen, wenn sie sich mit diesen Geräten bewegt. Die Aktivitätsdaten umfassen Ort und Zeit, wie sie vom GPS-Gerät aufgezeichnet wurden. FIT-Dateien werden auch verwendet, um die aufgezeichneten Aktivitätsdaten mithilfe von Web-APIs zu übertragen. Aus diesem Grund sind FIT-Dateien das am häufigsten verwendete Dateiformat für den Austausch von Fitnessdaten mit anderen Fitnessplattformen. Andere gängige Dateiformate sind [GPX](/de/gis/gpx/), TCX und [KML](/de/gis/kml/).

## FIT-Dateiformat – Weitere Informationen

FIT-Dateien werden als Binärdateien mit den von den Garmin-Geräten für die Aktivität aufgezeichneten Informationen auf der Disc gespeichert. Zu den in einer FIT-Datei gespeicherten Informationen gehören:

* Terminzeit
* Sportarten
* Runden- und Zwischenzeitdaten
* GPS-Track
* Sensordaten
* Ereignisse für aktive Sitzung

Aktivitätsdaten können in Echtzeit in der Datei aufgezeichnet oder nach Abschluss der Aktivitätsaufzeichnung exportiert werden.

### FIT-Aktivitätsmeldungen

Eine FIT-Aktivitätsdatei kann einige erforderliche Nachrichtentypen enthalten. Im Folgenden sind die erforderlichen Nachrichten für eine Aktivitätsdatei aufgeführt.

|Nachricht|Zweck|
---|---|
|Datei-ID| Die Datei-ID-Nachricht wird von allen FIT-Dateitypen benötigt und ist voraussichtlich die erste Nachricht in der Datei. Für Aktivitätsdateien sollte die Type-Eigenschaft auf 4.| gesetzt werden
|Aktivität| In einer FIT-Aktivitätsdatei ist eine einzelne Aktivitätsnachricht erforderlich. In der Aktivitätsnachricht sind die Eigenschaften Local Timestamp und Session Count enthalten. Der lokale Zeitstempel wird verwendet, um den Zeitzonenoffset zu bestimmen, der auf alle Zeitstempel in der Datei angewendet werden kann. Die meisten Geräte zeichnen FIT-Dateien in Echtzeit auf und die Anzahl der Sitzungen ist bis zum Ende der Aufzeichnung unbekannt. Aus diesem Grund ist die Aktivitätsnachricht oft die letzte Nachricht in der Datei.|
|Sitzung| Aktivitätsdateien enthalten eine oder mehrere Sitzungsnachrichten. Eine Sitzungsnachricht ist ein zusammenfassender Nachrichtentyp. Startzeit, Verstrichene Gesamtzeit, Timer-Gesamtzeit und Zeitstempel sind Pflichtfelder für alle zusammenfassenden Meldungen.|
|Runde| Rundenmeldungen stellen Runden oder Intervalle innerhalb der Sitzung dar. Eine Rundennachricht ist ein zusammenfassender Nachrichtentyp. Startzeit, Verstrichene Gesamtzeit, Timer-Gesamtzeit und Zeitstempel sind Pflichtfelder für alle zusammenfassenden Meldungen.|
|Aufnahme| Zu den aufgezeichneten Nachrichten gehören GPS-Koordinaten, Geschwindigkeit, Entfernung, Herzfrequenz, Leistung usw.|

## Nützliche Ressourcen für die FIT-Datei

* [Decodieren von FIT-Aktivitätsdateien](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Codieren von FIT-Aktivitätsdateien](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Verweise ##

* [FIT-Aktivitätsdatei] (https://developer.garmin.com/fit/file-types/activity/)

