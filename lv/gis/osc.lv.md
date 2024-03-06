{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC — OpenStreetMap faila formāta maiņa",
  "description":"Uzziniet par OSC failu formātu un API, kas var izveidot un atvērt OSC failus.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-lv",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Kas ir OSC fails?

OSC fails ir Mainīt faila formātu, kas satur modificētus ielu kartes datus esošai .osm ielu kartei. Tajā ir informācija par izmaiņām, kas radīsies [OSM file](/gis/osm/). OSC failam var būt trīs iespējamie OSM datu modifikācijas operāciju veidi, piemēram, ievietot, mainīt vai dzēst. Šie izmaiņu faili parasti tiek izmantoti datu eksportēšanai no OSM redaktora un importēšanai citā redaktorā.

Jūs varat atvērt OSC failus, izmantojot Merkaartar un osmchange programmatūru.

## OSC faila formāts

OSC faili parasti tiek saglabāti JOSM faila formātā, kur izmaiņas attēlo tagi. Tas sākas ar tagu osmChange, kas norāda faila sākumu. Apakštagi norāda, vai tā ir ievietošanas, modificēšanas vai dzēšanas darbība, kas jāveic attiecīgajā OSM faila mezglā. Mezgla saturs faktiski satur osm taga saturu.

### OSC faila formāta piemērs

Tālāk ir sniegts mezgla modifikācijas darbības piemērs. Katram elementam ir jābūt izmaiņu kopas ID un versijas numuram.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Atsauces

* [JOSM faila formāts](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


