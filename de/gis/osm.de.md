{
  "date" : "2019-10-11",
  "keywords" :[ "osm-Datei", "was ist eine osm-Datei", "Datei", "osm-Beispiel", "osm-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - OpenStreetMap-Dateiformat",
  "description":"Erfahren Sie mehr über das OSM-Dateiformat und APIs, die OSM-Dateien erstellen und öffnen können.",
  "linktitle" :"OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine OSM-Datei?

OpenStreetMap (OSM) ist eine riesige Sammlung von freiwilligen geografischen Informationsspeichern in verschiedenen Dateitypen, die verschiedene Codierungsschemata verwenden, um diese Daten in Bits und Bytes umzuwandeln. OSM ist eine gemeinsame Anstrengung zur Erstellung einer frei editierbaren Weltkarte. Das primäre Ergebnis dieser Zusammenarbeit sind geografische Daten und nicht die Karte selbst. Die Einschränkungen bei der Verwendung oder Verfügbarkeit von geografischen Informationen in weiten Teilen der Welt lösen die Notwendigkeit aus, ein OSM zu erstellen. Die von OSM verfügbaren Daten sind bereit, Google Maps für klassische Anwendungen (Facebook, Craigslist usw.) und Standarddaten für Anwendungen von GPS-Empfängern zu ersetzen.^^ ^^Obwohl die Datenqualität weltweit unterschiedlich ist, können OpenStreetMap-Daten bequem mit Patenten verglichen werden Datenquellen.

## Kurze Geschichte ##

Inspiriert vom Erfolg von Wikipedia hat Steve Coast, ein britischer Unternehmer, 2004 dieses Community-basierte Weltkartierungsprojekt in Großbritannien ins Leben gerufen. Er konzentrierte sich zunächst auf die Kartierung des Vereinigten Königreichs. Die OpenStreetMap Foundation wurde erstmals im April 2006 gegründet, um die Entwicklung, Erweiterung und Verbreitung kostenloser Geodaten für jedermann zu unterstützen. Im Dezember 2006 unterstützte Yahoo OpenStreetMap mit seinen Luftaufnahmen für die Kartenproduktion. Vollständige Straßendaten für die Niederlande und Fernstraßendaten für Indien und China wurden OSM im April 2007 von Automotive Navigation Data (AND) beigesteuert. Im Dezember 2007 war die Oxford University die bekannteste Organisation, die OpenStreetMap-Daten in ihre Hauptwebsite integriert hat. Seitdem tragen über 2 Millionen registrierte Benutzer Daten zu diesem Projekt bei, indem sie GPS-Geräte, Luftaufnahmen und manuelle Erhebungen verwenden. Diese von der Community bereitgestellten Daten werden unter der Open Database License zur Verfügung gestellt. Eine in England registrierte, gemeinnützige Organisation OpenStreetMap Foundation unterhält die OSM-Site.

## OSM-Dateiformat ##

Es gibt viele Möglichkeiten und Dateiformate, um geografische Daten zu speichern, aber das **OSM**-Dateiformat ist auf OpenStreetMap beschränkt. OSM ist ein speziell entwickeltes Standardformat, das einfach über das Internet transportiert werden kann. Eine .osm-Datei ist ein strukturiertes, geordnetes Format, das in XML kodiert ist. In OpenStreetMap gibt es vier Pivot-Elemente zum Speichern der topologischen Datenstruktur:

{{< figure src="../OSM.png" alt="OSM-Dateiformat" >}}


|Knoten|Wege|Beziehungen|Tags
---|---|---|---|
|<ul><li> Stellt die geografische Position dar, die als Breiten- und Längenpaare gespeichert ist.</li><li> Wird verwendet, um Kartenmerkmale ohne Größe darzustellen, z. B. Berggipfel.</li></ul> |<ul><li> Sortierte Listen von Knoten, die eine Polylinie oder ein Polygon kennzeichnen</li><li> Repräsentieren lineare Features wie Straßen und Flüsse sowie Zonen wie Parkflächen, Dschungel und Parks.</li></ul> |<ul><li> Sortierte Listen von Knoten und Wegen stellen ihre Beziehung dar wie Schranken und Wenden auf Straßen, Autobahnen überspannen verschiedene bestehende Wege und Bereiche mit Löchern.</li></ul> |<ul><li> Speichern Sie Metadaten über die Kartenobjekte.* Immer mit einem Knoten, Weg oder einer Beziehung verbunden</li></ul>


Tags werden verwendet, um physische Bodenmerkmale (Gebäude und Straßen usw.) in OpenStreetMap zu charakterisieren. Jedes Tag bezieht sich auf ein geografisches Merkmal des Merkmals, das durch diesen spezifischen Knoten oder diese Beziehung dargestellt wird. In diesem kostenlosen Tagging-System kann zur Beschreibung eines Features eine unbegrenzte Anzahl von Attributen in eine Karte aufgenommen werden. Spezifische Schlüssel-Wert-Kombinationen, die von registrierten Benutzern unterstützt werden, dienen als informelle Standards für die häufig verwendeten Tags. Neue Tags können jedoch immer dann erstellt werden, wenn neue Aspekte die Analyse zuvor nicht zugeordneter Attribute der Merkmale erfordern. Die meisten Funktionen verwenden nur eine kleine Anzahl von Tags zur Beschreibung.

Drei Arten von Dateien werden von OSM verwendet, um seine Hauptdaten zu speichern.

OSM behandelt alle diese Dateien mit den Informationen über ihre Formatierungsdetails. Aber dieselben internen Objekte werden von diesen Dateien erzeugt. Für Datendateien ist das sichtbare Flag für OSM-Objekte immer wahr, was für Verlaufs- und Änderungsdateien nicht der Fall ist.

Im allgemeinen Gebrauch gibt es eine Vielfalt an OSM-Dateiformaten. Dateiformate definieren die Inhaltscodierung auf Festplatte oder Kabel in Bits und Bytes. OSM kann maximal diese Formate lesen und schreiben.

**XML**

Das ursprüngliche OSM-Format ist XML-basiert. Die Rückgabedaten der Haupt-OSM-Datenbank-API sind im XML-Format.

**PBF**

Die Codierung von Protokollpuffern basiert auf dem Binärformat und ist eines der kompaktesten Formate.

**O5M/O5C**

Auf dem Binärformat basierendes einfacheres Format, das jedoch relativ selten verwendet wird. OSM kann dieses Format lesen, aber nicht schreiben.

**OPL**

Ein einfaches Format, das zur Verwendung mit standardmäßigen UNIX-Befehlszeilentools vorgeschlagen wird. Ähnlich wie CSV-Dateien, erlaubt eine OSM-Entität in einer Zeile.

**DEBUGGEN**

Ein textbasiertes Format, das zum Debuggen erstellt werden soll. Der OSM kann dieses Format schreiben, aber nicht lesen.

**SCHWARZES LOCH**

Ein Dummy-Format, das über alle Daten verfügt. Der OSM kann dieses Format schreiben, aber nicht lesen.

## OSM-Datenspeicherung ##

Die **PostgreSQL**-Hauptdatenbank von OSM enthält die Hauptkopie der OSM-Daten mit der PostGIS-Erweiterung. Für jedes Datenprimitiv verwaltet die Hauptdatenbank eine Tabelle, deren Zeilen einzelne Objekte speichern. Alle Bearbeitungen aktualisieren diese Datenbank und alle anderen Formate werden unter Verwendung dieser Datenbank gebildet. Es werden zahlreiche herunterladbare Datenbankpools erstellt, um Daten von einem Ort zum anderen zu übertragen. Zwei Formate, eines mit XML und das andere mit Protocol Buffer Binary Format (PBF), definieren diese Pools. Die vollständigen Daten werden in einer Datei namens planet.osm gespeichert

## Komprimierung in OSM-Dateien ##

Textbasierte Formate (XML, OPL und Debug) verwenden optional gzip- oder bzip2-Komprimierung.

## Verweise ##

* [OSM-Dateiformathandbuch](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [OSM lernen](https://learnosm.org/en/osm-data/getting-data/)

