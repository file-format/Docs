{
  "date" : "2019-10-11",
  "keywords" :[ "file gpx", "che cos'è un file gpx", "file", "esempio gpx", "estensione file gpx", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - Formato file di scambio GPX",
  "description":"Scopri il formato di file GPX e le API che possono creare e aprire file GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file GPX?

I file con estensione GPX rappresentano il formato GPS Exchange per lo scambio di dati GPS tra applicazioni e servizi Web su Internet. È un formato di file XML leggero che contiene dati GPS, ad esempio waypoint, rotte e tracce da importare e rossi da più programmi. Il formato file GPX è aperto ed è supportato da una varietà di applicazioni e dispositivi GPS. I dati GPS da tali file possono essere caricati per la visualizzazione su applicazioni di mappatura per scopi geospaziali.

## Formato file GPX ##

Un file GPX è costituito da dati sulla posizione di latitudine e longitudine, valori di elevazione e altre possibilmente altre informazioni descrittive. I dati sulla posizione sono espressi in gradi decimali e l'altitudine è espressa in metri. L'ora in un file GPX è in Coordinated Universal Time (UTC) utilizzando il formato ISO 8601. I vantaggi dell'utilizzo di un file GPX sono i seguenti:

* GPX ti consente di scambiare dati con un elenco crescente di programmi per Windows, MacOS, Linux, Palm e PocketPC.
* GPX può essere trasformato in altri formati di file utilizzando una semplice pagina Web o un programma di conversione.
* GPX è basato sullo standard XML, quindi molti dei nuovi programmi che usi (Microsoft Excel, ad esempio) possono leggere i file GPX.
* GPX rende facile per chiunque sul Web sviluppare nuove funzionalità che funzioneranno istantaneamente con i tuoi programmi preferiti.

Lo [Schema GPX](https://www.topografix.com/GPX/1/1/gpx.xsd) mostra la rappresentazione del formato file GPX come riferimento.

### Dati essenziali ###

Di seguito sono riportati i dati essenziali che fanno parte di un file GPX per la rappresentazione dei dati GPS.

* **Waypoint**: Un waypoint è una coordinata WGS84 (GPS) di un punto e rappresenta uno strato di caratteristiche di tipo OGR wkbPoint
* **Rotte**: rappresenta un livello di funzionalità di tipo OGR wkbLineString. Include un elenco di punti traccia, che sono punti di passaggio che mostrano una svolta o punti di tappa che portano a una destinazione
* **Tracce**: le tracce rappresentano il livello di funzionalità di tipo OGR wkbMultiLineString. È composto da almeno un segmento contenente waypoint in un elenco ordinato di punti che descrivono un percorso. Consiste in un elenco di punti traccia che rappresentano una traccia GPS continua.

### File di esempio GPX ###

Il seguente file GPX mostra l'organizzazione dei dati GPS in un file GPX e può dare una buona idea del contenuto di un file GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Riferimenti ##

* [Formato file GPX](http://www.topografix.com/gpx.asp)
* [GPX - Di Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

