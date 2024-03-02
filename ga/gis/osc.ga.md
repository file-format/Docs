{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Athraigh Formáid an Chomhaid",
  "description":"Foghlaim faoi fhormáid comhaid OSC agus APIanna ar féidir leo comhaid OSC a chruthú agus a oscailt.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-ga",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Cad is comhad OSC ann?

Is éard atá i gcomhad OSC ná Formáid Comhaid Athraithe ina bhfuil sonraí léarscáile sráide modhnaithe do léarscáil sráide .osm atá ann cheana féin. Tá faisnéis ann faoi na hathruithe atá le déanamh ar an [OSM file](/gis/osm/). Féadfaidh trí chineál oibríochta modhnuithe a bheith ag comhad OSC ar shonraí OSM .i. `cuir isteach`, `mionathraigh`, nó `scrios`. Úsáidtear na comhaid athraithe seo go coitianta chun sonraí a onnmhairiú amach as eagarthóir OSM agus a allmhairiú chuig eagarthóir eile.

Is féidir leat comhaid OSC a oscailt le bogearraí Merkaartar agus osmchange.

## Formáid Comhaid OSC

Déantar comhaid OSC a shábháil go coitianta i bhformáid comhaid JOSM áit a léirítear na hathruithe le clibeanna. Tosaíonn sé leis an gclib `osmChange` a léiríonn tús an chomhaid. Sonraítear leis na fochlibeanna más oibríocht ionsáite, modhnaithe nó scriosta é atá le déanamh ar an nód comhfhreagrach i gcomhad OSM. Tá an t-ábhar atá ar chlib osm i ndáiríre in ábhar nód.

### Sampla Formáid Comhaid OSC

Seo a leanas sampla d'oibríocht mhodhnú ar nód. Caithfidh ID an tsocraithe athruithe agus uimhir leagain a bheith ag gach eilimint.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Tagairtí

* [Formáid Comhaid JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format )


