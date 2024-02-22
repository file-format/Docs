{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC – OpenStreetMap Fájlformátum módosítása",
  "description":"Ismerje meg az OSC fájlformátumot és az API-kat, amelyek OSC-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-hu",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Mi az OSC fájl?

Az OSC-fájl egy Change File Format, amely egy meglévő .osm utcatérkép módosított utcatérkép-adatait tartalmazza. Információkat tartalmaz a(z) {{HIPERLINK1}} változásairól. Az OSC-fájl három lehetséges típusú módosítási műveletet tartalmazhat az OSM-adatokon, azaz beszúrás, módosítás vagy törlés. Ezeket a módosító fájlokat általában az adatok OSM-szerkesztőből való exportálására és másik szerkesztőbe történő importálására használják.

Az OSC fájlokat Merkaartar és osmchange szoftverrel nyithatja meg.

## OSC fájlformátum

Az OSC-fájlokat általában JOSM-fájlformátumban mentik, ahol a változtatásokat címkék jelzik. Az osmChange címkével kezdődik, amely a fájl elejét jelzi. Az alcímkék meghatározzák, hogy beszúrási, módosítási vagy törlési műveletről van-e szó, amelyet az OSM-fájl megfelelő csomópontján kell végrehajtani. Egy csomópont tartalma valójában egy osm címke tartalmát tartalmazza.

### OSC fájlformátum példa

Az alábbiakban egy csomópont módosítási műveletére mutatunk be példát. Minden elemnek rendelkeznie kell módosításkészlet-azonosítóval és verziószámmal.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Hivatkozások

* [JOSM fájlformátum](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


