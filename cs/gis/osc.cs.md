{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Změna formátu souboru",
  "description":"Přečtěte si o formátu souborů OSC a rozhraních API, která mohou vytvářet a otevírat soubory OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-cs",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Co je soubor OSC?

Soubor OSC je formát souboru Change File Format, který obsahuje upravená data mapy ulic pro existující mapu ulic .osm. Obsahuje informace o změnách, které mají být provedeny v [OSM file](/gis/osm/). Soubor OSC může mít tři možné typy operací úprav na datech OSM, tj. `vložit`, `upravit` nebo `smazat`. Tyto soubory změn se běžně používají k exportu dat z editoru OSM a importu do jiného editoru.

Soubory OSC můžete otevřít pomocí softwaru Merkaartar a osmchange.

## Formát souboru OSC

Soubory OSC se běžně ukládají ve formátu souboru JOSM, kde jsou změny reprezentovány značkami. Začíná tagem `osmChange`, který označuje začátek souboru. Dílčí značky určují, zda se jedná o operaci vložení, úpravy nebo odstranění, která má být provedena na odpovídajícím uzlu v souboru OSM. Obsah uzlu ve skutečnosti obsahuje obsah osm tagu.

### Příklad formátu souboru OSC

Následuje příklad operace úpravy na uzlu. Každý prvek musí mít ID changesetu a číslo verze.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Reference

* [Formát souboru JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


