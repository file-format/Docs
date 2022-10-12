{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "Erweiterung", "Datei", "Format", "System", "TMP-Datei", "TMP-Dokumente", "TMP-Dateien", "Temporäre Datei", "Anwendung", "Programme" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Temporäres Dateiformat",
  "description":"Erfahren Sie mehr über das TMP-Dateiformat und APIs, die TMP-Dateien erstellen und öffnen können.",
  "linktitle" :"TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Was ist eine TMP-Datei? ##

Eine TMP-Datei bezieht sich auf eine vorübergehende Sicherung, Speicherung oder ein anderes Dateisystem, das von einem Softwareprogramm generiert wird. Sie wird gelegentlich als unsichtbare Datei angelegt und häufig beim Beenden des Programms zerstört. TMP-Dateien können auch verwendet werden, um Informationen vorübergehend zu speichern, während eine neue Datei erstellt wird.

## TMP-Dateiformat ##

Eine TMP-Datei besteht normalerweise aus Rohdaten, die als Phase im Konvertierungsprozess von Material von einem Stil in einen anderen verwendet werden. Microsoft Word und Apple Safari sind zwei Apps, die das TMP-Dateiformat erzeugen und verwenden können.

Generierte TMP-Dokumente sollten theoretisch automatisch entfernt werden, wenn das Programm geschlossen oder die Maschine ausgeschaltet wird. In der Praxis ist dies nicht immer der Fall. Daher können Sie beim Navigieren durch die Dokumente Ihres Programms auf vorübergehende Dateien stoßen, die nicht aktiv vom System oder anderer Software verwendet werden.

### Hilfsspeicher ###

Virtueller Speicher wird in Betriebssystemen verwendet, Programme, die große Mengen an Informationen verwenden, müssen jedoch möglicherweise temporäre Dokumente erstellen.

### Interprozesskommunikation ###

Die meisten Betriebssysteme bieten Grundelemente zum Übertragen von Daten zwischen Programmen, wie Pipes, Sockets oder Hauptspeicher, aber die einfachste Methode besteht darin, Dateien in eine temporäre Datei zu übertragen und der empfangenden Anwendung den Speicherort der temporären Datei mitzuteilen.


## Technische Spezifikation ##

Das Erhalten von unverwechselbaren temporären Dokumentnamen wird normalerweise von Betriebssystemen und Softwareprogrammen bereitgestellt.
Temporäre Dateien können auf POSIX-Systemen mit den mkstemp- oder tmpfile-Bibliotheksfunktionen sicher generiert werden. Einige Systeme enthalten die frühere POSIX-Anwendung mktemp (seitdem nicht mehr vorhanden). Diese Dateien befinden sich normalerweise im regulären temporären Verzeichnis auf Unix-Plattformen in /TMP oder %TEMP% (es ist spezifisch für die Anmeldung) auf Windows-Rechnern.

Wenn das Programm beendet oder das Dokument geschlossen wird, wird die mit der tmpfile generierte transiente Datei automatisch entfernt. GetTempFileName (Windows) oder tmpnam (POSIX) können verwendet werden, um einen temporären Dateinamen zu erstellen, der länger hält als das Programm, das ihn erstellt hat.

## Bezug ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
