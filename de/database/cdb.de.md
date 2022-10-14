{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "Erweiterung", "CDB-Datei", "CDB-Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Was ist eine CDB-Datei" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das CDB-Dateiformat und APIs, die CDB-Dateien erstellen und öffnen können.",
  "title" :"CDB - Konstante Datenbankdatei",
  "linktitle" :"CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Was ist eine CDB-Datei?
Die CDB-Dateien werden in geschäftskritischen Anwendungen wie E-Mail verwendet. Die CDB steht für "Constant Database", ein schnelles, zuverlässiges und einfaches Paket zum Erstellen oder Lesen konstanter Datenbanken. Der Datenbankaustausch ist sicher gegen Systemabstürze. Benutzer müssen während eines Umschreibens nicht anhalten. CDB fungiert als assoziatives Array (auf der Festplatte), ordnet Schlüssel Werten zu und ermöglicht das Speichern mehrerer Werte in einem einzigen Schlüssel.

## CDB-Dateiformat
Das CDB-Dateiformat speichert Zahlen, Offsets, Längen und Hash-Werte im Little-Endian-Format als vorzeichenlose 32-Bit-Ganzzahlen. Schlüssel und Daten werden als undurchsichtige Byte-Strings ohne besondere Behandlung betrachtet. Am Anfang der Datenbank stellt der Header mit fester Größe 256 Hash-Tabellen dar, indem er ihre Position innerhalb der Datei und ihre Länge in Slots auflistet. Normalerweise werden die Daten als Folge von Datensätzen gespeichert, wobei jeder Datensatz Schlüssellänge, Datenlänge, Schlüssel und Daten speichert. Es gibt keine Sortier- oder Ausrichtungsregeln. Den Datensätzen folgt ein Satz von 256 Hash-Tabellen unterschiedlicher Länge. Da Null eine gültige Länge ist, sind möglicherweise weniger als 256 Hash-Tabellen physisch in der Datenbank gespeichert, aber es wird nichts als 256 Tabellen betrachtet. Hash-Tabellen bestehen aus einer Reihe von Slots, von denen jeder einen Hash-Wert und einen Datensatz-Offset enthält. "Leere Slots" haben einen Offset von Null.

### Struktur
Die CDB-Datenbank besteht aus einem vollständigen Datensatz in einer einzigen Computerdatei. Es enthält drei Teile:
- Ein Header mit fester Größe
- Daten
- Eine Reihe von Hash-Tabellen.

Suchen sind nur für exakte Schlüssel verfügbar. Lookups arbeiten mit dem folgenden Algorithmus:

- Hash den Schlüssel.
- Bestimmen Sie, an welcher Hash-Tabelle und an welchem Slot sich dieser Datensatz befinden soll.
- Testen Sie den angezeigten Slot in der Hash-Tabelle.

Für Nachschlagevorgänge von Schlüsseln mit mehr als einem Wert können zusätzliche Werte gefunden werden, indem einfach die Suche am nächsten Schlitz fortgesetzt wird.

#### Merkmale

Die CDB-Datenbankstruktur bietet mehrere Funktionen:

##### Schnelle Suche
Eine erfolgreiche Suche in einer riesigen Datenbank erfordert normalerweise nur zwei Festplattenzugriffe und eine erfolglose Suche nur einen.
##### Geringer Overhead
Eine Datenbank verwendet 2048 Bytes, 24 Bytes pro Datensatz und den Platz für Schlüssel und Daten.
##### Keine zufälligen Grenzen
CDB kann jede Datenbank bis zu 4 Gigabyte verwalten. Da es keine weiteren Einschränkungen gibt, müssen die Datensätze nicht einmal in den Speicher passen. Datenbanken werden in einem maschinenunabhängigen Format gespeichert.
##### Schneller atomarer Datenbankaustausch
Der Befehl **cdbmake** kann eine ganze Datenbank in zwei Größenordnungen umschreiben, schneller als andere Hashing-Pakete.
##### Schnelle Datenbank-Dumps
**cdbdump** kann den Inhalt einer Datenbank in einem cdbmake-kompatiblen Format drucken.


## Verweise ##

* [cdb (Software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(Software))
* [CDB-Spezifikation](http://cr.yp.to/cdb.html)

