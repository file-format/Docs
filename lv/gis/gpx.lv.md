{
  "date": "2019-10-11",
  "keywords": [
"gpx failu",
"kas ir gpx fails",
"failu",
"gpx piemērs",
"gpx faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPX — GPX Exchange faila formāts",
  "description": "Uzziniet par GPX failu formātu un API, kas var izveidot un atvērt GPX failus.",
  "linktitle": "GPX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gp-lvx"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir GPX fails?

Faili ar GPX paplašinājumu ir GPS Exchange formāts GPS datu apmaiņai starp lietojumprogrammām un tīmekļa pakalpojumiem internetā. Tas ir viegls XML faila formāts, kas satur GPS datus, ti, pieturas punktus, maršrutus un pēdas, kas jāimportē un sarkanā krāsā ar vairākām programmām. GPX faila formāts ir atvērts, un to atbalsta dažādas lietojumprogrammas un GPS ierīces. GPS datus no šādiem failiem var ielādēt attēlošanai kartēšanas lietojumprogrammās ģeotelpiskā nolūkā.

## GPX faila formāts ##

GPX fails sastāv no platuma un garuma atrašanās vietas datiem, augstuma vērtībām un citas, iespējams, citas aprakstošas informācijas. Atrašanās vietas dati tiek izteikti decimālgrādos, un augstums ir metros. Laiks GPX failā ir norādīts koordinētajā universālajā laikā (UTC), izmantojot ISO 8601 formātu. GPX faila izmantošanas priekšrocības ir šādas:

* GPX ļauj apmainīties ar datiem ar augošu programmu sarakstu operētājsistēmām Windows, MacOS, Linux, Palm un PocketPC.

* GPX var pārveidot citos failu formātos, izmantojot vienkāršu tīmekļa lapu vai pārveidotāju programmu.

* GPX pamatā ir XML standarts, tāpēc daudzas no jaunajām programmām, kuras izmantojat (piemēram, Microsoft Excel), var lasīt GPX failus.

* GPX ļauj ikvienam tīmeklī viegli izstrādāt jaunas funkcijas, kas uzreiz darbosies ar jūsu iecienītākajām programmām.


[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) uzziņai parāda GPX faila formāta attēlojumu.

### Būtiski dati ###

Tālāk ir sniegti būtiski dati, kas ir daļa no GPX faila GPS datu attēlošanai.

* **Maršruta punkti**: maršruta punkts ir punkta WGS84 (GPS) koordinātas un attēlo OGR tipa wkbPoint pazīmju slāni.

* **Maršruti**: attēlo OGR tipa wkbLineString līdzekļu slāni. Tajā ir iekļauts trases punktu saraksts, kas ir maršruta punkti, kas parāda pagrieziena vai posma punktus, kas ved uz galamērķi

* **Ieraksti**: celiņi ir OGR tipa wkbMultiLineString līdzekļu slānis. Tas sastāv no vismaz viena segmenta, kurā ir maršruta punkti sakārtotā punktu sarakstā, kas apraksta ceļu. Tas sastāv no ceļa punktu saraksta, kas attēlo nepārtrauktu GPS maršrutu.


### GPX piemēra fails ###

Šis GPX fails parāda GPS datu organizēšanu GPX failā un var sniegt labu priekšstatu par GPX faila saturu.

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

## Atsauces Nr.

* [GPX faila formāts](https://www.topografix.com/gpx.asp)

* [GPX — Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)


