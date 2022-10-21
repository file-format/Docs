{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das ACCDT-Dateiformat und APIs, die ACCDT-Dateien erstellen und öffnen können.",
  "title" :"ACCDT - Microsoft Access 2007-Vorlagendatenbank-Dateiformat",
  "linktitle" :"ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Was ist eine ACCDT-Datei?

Eine Datei mit der Erweiterung .accdt ist eine Microsoft Access-Datenbankvorlagendatei, die vordefinierte Datenbankelemente enthält. Diese Elemente sind eine Sammlung von Strukturen, die Datenbankanwendungen definieren, wie Datenbankschemata zum Speichern von Daten, Layoutbeschreibungen für Ansichten der Daten und Metadaten, die die Datenbank beschreiben. Als Vorlagendateien können ACCDT-Dateien verwendet werden, um Datenbanken basierend auf den darin verfügbaren Vorlageneinstellungen zu erstellen. Die resultierenden Datenbankdateien werden als [ACCDB](/de/database/accdb/)-Dateien gespeichert und mit Daten in Tabellen gefüllt. Microsoft Access 2007 und höher können ACCDT-Dateien öffnen.

## ACCDT-Dateiformat

ACCDT-Vorlagendateien basieren auf den Office Open XML-Spezifikationen und alle Daten sind in einem ZIP-Paket enthalten. Struktur- und Inhaltsinformationen der Datenbank sind in den [XML](/de/web/xml/)-Dateien und Textdateien enthalten und über Beziehungen miteinander verknüpft. Sie können eine ACCDT-Datei in die Erweiterung [.zip](/de/compression/zip/) umbenennen und eine beliebige Komprimierungssoftware verwenden, um den Inhalt des ZIP-Archivs zu extrahieren.

### Dateistruktur

ACCDT-Dateien sind Pakete, die eine Sammlung verwandter Teile enthalten. Jeder **Teil** speichert Informationen über den Inhalt einer Datenbankanwendung unter Verwendung von XML-, Text- und Binärformaten, darunter:

* Datenbankobjekte
* Zugehörige Metadaten
* Struktur des Pakets

#### Paket

Ein Paket ist ein [ZIP](/de/compression/zip/)-Archiv, das mehrere Teile enthält und den Open Packaging Conventions entspricht, die in [ISO/IEC-29500-2](https://go.microsoft.com/fwlink/ ?LinkId=150883). ACCDT-Dateien müssen mindestens einen Template-Metadatenteil enthalten, der das Ziel einer Beziehung sein sollte. Diese Template-Metadaten sind der Anfangsteil einer ACCDT-Datei.

#### Teil

Ein Teil ist ein Strom von Bytes, dem ein Typ zugeordnet ist, um die Art und den Typ des darin gespeicherten Inhalts anzugeben. Die Teileaufzählung gibt gültige Teile, gültige Inhaltstypen und erforderliche Beziehungen zwischen allen Teilen in einem Paket an.

#### Beziehung

„Package Relationship“ – wobei das Ziel ein Teil und die Quelle das Paket als Ganzes ist.

„Teil-zu-Teil-Beziehung“ – wobei das Ziel ein Teil und die Quelle ein Teil des Pakets ist.

„Explizite Beziehung“ – wo eine Ressource von den Inhalten eines Quellteils referenziert wird, indem auf ein Beziehungselement durch den Wert seines ID-Attributs verwiesen wird.

„Implizite Beziehung“ – eine Beziehung, die nicht explizit ist.

„Interne Beziehung“ – wobei das Ziel ein Teil des Pakets ist.

„Externe Beziehung“ – wobei das Ziel eine externe Ressource ist, die nicht im Paket enthalten ist.

## Verweise ##

* [Dateiformat für Zugriffsvorlage](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

