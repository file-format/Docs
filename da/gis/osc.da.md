{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Skift filformat",
  "description":"Lær om OSC-filformat og API'er, der kan oprette og åbne OSC-filer.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-da",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Hvad er en OSC fil?

En OSC-fil er et ændringsfilformat, der indeholder modificerede gadekortdata for et eksisterende .osm-gadekort. Den indeholder oplysninger om de ændringer, der skal foretages i [OSM file](/gis/osm/). OSC-filen kan have tre mulige typer ændringsoperationer på OSM-data, dvs. 'indsæt', 'modificerer' eller 'slet'. Disse ændringsfiler bruges almindeligvis til at eksportere data ud af OSM-editor og importere til en anden editor.

Du kan åbne OSC filer med Merkaartar og osmchange software.

## OSC filformat

OSC-filer gemmes normalt i JOSM-filformat, hvor ændringerne er repræsenteret af tags. Det starter med `osmChange` tag, der angiver begyndelsen af filen. Undertaggene angiver, om det er en indsæt-, ændrings- eller sletoperation, der skal udføres på den tilsvarende node i OSM-filen. Indholdet af en node indeholder faktisk indholdet af et osm-tag.

### Eksempel på OSC-filformat

Følgende er et eksempel på ændringsoperation på en node. Hvert element skal have et ændringssæt-id og et versionsnummer.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Referencer

* [JOSM-filformat](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


