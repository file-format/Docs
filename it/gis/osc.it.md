{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Cambia formato file",
  "description":"Scopri il formato file OSC e le API che possono creare e aprire file OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-it",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Cos'è un file OSC?

Un file OSC è un formato file di modifica che contiene i dati della mappa stradale modificati per una mappa stradale .osm esistente. Contiene informazioni sulle modifiche da apportare a [OSM file](/gis/osm/). Il file OSC può avere tre possibili tipi di operazioni di modifica sui dati OSM, ovvero inserisci, modifica o elimina. Questi file di modifiche vengono comunemente utilizzati per esportare dati dall'editor OSM e importarli in un altro editor.

Puoi aprire file OSC con Merkaartar e il software osmchange.

## Formato file OSC

I file OSC vengono comunemente salvati nel formato file JOSM in cui le modifiche sono rappresentate da tag. Inizia con il tag `osmChange` che indica l'inizio del file. I sottotag specificano se si tratta di un'operazione di inserimento, modifica o eliminazione da eseguire sul nodo corrispondente nel file OSM. Il contenuto di un nodo contiene in realtà il contenuto di un tag osm.

### Esempio di formato file OSC

Di seguito è riportato un esempio di operazione di modifica su un nodo. Ogni elemento deve avere un ID del changeset e un numero di versione.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Riferimenti

* [Formato file JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


