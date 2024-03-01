{
  "date": "2019-10-11",
  "keywords": [
"gpx tiedosto",
"mikä on gpx-tiedosto",
"tiedosto",
"gpx esimerkki",
"gpx tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPX - GPX Exchange -tiedostomuoto",
  "description": "Opi GPX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata GPX-tiedostoja.",
  "linktitle": "GPX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gp-fix"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on GPX-tiedosto?

GPX-laajennuksella varustetut tiedostot edustavat GPS Exchange -muotoa GPS-tietojen vaihtoon sovellusten ja Internetin verkkopalvelujen välillä. Se on kevyt XML-tiedostomuoto, joka sisältää GPS-tietoja eli reittipisteitä, reittejä ja jälkiä, jotka useat ohjelmat tuovat ja punaiset. GPX-tiedostomuoto on avoin, ja useat sovellukset ja GPS-laitteet tukevat sitä. GPS-tiedot tällaisista tiedostoista voidaan ladata näytettäväksi karttasovelluksissa geospatiaalisia tarkoituksia varten.

## GPX-tiedostomuoto ##

GPX-tiedosto koostuu leveys- ja pituusasteiden sijaintitiedoista, korkeusarvoista ja muista mahdollisesti muista kuvaavista tiedoista. Sijaintitiedot ilmaistaan desimaaliasteina ja korkeus metreinä. GPX-tiedoston aika on ilmoitettu koordinoidussa yleisajassa (UTC) ISO 8601 -muodossa. GPX-tiedoston käytön edut ovat seuraavat:

* GPX:n avulla voit vaihtaa tietoja kasvavan Windows-, MacOS-, Linux-, Palm- ja PocketPC-ohjelmien luettelon kanssa.

* GPX voidaan muuntaa muihin tiedostomuotoihin käyttämällä yksinkertaista verkkosivua tai muunnosohjelmaa.

* GPX perustuu XML-standardiin, joten monet käyttämistäsi uusista ohjelmista (esimerkiksi Microsoft Excel) voivat lukea GPX-tiedostoja.

* GPX:n avulla kaikkien verkossa olevien on helppo kehittää uusia ominaisuuksia, jotka toimivat välittömästi suosikkiohjelmiesi kanssa.


{{HYPERLINKKI}} näyttää GPX-tiedostomuodon esityksen viitteeksi.

### Olennaiset tiedot ###

Seuraavassa on tärkeitä tietoja, jotka ovat osa GPX-tiedostoa GPS-tietojen esittämiseksi.

* **Reittipisteet**: Reittipiste on pisteen WGS84 (GPS) -koordinaatit ja edustaa OGR-tyypin wkbPoint ominaisuuksia.

* **Reitit**: edustaa OGR-tyypin wkbLineString-ominaisuuksien kerrosta. Se sisältää luettelon jälkipisteistä, jotka ovat reittipisteitä, jotka näyttävät käännöksiä tai vaihepisteitä, jotka johtavat määränpäähän

* **Raidat**: Jäljet edustavat OGR-tyypin wkbMultiLineString-ominaisuuksien kerrosta. Se koostuu vähintään yhdestä segmentistä, joka sisältää reittipisteitä järjestetyssä pisteluettelossa, joka kuvaa polkua. Se koostuu luettelosta jälkipisteistä, jotka edustavat jatkuvaa GPS-reittiä.


### GPX-esimerkkitiedosto ###

Seuraava GPX-tiedosto näyttää GPS-tietojen järjestämisen GPX-tiedostossa ja voi antaa hyvän käsityksen GPX-tiedoston sisällöstä.

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

## Viitteet ##

* [GPX-tiedostomuoto](https://www.topografix.com/gpx.asp)

* [GPX - Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)


