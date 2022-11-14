{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "file", "estensione", "formato file", "Posizione GPS", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - Formato file posizione GPS",
  "description":"Scopri il formato di file LOC e le API che possono creare e aprire file LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Che cos'è un file LOC?

Un file con estensione .loc è un file di posizione GPS che contiene posizioni geospaziali come waypoint. Un waypoint è una coppia di valori di latitudine-longitudine che si riferiscono a una posizione utilizzata dalle applicazioni GIS (Geographical Information System). I programmi di mappatura GPS, come DeLorme Topo, utilizzano i file LOC per leggere e visualizzare le informazioni contenute in questi file LOC come livelli selezionabili dagli utenti finali. Inoltre, vengono utilizzati per scambiare dati GPS tra le applicazioni. I file LOC possono essere aperti utilizzando applicazioni come [TopoGrafix EasyGPS](https://www.easygps.com/) che visualizza il contenuto di tali file come livelli e dati tracciati sulla mappa nella rispettiva geolocalizzazione.

## Formato file LOC - Ulteriori informazioni

I file LOC hanno somiglianze con i file [GPX](/it/gis/gpx/) ma vengono salvati in un formato diverso. Questi vengono salvati come file [XML](/it/web/xml/) in cui il contenuto dei waypoint e le informazioni associate sono contenuti in tag strutturati. Poiché XML è un linguaggio generalizzato per lo scambio di dati tra diverse applicazioni, ciò facilita lo scambio di dati LOC con altre applicazioni.

## Formato file LOC - Esempio

Di seguito è riportato l'intestazione e il testo di un waypoint da un file LOC. Come si può vedere, le informazioni di intestazione contengono l'origine della posizione dei dati. Il waypoint contiene informazioni come l'"ID" e i dati di contenuto associati associati al waypoint. Infine, il waypoint è una raccolta di valori di latitudine e longitudine e il testo associato a questo particolare waypoint.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Riferimenti

* [TopGraphic EasyGPS](https://www.easygps.com/)

