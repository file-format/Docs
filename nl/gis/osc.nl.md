{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Bestandsformaat wijzigen",
  "description":"Meer informatie over de OSC-bestandsindeling en API's waarmee OSC-bestanden kunnen worden gemaakt en geopend.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-nl",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Wat is een OSC-bestand?

Een OSC-bestand is een wijzigingsbestandsindeling die gewijzigde stratenkaartgegevens bevat voor een bestaande .osm-stratenkaart. Het bevat informatie over de wijzigingen die moeten worden doorgevoerd in de [OSM file](/gis/osm/). OSC-bestanden kunnen drie mogelijke typen wijzigingsbewerkingen op OSM-gegevens hebben, namelijk 'insert', 'modify' of 'delete'. Deze wijzigingsbestanden worden doorgaans gebruikt om gegevens uit de OSM-editor te exporteren en naar een andere editor te importeren.

U kunt OSC-bestanden openen met Merkaartar- en osmchange-software.

## OSC-bestandsindeling

OSC-bestanden worden doorgaans opgeslagen in de JOSM-bestandsindeling, waarbij de wijzigingen worden weergegeven door tags. Het begint met de tag `osmChange` die het begin van het bestand aangeeft. De subtags specificeren of het een invoeg-, wijzig- of verwijderbewerking is die moet worden uitgevoerd op het corresponderende knooppunt in het OSM-bestand. De inhoud van een knooppunt bevat feitelijk de inhoud van een osm-tag.

### Voorbeeld van OSC-bestandsindeling

Hieronder volgt een voorbeeld van een wijzigingsbewerking op een knooppunt. Elk element moet een wijzigingenset-ID en een versienummer hebben.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Referenties

* [JOSM-bestandsindeling](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


