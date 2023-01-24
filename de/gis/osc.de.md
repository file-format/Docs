{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSC - OpenStreetMap Dateiformat ändern",
  "description":"Erfahren Sie mehr über das OSC-Dateiformat und APIs, die OSC-Dateien erstellen und öffnen können.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Was ist eine OSC-Datei?

Eine OSC-Datei ist ein Änderungsdateiformat, das geänderte Straßenkartendaten für eine vorhandene .osm-Straßenkarte enthält. Es enthält Informationen über die an der [OSM-Datei](/de/gis/osm/) vorzunehmenden Änderungen. Die OSC-Datei kann drei mögliche Arten von Änderungsoperationen an OSM-Daten haben, dh „Einfügen“, „Ändern“ oder „Löschen“. Diese Änderungsdateien werden häufig verwendet, um Daten aus dem OSM-Editor zu exportieren und in einen anderen Editor zu importieren.

Sie können OSC-Dateien mit Merkaartar und osmchange-Software öffnen.

## OSC-Dateiformat

OSC-Dateien werden üblicherweise im JOSM-Dateiformat gespeichert, in dem die Änderungen durch Tags dargestellt werden. Es beginnt mit dem `osmChange`-Tag, das den Anfang der Datei anzeigt. Die untergeordneten Tags geben an, ob es sich um eine Einfüge-, Änderungs- oder Löschoperation handelt, die auf dem entsprechenden Knoten in der OSM-Datei ausgeführt werden soll. Der Inhalt eines Knotens enthält tatsächlich den Inhalt eines osm-Tags.

### Beispiel für ein OSC-Dateiformat

Im Folgenden finden Sie ein Beispiel für eine Änderungsoperation an einem Knoten. Jedes Element muss eine Changeset-ID und eine Versionsnummer haben.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Verweise

* [JOSM-Dateiformat](https://wiki.openstreetmap.org/wiki/JOSM_file_format)

