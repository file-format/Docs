{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das SQLITE-Dateiformat und APIs, die SQLITE-Dateien erstellen und öffnen können.",
  "title" :"SQLite-Dateiformat",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Was ist eine SQLite-Datei?

Eine Datei mit der Erweiterung .sqlite ist eine einfache SQL-Datenbankdatei, die mit der Software [SQLite](https://www.sqlite.org/index.html) erstellt wurde. Es ist selbst eine Datenbank in einer Datei und implementiert eine eigenständige, voll funktionsfähige, hochzuverlässige [SQL](/de/database/sql/)-Datenbank-Engine. SQLite-Datenbankdateien können verwendet werden, um umfangreiche Inhalte zwischen Systemen auszutauschen, indem diese Dateien einfach über das Netzwerk ausgetauscht werden. Fast alle Mobiltelefone und Computer verwenden SQLite zum Speichern und Teilen von Daten und ist das bevorzugte Dateiformat für plattformübergreifende Anwendungen. Aufgrund seiner kompakten Verwendung und einfachen Bedienbarkeit wird es in andere Anwendungen gebündelt geliefert. SQLite-Bindungen existieren für Programmiersprachen wie C, [C#](/de/programming/cs/), [C++](/de/programming/cpp), [Java](/de/programming/java/), [PHP](/de/programming/php/ ), und viele andere.

## SQLite-Dateiformat

SQLite ist in Wirklichkeit eine C-Language-Bibliothek, die das SQLite-RDBMS unter Verwendung des SQLite-Dateiformats implementiert. Mit der Entwicklung neuer Geräte jeden Tag wurde das Dateiformat abwärtskompatibel gehalten, um ältere Geräte aufzunehmen. Das SQLite-Dateiformat wird als Langzeitarchivierungsformat für die Daten angesehen.

### Die Datenbankdatei

Eine SQLite-Datenbank wird vollständig über zwei Dateien gepflegt.
* Hauptdatenbankdatei - Enthält den vollständigen Status der SQLite-Datenbank
* Rollback-Journal - Speichert zusätzliche Informationen in einer zweiten Datei und wird während der Durchführung von Transaktionen verwendet. Falls sich SQLite im WAL-Modus befindet, wird eine Write-Head-Protokolldatei verwaltet.

#### Journaldatei

Diese Datei dient dazu, alle Informationen aufrechtzuerhalten, falls die letzte Transaktion in Fällen wie einem Computerabsturz nicht abgeschlossen werden konnte. Diese Datei wird verwendet, um die Datenbankdatei in einem konsistenten Zustand wiederherzustellen.

#### Seiten

Die SQLite-Hauptdatenbankdatei besteht aus einer oder mehreren Seiten. Jede Seite in der Hauptdatenbank hat zu jedem Zeitpunkt eine einzige Verwendung, die eine der folgenden ist:

* Die Lock-Byte-Seite
* Eine Freelist-Seite
* Eine Freelist-Trunk-Seite
* Eine Freelist-Blattseite
* Eine B-Tree-Seite
* Eine Tabellen-B-Tree-Innenseite
* Eine Tabellen-B-Tree-Blattseite
* Eine Index-B-Tree-Innenseite
* Eine Index-B-Tree-Blattseite
* Eine Payload-Überlaufseite
* Eine Zeigerkartenseite

Die Größe von SQLite-Datenbankdateien kann von einigen Kilobyte bis zu einigen Gigabyte reichen.

### SQLite-Header

Der SQLite-Datenbank-Header befindet sich in den ersten 100 Bytes der Datenbankdatei. Jede gültige SQLite-Datenbankdatei beginnt mit 16 Bytes (in Hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Details der Header-Felder sind in der folgenden Tabelle aufgeführt.

|Offset|Größe|Beschreibung|
---|---|---|
|0|16|Die Header-Zeichenfolge: "SQLite-Format 3\000"|
|16|2|Die Größe der Datenbankseite in Bytes. Muss eine Zweierpotenz zwischen 512 und 32768 sein, oder der Wert 1, der eine Seitengröße von 65536 darstellt.|
|18|1|Dateiformat Schreibversion. 1 für Vermächtnis; 2 für WAL.|
|19|1|Dateiformat gelesene Version. 1 für Vermächtnis; 2 für WAL.|
|20|1|Bytes unbenutzter "reservierter" Platz am Ende jeder Seite. Normalerweise 0.|
|21|1|Maximaler eingebetteter Nutzlastanteil. Muss 64 sein.|
|22|1|Minimaler eingebetteter Nutzlastanteil. Muss 32 sein.|
|23|1|Blatt-Nutzlastanteil. Muss 32 sein.|
|24|4|Dateiänderungszähler.|
|28|4|Größe der Datenbankdatei in Seiten. Die "In-Header-Datenbankgröße".|
|32|4|Seitennummer der ersten Stammseite der Freelist.|
|36|4|Gesamtzahl der Freelist-Seiten.|
|40|4|Das Schema-Cookie.|
|44|4|Die Nummer des Schemaformats. Unterstützte Schemaformate sind 1, 2, 3 und 4.|
|48|4|Standardgröße des Seiten-Cache.|
|52|4|Die Seitenzahl der größten Stamm-B-Tree-Seite im Auto-Vakuum- oder Inkremental-Vakuum-Modus, andernfalls Null.|
|56|4|Die Textcodierung der Datenbank. Ein Wert von 1 bedeutet UTF-8. Ein Wert von 2 bedeutet UTF-16le. Ein Wert von 3 bedeutet UTF-16be.|
|60|4|Die "Benutzerversion", wie sie vom user_version-Pragma gelesen und gesetzt wird.|
|64|4|Wahr (nicht Null) für inkrementellen Vakuummodus. Sonst False (Null).|
|68|4|Die von PRAGMA application_id.| festgelegte "Anwendungs-ID".
|72|20|Reserviert für Erweiterung. Muss Null sein.|
|92|4|Die Gültig-für-Version-Nummer.|
|96|4|SQLITE_VERSION_NUMBER|

## Verweise ##

* [SQLite-Dateiformat - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite – C-Sprachspezifikationen](https://www.sqlite.org/c3ref/intro.html)

