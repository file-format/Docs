{
  "date" : "2021-07-29",
  "keywords" :[ "gpkg-Datei", "gpkg-Dateiformat", "was ist eine gpkg-Datei", "Datei", "gpkg-Beispiel", "gpkg-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPKG - GeoPackage-Formatdateien",
  "description":"Erfahren Sie mehr über das GPKG-Dateiformat und APIs, die GPKG-Dateien erstellen und öffnen können.",
  "linktitle" : "GPKG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Was ist eine GPKG-Datei?
Eine Datei mit der Erweiterung .gpkg besteht aus einem geografischen Informationssystem, das als SQLite-Datenbankcontainer implementiert ist und Daten- und Metadatentabellen mit typischen Definitionen, Formatbeschränkungen, Integritätserklärungen und Inhaltseinschränkungen enthält. Es wurde 2014 veröffentlicht; vom OGC (Open Geospatial Consortium) im Auftrag des US-Militärs definiert. Verschiedene Regierungen, kommerzielle und Open-Source-Organisationen unterstützen das GeoPackage umfassend.

## GPKG-Dateiformat
Ein GeoPackage besteht aus einer erweiterten SQLite 3-Datenbankdatei; Ein Standard definiert eine Reihe von Regeln (erforderliche Konventionen) für:
- Speichern von Kachelmatrixsätzen von Bildern
- Vektorfunktionen
- Rasterkarten in verschiedenen Maßstäben
- Metadaten und Schema

Sie können ein GeoPackage erweitern, indem Sie die in Abschnitt 2.3 des Standards definierten Erweiterungsregeln verwenden. Der Zweck des Entwerfens eines GeoPackage bestand darin, eine möglichst einfache Datenbank zu erstellen und sie in eine gebrauchsfertige einzelne Datei aufzunehmen. Dadurch ist es ideal für mobile Anwendungen im Offline-Modus und schnelles Teilen auf Cloud-Speicher oder USB-Speichergeräten usw.

### GPKG-Inhalt
Die GeoPackages enthalten eine Reihe von Tabellen, wie andere relationale Datenbanken. Diese Tabellen können entweder benutzerdefinierte Tabellen oder Metadatentabellen sein. GeoPackages bestehen aus zwei obligatorischen Metadatentabellen:

#### gpkg_contents
Ein Inhaltsverzeichnis für ein GeoPackage. Die obligatorischen Spalten in dieser Tabelle sind:

- **table_name**: der tatsächliche Name der benutzerdefinierten Datentabelle;
- **data_type**: der Datentyp, zB Titel, Features und Attribute;
- **Kennung und Beschreibung**: für Menschen lesbarer Text ;
- **last_change**: das Informationsdatum der letzten Änderung im ISO 8601-Format;
- **min_x, min_y, max_x und max_y**: die räumlichen Ausdehnungen des Inhalts. ;
- **srs_id**: Raumbezugssystem .

#### gpkg_spatial_ref_sys
Für Raumbezugsinhalte; einschließlich, aber nicht beschränkt auf Kacheln und Features, muss jede Inhaltszeile auf ein Koordinatenreferenzsystem verweisen; in der Tabelle **gpkg_spatial_ref_sys** gespeichert. Die obligatorischen Spalten in dieser Tabelle sind:

- **srs_name, description**: ein für Menschen lesbarer Name und eine Beschreibung für den SRS;
– **srs_id**: eine eindeutige Kennung für den SRS; auch der Primärschlüssel für die Tabelle;
- **Organisation**: Groß-/Kleinschreibung beachtender Name der definierenden Organisation.
- **organization_coordsys_id**: Numerische ID des von der Organisation zugewiesenen SRS;
- **Definition**: Bekannte Textdefinition des SRS.


## Verweise

* [GeoPackage - von Wikipedia)](https://en.wikipedia.org/wiki/GeoPackage)
* [Erste Schritte mit GeoPackage](http://www.geopackage.org/guidance/getting-started.html)

