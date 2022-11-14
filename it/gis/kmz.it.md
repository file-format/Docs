{
  "date" : "2019-10-11",
  "keywords" :[ "file kmz", "che cos'è un file kmz", "file", "esempio kmz", "estensione file kmz", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - Formato file compresso KML",
  "description":"Scopri il formato di file KMZ e le API che possono creare e aprire file KMZ.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file KMZ?

Il file KMZ (KML zippato) è una rappresentazione del file zippato [KML](/it/gis/kml/) che contiene informazioni geospaziali visualizzabili in applicazioni GIS come Google Earth. Le informazioni sui segnaposto sono rappresentate nel file come latitudine e longitudine insieme a un nome personalizzato. Il singolo file KMZ in pacchetto può essere condiviso facilmente con altri utenti. I file KMZ possono includere anche i dati del modello 3D per la rappresentazione geografica del modello. Un file KMZ può essere aperto in Google Maps salvando il file in una posizione online e quindi digitando l'URL nella casella di ricerca di Google Maps.

## Struttura del file ##

Il contenuto di un file MKZ è costituito da un file KML principale e da zero o più file associati. Può essere estratto utilizzando l'utilità di decompressione standard come WinZIP. Anche il formato file KMZ viene compresso in un archivio con un rapporto di compressione di 10:1. Puoi esportare i dati da Google Earth come applicazioni direttamente nel formato file KMZ. Il file KML principale è denominato **doc.kml**. Durante il confezionamento di un file KMZ, è possibile aggiungervi più di un file KML, ma ciò non sarà di alcun vantaggio poiché Google Earth cerca il primo file KML all'apertura del file KMZ e lo legge. Ignora qualsiasi altro file KML trovato nell'archivio. Per essere sicuri che il file KML desiderato venga letto da Google Earth, si consiglia di inserire un solo file KML all'interno del file KMZ.

Le immagini, i modelli, le trame, i file audio e le altre risorse a cui si fa riferimento nel file doc.kml vengono inseriti in un'altra sottocartella all'interno della cartella principale. Ciò può comportare anche una certa complessità a seconda del numero di file di supporto. I collegamenti a queste risorse costitutive possono essere referenziati relativamente o tramite referenziazione assoluta.

### Riferimento relativo ###

Quando le risorse vengono posizionate accanto al doc.kml principale all'interno di una sottocartella all'interno della cartella principale, il relativo riferimento può puntare a questi file di supporto come mostrato nell'esempio seguente (solo per icona).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Riferimento assoluto ###

Anche le risorse possono essere referenziate in modo assoluto. I riferimenti assoluti contengono l'URL completo del file collegato. Quando i file vengono inviati su un server centrale, il riferimento assoluto assicura che questi rimangano non ambigui rispetto al riferimento relativo. Non è consigliabile fare riferimento in modo assoluto ai file locali poiché questi collegamenti si interromperanno quando i file vengono spostati su un nuovo sistema. Un esempio di riferimento assoluto è il seguente:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Guarda anche ##

* [GeoJSON](/it/gis/geojson/)

## Riferimenti ##

* [File di Google Earth e KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

