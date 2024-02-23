{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Ändra filformat",
  "description":"Lär dig mer om OSC-filformat och API:er som kan skapa och öppna OSC-filer.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-sv",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Vad är en OSC fil?

En OSC-fil är ett ändringsfilformat som innehåller modifierad gatukarta för en befintlig .osm-gatakarta. Den innehåller information om de ändringar som ska göras i [OSM file](/gis/osm/). OSC-filen kan ha tre möjliga typer av modifieringsoperationer på OSM-data, dvs. infoga, modifiera eller ta bort. Dessa ändringsfiler används vanligtvis för att exportera data från OSM-editorn och importera till en annan editor.

Du kan öppna OSC-filer med Merkaartar och osmchange programvara.

## OSC filformat

OSC-filer sparas vanligtvis i JOSM-filformat där ändringarna representeras av taggar. Den börjar med osmChange-taggen som indikerar början av filen. Undertaggarna anger om det är en infoga, modifiera eller ta bort operation som ska utföras på motsvarande nod i OSM-filen. Innehållet i en nod innehåller faktiskt innehållet i en osm-tagg.

### Exempel på OSC-filformat

Följande är ett exempel på modifieringsoperation på en nod. Varje element måste ha ett ändringsuppsättnings-ID och ett versionsnummer.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Referenser

* [JOSM-filformat](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


