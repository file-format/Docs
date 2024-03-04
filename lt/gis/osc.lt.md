{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC – OpenStreetMap Keisti failo formatą",
  "description":"Sužinokite apie OSC failo formatą ir API, kurios gali kurti ir atidaryti OSC failus.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-lt",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Kas yra OSC failas?

OSC failas yra Keisti failo formatą, kuriame yra modifikuoti esamo .osm gatvių žemėlapio duomenys. Jame pateikiama informacija apie [OSM file](/gis/osm/) pakeitimus. OSC faile gali būti trijų tipų OSM duomenų modifikavimo operacijos, ty įterpti, keisti arba ištrinti. Šie pakeitimų failai dažniausiai naudojami duomenims eksportuoti iš OSM redaktoriaus ir importuoti į kitą redaktorių.

OSC failus galite atidaryti naudodami Merkaartar ir osmchange programinę įrangą.

## OSC failo formatas

OSC failai paprastai išsaugomi JOSM failo formatu, kur pakeitimai pateikiami žymomis. Jis prasideda žyma osmChange, kuri nurodo failo pradžią. Antrinės žymos nurodo, ar tai įterpimo, modifikavimo ar ištrynimo operacija, kuri turi būti atlikta atitinkamame OSM failo mazge. Mazgo turinyje iš tikrųjų yra osm žymos turinys.

### OSC failo formato pavyzdys

Toliau pateikiamas mazgo modifikavimo operacijos pavyzdys. Kiekvienas elementas turi turėti pakeitimų rinkinio ID ir versijos numerį.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Nuorodos

* [JOSM failo formatas](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


