{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file TCX - File XML del centro di formazione",
  "description":"Scopri il formato di file TCX e le API che possono creare e aprire file TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Che cos'è un file TCX?

Un file TCX (Training Center XML) è un formato di scambio dati utilizzato per condividere dati tra dispositivi fitness. È stato introdotto nel 2008 con il prodotto Garmin Training Center. I dati di allenamento come frequenza cardiaca, cadenza della corsa, cadenza della bicicletta, calorie e tempo sul giro sono memorizzati nel formato [XML](/it/web/xml/) all'interno del file TCX. Inoltre, nel file TCX sono inclusi anche i dati di riepilogo sul percorso di allenamento. I file TCX sono simili ai file [FIT](/it/gis/fit/) creati con i dispositivi indossabili per lo sport Garmin.

## Formato file TCX - Ulteriori informazioni

I file TCX vengono salvati su disco come file XML con ogni record salvato come attività. Un'attività comprende tutti i dati di un allenamento come tempo, tempo sul giro, Id, frequenza cardiaca, intensità, cadenza e informazioni sulla traccia che contengono le coppie di posizioni insieme al timestamp per quella posizione lat-long simile al [GPX](/it/gis/gpx/).

### Versioni del formato file TCX

Esistono due versioni di questo formato con i propri schemi XML ospitati da Garmin. Di seguito ne elenchiamo alcuni:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Protocollo dati TCX

Una versione rapida del formato XML TCX è disponibile su Github come [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Riferimenti ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [Visualizzatore TCX](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

